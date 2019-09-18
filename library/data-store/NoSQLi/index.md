---
layout: page
title: "NoSQLi"
---

### Articles & Notes

- [x] [What is NoSQLi?](http://www.petecorey.com/blog/2017/07/03/what-is-nosql-injection/)
  * Variables passed are not always strings for NoSQL databases, they can be JSON objects, and if those are not validated properly, this can lead to query operators being passed in
- [x] [NoSQL - Wikipedia](https://en.wikipedia.org/wiki/NoSQL)
- [x] [OWASP - Testing for NoSQLi](https://www.owasp.org/index.php/Testing_for_NoSQL_injection)
  * Two methods listed here
    1. Direct injection / evaluation of code using strings that get passed to a query
    2. Using reserved variable names for various NoSQL databases with application programming variables
      * Ex. PHP $where & MongoDB $where, php $where could be a string and used in the Mongo query if $where for the query is not quoted properly
- [ ] [NoSQL Injections Analysis](https://www.infoq.com/articles/nosql-injections-analysis/)
  * Types of NoSQL Injection Attacks
    1. Tautologies - creating 'always true' conditions
    2. Union Queries - Similar concept to SQL injection UNIONs, data extration
    3. JavaScript Injections - Running arbitrary JavaScript in the database context
    4. PiggyBacking Queries - The ability to add additional queries beyond what the developer intended
    5. Origin Violation - Using CSRF to compromise a database
- [x] [Pentest People - NoSQLi](https://www.pentestpeople.com/nosql-injection/)
- [ ] [Does NoSQL Equal No Injection?](https://securityintelligence.com/does-nosql-equal-no-injection/)
- [ ] [NoSQLi in mongodb](https://zanon.io/posts/nosql-injection-in-mongodb)
- [ ] [REDIS NoSQLi](https://medium.com/@PatrickSpiegel/https-medium-com-patrickspiegel-nosql-injection-redis-25b332d09e58)
- [ ] [How to test for NoSQLi](https://security.stackexchange.com/questions/154104/how-to-test-for-nosql-injections)
- [ ] [mongo won't prevent NoSQLi](https://blog.sqreen.com/mongodb-will-not-prevent-nosql-injections-in-your-node-js-app/)
- [ ] [NoSQLi in Meteor](https://blog.designveloper.com/2016/08/06/nosql-injection-in-meteor-js-application/)
- [ ] [Hacking Nodejs + MongoDB](https://blog.websecurify.com/2014/08/hacking-nodejs-and-mongodb.html)
- [ ] [Server-Side JavaScript Injection](https://media.blackhat.com/bh-us-11/Sullivan/BH_US_11_Sullivan_Server_Side_WP.pdf)
- [ ] [NoSQL, But Even Less Security](http://blogs.adobe.com/asset/files/2011/04/NoSQL-But-Even-Less-Security.pdf)
- [ ] [NoSQLi](http://erlend.oftedal.no/blog/?blogid=110)
- [ ] [NoSQL/SSJS Injection](http://www.syhunt.com/?n=Articles.NoSQLInjection)
- [ ] [How does MongoDB address SQL or Query injection?](http://docs.mongodb.org/manual/faq/developers/#how-does-mongodb-address-sql-or-query-injection)
- [ ] [Hacking NodeJS and MongoDB](http://blog.websecurify.com/2014/08/hacking-nodejs-and-mongodb.html)
- [ ] [Attacking NodeJS and MongoDB](http://blog.websecurify.com/2014/08/attacks-nodejs-and-mongodb-part-to.html)

### Labs

- [NoSQLi Labs](labs/php-mongodb/)

### Tools

- [NoSQLMap](https://github.com/codingo/NoSQLMap)
- [payloads](https://github.com/cr0hn/nosqlinjection_wordlists)

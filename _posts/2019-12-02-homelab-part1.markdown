---
layout: post
title:  "Home Lab Part 1: Goals & Materials"
date:   2019-12-02
description: How I am setting up a home lab, and how you can too
categories: homelab
---

I am excited to finally get started on my home lab, I want to walk through how I am setting up mine, and offer some suggestions for anyone that wants to setup their own.

## Why

The most important first step is to figure out why you want to setup a lab, this will give you direction and clarity when it comes to determining your goals for the lab.  Taking the time to spend a few minutes on this will make you much more productive later on, and help you focus your efforts.  Ask yourself some questions.

- What are you hoping to learn?
- What are you curious about?
- How much time / money are you willing to invest?

To some, this may seem obvious, but it is worthwhile to at least consider and write it down if you haven't already.  There is no quicker way for a project to end up abandoned than to forget why you are doing it and lose focus.

For myself, I have been wanting to setup a home lab for quite a while now.  I tend to get bogged down in the things that I "have" to do at my day job.  A home lab is a way for me to stay passionate about technology because it is a project that I work on for the fun of it; it has no purpose outside of me discovering and learning something new.  I also find that a large part of exploiting systems, is understanding how they work and being curious about their configuration.  Having a lab will give me a greater understanding of how systems work, how they are configured, and what the potential weaknesses are.

In addition to being a passion project, this will have some benefits for my home life as well, like saving money by not having to maintain a Google Drive account any longer. Mostly though, this is for fun.  I intend to blog as I go through the process and learn some new things.  Next up is goals for the project.

## Goals

You have to decide what your goals are.  Do you want to learn more about virtualization software?  Are you interested in discovering more about networking, web applications, or Industrial Control Systems (ICS) environments?  Do you want to reverse engineer malware or chase bug bounties?  Thinking clearly through these things, and documenting them will help you focus and accomplish something with your lab, rather than being aimless and never getting anything done.  I find that even when I want to do something for 'fun', I need to start with goals in mind to keep me from getting distracted.  The following is what I came up with.

### My goals

### 1. [Network Attached Storage (NAS)](https://en.wikipedia.org/wiki/Network-attached_storage)

I want to get some storage space setup at home so that I can stop giving Google more of my privacy and money.  It will also be good to have a home media network so I can potentially eliminate physical DVDs, have a place to store photos, and other digital documents.  I have also come across NAS systems frequently during engagements, training, and other scenarios, I understand them but have never configured one myself.  This is a good opportunity for me to configure one and see where the potential for misconfiguration and vulnerabilities could lie with these systems.  I will also be able to make better recommendations about the security of these systems with a more thorough understanding.

### 2. Malware Sandbox, probably [Cuckoo Sandbox](https://cuckoosandbox.org/)

As someone that exploits systems, I want to study the tradecraft of others that do the same.  I also like catching bad guys and stopping them where I am able.  This means a malware sandbox will fit nicely in my kit of tools.  I could likely develop some sandbox-detecting implants, improve the sandbox itself, and share the knowledge that I gain with the community to make us better at cathing the real bad guys.

### 3. Firewall, probably [pfSense](https://www.pfsense.org/)

This one seems obvious, a firewall to create separate networks for various purposes. I also want to block and detect things that I don't want on my home network.  Lastly, I would like to setup a VPN for the outbound interface to avoid and sort of tracking and analytics done by my ISP, I wear a small tinfoil hat.

### 4. Random stuff that I don't want to pay Amazon to host

There is a lot of software and systems that I want to play around with for experimentation purposes, I could go broke trying to pay Amazon for all of that.

A lot of folks will probably shout "Use [Docker](https://www.docker.com/)!"  I have used Docker, and I still do, but this is for fun and learning.  If I set up a full on virtual corporate network, I see a lot of benefit in that for educational purposes from a systems administration perspective.  I can also test all the hacks I want to without any risk of repurcussion, and in a very realistic environment.

This includes something like [Moloch](https://github.com/aol/moloch) which is a full packet capture solution I have been wanting to run myself for a while now.  I have played around with it before, but never gone through the process of standing up my own instance.

### 5. Implant CI/CD pipeline

Implant authors need automated builds too...and this scratches my developer itch.

### 6. Password Cracking Rig

This one is a maybe, I haven't delved heavily into password cracking so far, but it could be good to have.  This one will probably get accelerated if I ever start a security assessments consulting business.

### 7. Industrial Control Systems (ICS) lab

I have taken some of the [CISA offered training](https://www.us-cert.gov/ics/Training-Available-Through-ICS-CERT) related to ICS and found it very interesting.  At some point in this process I would like to get some simulated ICS systems setup so that I can discover and tamper with the various protocols and devices, and see how they react to different tests and attacks.

### 8. Just 'cause

I'm a geek, and find tech interesting and enjoyable.  I have worked primarily on software at high layers and want to expirement with the full stack, from hardware all the way up to a running app.

## The Materials List

With goals in mind, it is easy to start coming up with a list of components.  I start by brainstorming as though I had all the money and resources I could ever want available to me, which help me decide on some of the important items such as, getting rack mount servers or a simple desktop server.  The brainstorming process helps develop my wish list; having the wish list makes it easy for me to determine a good purchase when I come across it.  Being on a budget and knowing what I want are the two things necessary to move forward with a purchase when the opportunity arises.  My list follows.

### A Rack

I decided to go with a rack mount system so that I can upgrade and swap items out over time.  I like having the flexibility to change independent pieces, have everything organized well, and contained so that my small children don't hurt themselves or the equipment in the process.  This also allows for placing my cable modem and wireless access point inside the cabinet so that I can keep all the tech items for the house / lab contained in a single cabinet.  I will get a drawer and a shelf for inside the cabinet also so that I can keep miscellaneous cables, cords, and computer items there also.  I am not a fan of having things scattered throughout the house and having to go digging for them whenever I need them, so going with a server rack / cabinet was a big decision for keeping everything together and organized.

### Server(s)

The biggest thing to note here is that I want to run quite a bit, so bigger is better.  I am planning to virtualize just about everything, so if I can get more I'll take it.  I had a few considerations for specifics.

I want to be able to house quite a bit of data on NAS, so a server with a fair number of drive slots and the ability to do a RAID configuration is a must.

### Uninterruptable Power Supply (UPS)

I would like to be able to gracefully shutdown in the event of a power outage, but not necessarily run for days / weeks on end.

### Switch

Something to distribute network connectivity, nothing more.  Maybe at some point I will get a fancy Cisco router and learn more about iOS, but at this point, I just want network connectivity for everything.

### Misc.

Monitor, keyboard, mouse, KVM.  As long as they work, I don't care.

## Wrapping Up

As I went through this process of writing goals, and making a list of materials I wanted, I started to look out for new and used equipment that would fit what I needed.  I was fortunate enought to find a ready setup for a good price on the used market.  In my next post, I will detail what I got and how I got started with it.

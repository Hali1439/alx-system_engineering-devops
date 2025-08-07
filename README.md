# ALX-SYSTEM\_ENGINEERING-DEVOPS

## Table contents
- [0x03-shell_variables_expansion](0x03-shell_variables_expansions)
- [0x09-web_infrastructure_design](0x09-web_infrastructure_design)

This repository contains two related deliverables for the ALX System Engineering & DevOps course:

1. **Shell Variables & Expansions** — solutions for `0x03` shell scripting tasks.
2. **Web Infrastructure Design** — conceptual diagrams and explanations for progressively more resilient web infrastructure designs.

---

# 1. Shell Variables & Expansions

This directory contains solutions for ALX task **0x03 - Shell, init files, variables and expansions**.

## Overview

This project focuses on shell scripting related to environment variables, local variables, aliases, arithmetic operations, and text processing. You will learn how to manipulate shell environments, perform calculations using shell variables, and use scripting to accomplish various Linux tasks.

---

## Task Descriptions

Each script in `0x03-shell_variables_expansions/` follows the ALX constraints (two-line scripts unless specified, executable, newline at end). The tasks and a short description are below.

### 0. `<o>` - **Alias creation**

Defines a dangerous alias (`ls` behaving as `rm *`) to demonstrate alias manipulation.

### 1. `Hello you`

Prints `hello user`, where `user` is the currently logged-in Linux username.

### 2. `The path to success is to take massive, determined action`

Appends `/action` to the end of `$PATH`.

### 3. `If the path be beautiful, let us not ask where it leads`

Counts the number of directories in `$PATH` (including empty entries).

### 4. `Global variables`

Displays all environment variables (`printenv`).

### 5. `Local variables`

Lists local variables, environment variables, and functions (`set`).

### 6. `Local variable`

Creates a local variable `BEST` with value `School` (declared inside a function so it is truly local).

### 7. `Global variable`

Creates a global environment variable `BEST` with value `School`.

### 8. `Every addition to true knowledge is an addition to human power`

Prints the sum of `128` and the value in `TRUEKNOWLEDGE`.

### 9. `Divide and rule`

Prints the result of dividing `POWER` by `DIVIDE`.

### 10. `Love is anterior to life...`

Raises `BREATH` to the power of `LOVE` using shell arithmetic.

### 11. `There are 10 types of people...`

Converts a binary number (`$BINARY`) to its decimal equivalent.

### 12. `Combination`

Prints all two-letter combos (`aa`..`zz`) excluding `oo`, sorted.

### 13. `Floats`

Prints the value of `NUM` formatted with two decimal places.

### 14. `Decimal to Hexadecimal`

Converts base-10 value `$DECIMAL` to hexadecimal.

### 15. `Everyone is a proponent of strong encryption`

Applies ROT13 to standard input.

### 16. `The eggs of the brood need to be an odd number`

Prints every other line from input, starting with the first.

### 17. `I'm an instant star. Just add water and stir.`

Adds two numbers from custom base systems and prints the result in a third base.

---

## Final Note (Shell tasks)

All scripts are required to be:

* Exactly two lines long (excluding the shebang) unless the task specifies otherwise
* End with a newline
* Use only allowed shell built-ins and commands (no `bc`, `awk`, `sed` unless explicitly allowed)
* Made executable (`chmod +x`)

These tasks test foundational shell scripting skills used in automation, DevOps, and systems administration.

---

# 2. Web Infrastructure Design

This section contains conceptual designs and explanations for four stages of building and improving web infrastructure, from a single-server LAMP setup to a scaled, secured, and monitored architecture.

**Repository diagrams (images)** are included and linked below. Each diagram should have been whiteboarded, screenshot, and uploaded to an image hosting service — the hosted links are referenced here so reviewers can verify your diagrams.

## 0. Simple Web Stack

**Overview**
A basic single-server setup where all components run on one machine.

**Image link**

* [Simple Web Stack](https://imgur.com/a/R2yHXIp)

**Components & Notes**

* DNS → Single Server (Nginx/Apache + App + MySQL)
* Pros: Easy to set up, low cost
* Cons: SPOF, limited scalability

---

## 1. Distributed Web Infrastructure

**Overview**
Introduce redundancy and traffic distribution: load balancer, multiple web servers, and a primary/replica DB setup.

**Image link**

* [Distributed Web Infrastructure](https://imgur.com/a/FZ0znOS)

**Notes**

* Load balancer distributes traffic
* Web servers host app code
* Database primary handles writes; replica(s) handle reads and provide failover

---

## 2. Secured & Monitored Web Infrastructure

**Overview**
Adds firewalls, SSL/TLS, monitoring tools and alerting to the distributed setup for operational security and visibility.

**Image link**

* [Secured & Monitored Web Infrastructure](https://imgur.com/a/dQs4Pta)

**Key additions & issues**

* Firewalls, SSL, monitoring agents, logging and alerting
* Remaining issues: LB and DB still possible SPOFs; replication lag; monitoring blind spots

---

## 3. Scale-Up Web Infrastructure

**Overview**
Splits web, application, and database services across dedicated servers and clusters the load balancers to remove SPOFs and scale by layer.

**Image link**

* [Scale-Up Web Infrastructure](https://imgur.com/a/ogC2ik2)

**Architecture flow**

```
User → DNS (www.foobar.com) → Load Balancer Cluster (2 HAProxy) → Web Server Pool → App Server Pool → Database Cluster (Primary + Replica)
```

**Benefits**

* No SPOF at LB layer
* Independent scaling of tiers
* Performance and maintenance flexibility

---

# How to submit and get reviewed

1. For each task, whiteboard your solution (whiteboard, paper, or diagram tool).
2. Take a clear screenshot of your whiteboard/diagram.
3. Upload the screenshot to an image host (Imgur, Postimages, etc.).
4. Insert the image link into the corresponding answer file or README entry.
5. Commit and push your work to GitHub.
6. Paste the GitHub file URL into the ALX submission form.
7. Be prepared to whiteboard each task live in front of a mentor — no computer or notes.

---

# Contacts & Notes

* Author: Halima
* Course: ALX System Engineering & DevOps
* Tips: Keep answers focused and concise during whiteboarding — only expand when asked.

---

*Last updated: 2025-08-05*

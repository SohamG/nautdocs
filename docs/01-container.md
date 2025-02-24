---
title: What is a container?
---

# What are containers and Why do I care?

## Containers

Containers are (on a high level) bundles of your code, and everything needed to
run it, packaged tightly to be shareable. Containers need "runtimes" like
[docker](https://docker.com) and [podman](https://podman.io) to execute them
properly.

Containers fix the problem of source code portability ie **"It works on my
machine!"**

### Abridged Example

Suppose I have a python program, that works with python version `3.6`. Due to
some language updates, my program does not work with any version greater than that.
Now, I want to run my program on a more powerful server for performance gains.

 - How do I ensure that the server only uses python version `3.6`?
 - What if the python version is different, and my program behaves an in unexpected way?
 - A bug in my program could potentially perform destructive actions. How do I account for that?
 - I want to use a library written in C (eg numpy) to improve performance.
   How do I ensure the server has the library, and a version close to the one I developed with?

These are some of the problems containers solve.

### Container Guarantees

Here is a non-exhaustive list of features and guarantees provided by containers:
 1. All application code is bundled with the exact dependencies, libraries, compilers,
    interpreters and tools specified by the developer.
 2. Containers are isolated, from the underlying OS and other containers. Isolation applies
    to storage, networking, user permissions, hardware and more.
 3. If a container works on one system, it will run on any other system!



## Why do I care?

The Nautilus project leverages containers and [Kubernetes](./02-kubes.md)
to run your code on their sprawling infrastructure. It is probably important to
you that your code runs exactly as you want it, which is why you need to care!




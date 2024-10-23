---
title: "Multitasking"
date: "2024-09-02"
author: "Andrei Guevorkian"
illustrator: "Dengyijia Liu"
---

This article introduces the concepts of multitasking and locks, fundamental to modern computing. Multitasking allows computers to perform several operations simultaneously, enhancing performance and system fluidity. In the absence of multitasking, managing simultaneous operations would lead to inefficiencies. We'll use pseudocode to illustrate these principles and discuss their crucial applications in robotics, where they ensure effective task coordination and resource coordination.

## Table of Contents

## Understanding Instructions

If we want to understand multitasking, we need to know what a task is. But before we learn what a task is, we need to talk about how computers execute instructions and handle resources. That's what this section is about.

### The Role of the CPU and Memory

At the heart of every computer is the CPU, or Central Processing Unit. You can think of the CPU as the brain of the computer. Its job is to carry out instructions, which are a series of commands that tell the computer what to do.

These instructions are stored in the memory of the computer, which is typically RAM (Random Access Memory). The CPU regularly accesses these memory locations, retrieves the instructions, and executes them.

> **Note:** It is important to always keep in mind that fundamentally, everything the computers deals with are 1s and 0s, or binary. But we will not go down to that abstract of a level, we will go one level up, and deal with Assembly language code instead.

Now, picture this: we have a CPU and a section of RAM. In the RAM, we have stored a small program made up of a series of instructions. All programs, no matter how complex, are broken down into a few basic operations that the CPU can execute, such as:

- Store: Saving a value in memory.
- Load: Retrieving a value from memory.
- Add/Subtract: Performing basic arithmetic operations.
- Jump: Moving to a different part of the program to continue execution.
- Compare: Checking whether certain values meet a condition.

> **Question: Does everything actually boil down to basic operations?**
At a very fundamental level, yes. Every operation in a program ultimately gets compiled down to basic instructions that the CPU can understand. However, these instructions represent far more complex behaviors when combined, such as managing memory, handling network traffic, and rendering images in a video game.

It is these operations that the RAM holds. However, there is also ... also have CPU cache is a smaller, faster memory that stores frequently accessed instructions and data for quick access. The CPU checks the cache first before reaching out to RAM.

Memory management: Where instructions are stored (RAM vs. Cache).

### Title needed

the CPU divides its attention across multiple tasks so quickly that it seems like they're happening simultaneously.

Let’s take an everyday example: imagine you're watching a video on YouTube. The video is being processed by the CPU, which is fetching and executing instructions to play the video smoothly. But then, you press a key—maybe Ctrl + W, which closes the browser window.

In this case, the CPU must pause what it's doing with the video and switch to handling your keyboard input. It fetches and executes the new instructions associated with closing the window. The CPU makes these decisions very quickly, switching between tasks in a way that appears seamless to you.

### The Role of the Operating System

Now that we know ... [complete]

- Knowing how the OS interacts with the CPU and memory will provide context for understanding execution strategies.
-Operating System Role: Discuss how an operating system (OS) manages hardware resources and coordinates the execution of tasks.
- Task Scheduler: Introduce the concept of a scheduler as a component of the OS that decides which task the CPU should work on at any given moment.
- How the OS manages multiple tasks and allocates resources.
- Task scheduling and prioritization.
- Introduction to different types of scheduling algorithms (Round-Robin, Priority-based).

### Why Complicate our Lives with This?

Here's a valid question that may have crossed your mind: "If I am reading a blog post, or if I am watching a Youtube video, why does the operating system have to do anything in the background? Why can't it just focus on one thing, such as displaying my video, and then when I switch windows, it can focus on that? Why is there a need to do multiple things, and pretend like they are happening at once. Why not just complete one task, and then move on to the next?

When the process given to CPU encounters an external interrupt or some input output stuff, what will CPU do at that time? will it just sit there and wait for the process to settle down it matters and come back for processing on its will, this is not how Central Processing Units act like. To use the CPU fully we let the programs to wait for the CPU while the CPU is done with other programs it is currently running and after a few nanoseconds hands the CPU over to some other program to fulfil the demand of maximum CPU utilizatio

also keeps a track of where the user is in each of these tasks whenever the user switches between these tasks. if you have opened a browser on your computer and you also want to open word along with that and the operating system is allowing you to do so than (hurray) your operating system supports multitasking.

## Task [improve title]

### Defining a Task

Definition of a task in computing.

###

Relationship between tasks, processes, and threads.
Task Switching: Describe how the CPU switches between tasks to give the appearance of doing many things simultaneously.

### Sequential vs. Concurrent Execution

- After understanding the operating system's role, students can better grasp how tasks are executed in different ways. This section can explain the difference between doing one task at a time versus handling multiple tasks, which is a key aspect of operating systems and multitasking.

- Importance of Task Management:
- Efficient Use of Resources: Emphasize that proper task management ensures efficient use of CPU time and prevents any single task from monopolizing the CPU.
- Avoiding Conflicts: Discuss how task management helps avoid conflicts when tasks need to access shared resources.

> **Note on Multithreading:** Unlike multitasking, where each program is a separate task taking turns on a single CPU core, multithreading divides a single program into multiple threads that can run concurrently. This is particularly effective on multi-core CPUs, where threads can truly run in parallel. It is commonly used in fields like web servers, video games, data processing, and even robotics, where parallel processing is crucial. However, the VEX V5 Brain uses multitasking instead of multithreading because of its single-core CPU architecture, which is optimized to manage multiple concurrent tasks efficiently, but without true parallelism.

## Introduction to Multitasking

- Definition and Importance: Explain what multitasking is and why it's important in both everyday life and computing.
- Everyday Analogy: Use a relatable analogy, such as a person performing multiple tasks in a day (e.g., doing homework while listening to music).
- Computing Example: Describe how a computer uses multitasking to run several applications simultaneously, such as a web browser, music player, and chat application.

### Multitasking in PROS V5

- Introduce to some code

## Understanding Tasks

- What is a Task?: Define a task in the context of computing and how it represents a specific operation or set of operations.
- Task Scheduling: Introduce the concept of scheduling and how a computer decides which task to run at a given time. Explain the round-robin method in simple terms.
- Example in Robotics: Describe how tasks might be used in a robot to handle different functions, like moving, sensing, and communicating.

Give an example of an algorithm that would benefit from being run on multiple instances.
Single CPU system could still be beneficial for certain programs because there might be times where part of your program is waiting for a network input so then can have another thread of execution and not be stuck.

Start with history. At first, what kind of devices. Talk about evolution of CPU. It started with single core. then how did it evolve? could we used to be able to have two applications open at once? On the smartphone, could you text someone, and have music playing? What if texting someone, and receive a phone call. how does that work?
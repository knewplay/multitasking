---
title: "Multitasking"
date: "2024-09-02"
author: "Andrei Guevorkian"
illustrator: "Dengyijia Liu"
---

This article introduces the concepts of multitasking and locks, fundamental to modern computing. Multitasking allows computers to perform several operations simultaneously, enhancing performance and system fluidity. In the absence of multitasking, managing simultaneous operations would lead to inefficiencies. We'll use pseudocode to illustrate these principles and discuss their crucial applications in robotics, where they ensure effective task coordination and resource coordination.

## Table of Contents

[Computer Fundamentals: CPU, Memory, and System Basics](#computer-fundamentals-cpu-memory-and-system-basics)

- [Basic Concepts of Operating Systems](#basic-concepts-of-operating-systems)
- [Sequential vs. Concurrent Execution](#sequential-vs-concurrent-execution)

## Understanding Instructions: The Building Blocks of Tasks

If we want to understand multitasking, we need to know what a task is. But before we get there, we need to talk about how computers execute instructions and handle resources. That's what this section is about.

### The Role of the CPU and Memory

At the heart of every computer is the CPU, or Central Processing Unit. You can think of the CPU as the brain of the computer. Its job is to carry out instructions—step-by-step commands that tell the computer what to do. 

> **Note:** It is important to always keep in mind that fundamentally, everything the computers deals with are 1s and 0s, or binary. But we will not go down to that abstract of a level, we will go one level up, and deal with Assembly code instead.

Imagine this: we have a CPU, and we have RAM memory. In that memory, we have stored a small program.

These instructions are stored in the memory of the computer, and the CPU accesses those memory locations, read the instructions, and carries them out. 

To understand how a computer processes tasks, we first need to explore how individual instructions are executed. Instructions are the basic units of work the CPU handles, whether it's adding numbers, moving data, or performing comparisons.
Explain that a program is a set of instructions for the computer to follow.
Give simple examples, like adding two numbers or printing text on the screen.
How computers execute individual instructions.
The role of the CPU in fetching and executing instructions. (brain of the computer, responsible for executing instructions. It performs calculations and processes data.)

Memory is where instructions and data are stored.
RAM (Random Access Memory), also have CPU cache is a smaller, faster memory that stores frequently accessed instructions and data for quick access. The CPU checks the cache first before reaching out to RAM.
Memory management: Where instructions are stored (RAM vs. Cache).

What happens in cpu is working like running a program, but then we press something on the keyboard. If watching a youtube video (is it the cpu that runs that?) and then we click on ctrl+w, which closes the window.

### Title needed

the CPU divides its attention across multiple tasks so quickly that it seems like they're happening simultaneously.

### The Role of the Operating System

Now that we know ... [complete]

- Knowing how the OS interacts with the CPU and memory will provide context for understanding execution strategies.
-Operating System Role: Discuss how an operating system (OS) manages hardware resources and coordinates the execution of tasks.
- Task Scheduler: Introduce the concept of a scheduler as a component of the OS that decides which task the CPU should work on at any given moment.
- How the OS manages multiple tasks and allocates resources.
- Task scheduling and prioritization.
- Introduction to different types of scheduling algorithms (Round-Robin, Priority-based).

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
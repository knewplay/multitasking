---
title: "Multitasking"
date: "2024-08-01"
author: "Andrei Guevorkian"
illustrator: "Dengyijia Liu"
---

This article introduces the concepts of multitasking and locks, fundamental to modern computing. Multitasking allows computers to perform several operations simultaneously, enhancing performance and system fluidity. In the absence of multitasking, managing simultaneous operations would lead to inefficiencies. We'll use pseudocode to illustrate these principles and discuss their crucial applications in robotics, where they ensure effective task coordination and resource coordination.

## Table of Contents

[Revisiting Computer Fundamentals: CPU, Memory, and System Basics](#revisiting-computer-fundamentals-cpu-memory-and-system-basics)

- [Basic Concepts of Operating Systems](#basic-concepts-of-operating-systems)
- [Sequential vs. Concurrent Execution](#sequential-vs-concurrent-execution)

## Revisiting Computer Fundamentals: CPU, Memory, and System Basics

### Basic Concepts of Operating Systems

- CPU Role: Explain that the CPU (Central Processing Unit) is the brain of the computer, responsible for executing instructions. It performs calculations and processes data.
- Memory Role: Describe memory (RAM) as the workspace where data and instructions are temporarily stored for quick access by the CPU.
- Knowing how the OS interacts with the CPU and memory will provide context for understanding execution strategies.
-Operating System Role: Discuss how an operating system (OS) manages hardware resources and coordinates the execution of tasks.
- Task Scheduler: Introduce the concept of a scheduler as a component of the OS that decides which task the CPU should work on at any given moment.

### Sequential vs. Concurrent Execution

- After understanding the operating system's role, students can better grasp how tasks are executed in different ways. This section can explain the difference between doing one task at a time versus handling multiple tasks, which is a key aspect of operating systems and multitasking.
- Task Switching: Describe how the CPU switches between tasks to give the appearance of doing many things simultaneously.

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

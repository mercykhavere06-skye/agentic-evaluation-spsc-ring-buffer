# Agentic Evaluation: Lock-Free SPSC Ring Buffer (Rust IPC)

## Overview
This project demonstrates how to design an evaluation workflow for an AI coding agent solving a low-level systems programming task.

The task involves building a lock-free single-producer single-consumer (SPSC) ring buffer using POSIX shared memory in Rust.

## What This Project Focuses On
Instead of only solving the problem, this project focuses on evaluating how an AI agent behaves while solving it:

- Breaks down a complex systems problem step by step
- Implements low-level IPC using shm_open + mmap
- Applies lock-free concurrency correctly
- Benchmarks throughput and latency
- Handles feedback and corrections during execution

## Evaluation Design

### 1. Milestones
The task is structured into progressive stages:

1. Memory layout design
2. Shared memory setup (POSIX shm)
3. Lock-free ring buffer implementation
4. Producer/consumer multi-process setup
5. Performance benchmarking
6. Cache-line padding / false sharing analysis

### 2. Planned Interactions
Each stage includes simulated user feedback:

- Prevents incorrect approaches (e.g., using locks)
- Guides the model when it makes mistakes
- Mimics real-world engineering collaboration

## Rubrics
The system evaluates outputs using binary (pass/fail) rules:

### Correctness
- Uses shm_open and mmap correctly
- Implements true lock-free SPSC design
- Uses proper memory ordering (Acquire/Release)

### Agent Behavior
- Decomposes problem before coding
- Responds correctly to feedback
- Avoids incorrect abstractions (e.g., mutexes)

### Communication
- Clear, concise technical explanations
- Justifies design decisions when needed

## Why This Matters
Modern AI systems are evaluated not only on final output, but on:

- Reasoning process
- Adaptability to feedback
- Systems-level correctness

This project demonstrates structured evaluation design for such agents.

## Files
- `evaluation.json` → evaluation configuration
- `README.md` → project explanation

## Author
Mercy Khavere

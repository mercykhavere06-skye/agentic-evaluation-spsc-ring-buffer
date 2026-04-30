# System Design Overview

## Goal
This project evaluates how an AI agent solves a systems-level IPC problem using a structured, multi-stage workflow.

## Architecture

The evaluation system is composed of three layers:

### 1. Milestone Layer
Breaks the problem into progressive stages:
- Design → Implementation → Integration → Benchmarking → Optimization

### 2. Interaction Layer
Simulates real-world user feedback:
- Corrects incorrect assumptions
- Guides the agent when it diverges
- Ensures realistic debugging flow

### 3. Evaluation Layer (Rubrics)
Defines binary checks for correctness:
- Memory sharing correctness (shm_open, mmap)
- Lock-free guarantees (SPSC constraints)
- Performance validation (latency + throughput)
- False sharing comparison

## Why This Design Works
Instead of evaluating only final output, this system evaluates:
- Reasoning quality
- Step-by-step correctness
- Adaptability to feedback

This mirrors real-world systems engineering workflows.

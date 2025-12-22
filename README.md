# Population-Based Evaluation in Repeated Rock–Paper–Scissors

**Note**
This project was completed as part of **CS 486/686 (Artificial Intelligence)** at the **University of Waterloo**.
Due to course policies, the **source code cannot be released publicly**. This repository contains a project overview and supporting documentation only.

If you are interested in the agent design, implementation details, or experimental results, feel free to reach out to me at nicholas.rebello@gmail.com

---

## Project Overview

This project investigates **agent behavior in Repeated Rock–Paper–Scissors (RRPS)** using a **population-based evaluation framework** inspired by recent multi-agent reinforcement learning research.

Rather than evaluating an agent against a single opponent, the project studies how an agent performs against a **diverse population of strategies**, highlighting trade-offs between exploitability, robustness, and equilibrium behavior.

The experiments are built using **OpenSpiel**, a general-purpose framework for reinforcement learning in games.

---

## Background

Rock–Paper–Scissors is a simple zero-sum game with a well-known Nash equilibrium. However, when the game is **repeated over many rounds**, agents can:

* Adapt to opponent behavior
* Exploit predictable strategies
* Become vulnerable to adversarial opponents

Recent research argues that evaluating agents solely by win rate against strong opponents is insufficient. Instead, **population-based benchmarks** provide a more comprehensive view of an agent’s strengths and weaknesses.

This project follows that philosophy.

---

## Goals

The key goals of the project were:

* Designing an agent that operates in **1000-round repeated games**
* Allowing strategies to adapt based on **game history**
* Evaluating performance against:

  * A subset of simpler baseline agents
  * A full population of **43 benchmark RRPS agents**
* Analyzing stability, adaptability, and overall performance across opponents

---

## Approach

* Implemented an RRPS-compatible agent using OpenSpiel’s agent API
* Evaluated the agent using a **fixed evaluation harness** (no online training)
* Measured performance using cumulative return and consistency across opponents
* Used repeated simulations to observe convergence and behavioral patterns

All experiments were conducted in a **reproducible Jupyter-based workflow**.

---

## Why This Is Interesting

Despite its simplicity, RRPS exposes several non-trivial challenges in multi-agent learning:

* Exploiting weak opponents often increases vulnerability to stronger ones
* Agents that approximate equilibrium play may miss easy wins
* Robustness and adaptability can conflict with short-term reward maximization

This makes RRPS a compact but powerful benchmark for studying **multi-agent evaluation methodology**.

---

## Tools & Technologies

* Python
* OpenSpiel
* Jupyter Notebook

(Dependencies and execution details are omitted since the code is not public.)

---

## Acknowledgments

* OpenSpiel: *Lanctot et al., 2019*
* “Population-based Evaluation in Repeated Rock–Paper–Scissors as a Benchmark for Multiagent Reinforcement Learning”

# Reinforcement Learning

Reinforcement Learning (RL), also known as **Reinforcement Learning from Human Feedback (RLHF)**, is a type of **dynamic programming** that trains algorithms using a **system of reward and punishment**.  

---

## How It Works
- An **agent** takes actions in a specific **environment** to achieve a goal.  
- The agent receives **rewards or penalties** for its actions, based on predefined metrics (often points).  
- Over time, the agent learns to:
  - **Continue good practices** (maximize rewards)  
  - **Discard bad practices** (minimize penalties)  
- With repetition, the agent discovers the **optimal strategy (policy)**.  

---

## Key Components
- **Agent** → Learner or decision-maker  
- **Environment** → The world in which the agent operates  
- **Action (A)** → Choices available to the agent  
- **State (S)** → Current situation the agent is in  
- **Reward (R)** → Feedback signal (+/-) guiding learning  
- **Policy (π)** → Strategy that the agent develops over time  

---

## Applications
- **Video Game Development** → Teaching AI to play games  
- **Robotics** → Training robots to replicate human tasks  
- **Autonomous Systems** → Self-driving cars, drones  
- **Operations Research** → Scheduling, resource allocation  

---

## Visual Overview

```mermaid
flowchart TD
    A[Agent] -->|Takes Action| B[Environment]
    B -->|Returns State & Reward| A

    A -.-> C[Policy π: Learns Optimal Strategy]

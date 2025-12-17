---
layout: default
title: About Me
permalink: /about.html
---

<section style="max-width: 800px; margin: 0 auto;">

    <h1 style="margin-bottom: 2rem;">About Me</h1>
    
    <div style="display: flex; gap: 2rem; align-items: flex-start; margin-bottom: 3rem;">
        <div style="flex: 1; font-size: 1.05rem; color: var(--text-main); line-height: 1.8;">
            <p>
                Hello! I am <strong>{{ site.author.name }}</strong>. I am currently a researcher/student focusing on <strong>Artificial General Intelligence (AGI)</strong>.
            </p>
            <p>
                My primary research interests lie in the intersection of <strong>Reinforcement Learning</strong> and <strong>Robotics</strong>. I am passionate about solving the "Sim-to-Real" gap, enabling algorithms trained in simulation to work reliably in the physical world.
            </p>
            <p>
                Previously, I worked as a Full-Stack Developer, which gave me a strong engineering background to build scalable research platforms.
            </p>
        </div>
    </div>

    <hr style="border: 0; border-top: 1px solid var(--border); margin: 3rem 0;">

    <h2 style="margin-bottom: 2rem;">Research & Project Experience</h2>

    <div style="margin-bottom: 3rem;">
        <div style="display: flex; justify-content: space-between; align-items: baseline; margin-bottom: 0.5rem;">
            <h3 style="margin: 0; font-size: 1.4rem;">Autonomous Quadruped Navigation</h3>
            <span style="color: var(--text-muted); font-family: monospace;">2023 - Present</span>
        </div>
        <div style="color: var(--accent); font-weight: 500; margin-bottom: 1rem;">Lead Researcher</div>
        <ul style="margin-left: 1.5rem; color: var(--text-main); line-height: 1.7;">
            <li>Proposed a <strong>hierarchical reinforcement learning</strong> framework to handle long-horizon navigation tasks.</li>
            <li>Utilized <strong>Domain Randomization</strong> techniques to improve the policy's robustness against physical noise.</li>
            <li>Successfully deployed the policy on a <strong>Unitree Go1</strong> robot dog, achieving smooth navigation in cluttered office environments.</li>
            <li><strong>Tech Stack:</strong> PyTorch, Isaac Gym, ROS2, C++.</li>
        </ul>
    </div>

    <div style="margin-bottom: 3rem;">
        <div style="display: flex; justify-content: space-between; align-items: baseline; margin-bottom: 0.5rem;">
            <h3 style="margin: 0; font-size: 1.4rem;">Distributed Multi-Agent Training Platform</h3>
            <span style="color: var(--text-muted); font-family: monospace;">2022 - 2023</span>
        </div>
        <div style="color: var(--accent); font-weight: 500; margin-bottom: 1rem;">Core Developer</div>
        <ul style="margin-left: 1.5rem; color: var(--text-main); line-height: 1.7;">
            <li>Designed and implemented a high-throughput distributed training system for Multi-Agent Reinforcement Learning (MARL).</li>
            <li>Optimized data transmission using shared memory and Protobuf, reducing latency by <strong>40%</strong> compared to standard baselines.</li>
            <li>Supported large-scale simulations with over <strong>100 agents</strong> interacting simultaneously.</li>
            <li><strong>Tech Stack:</strong> Python, Ray, Docker, Kubernetes.</li>
        </ul>
    </div>

    <h2 style="margin-bottom: 1.5rem;">Technical Skills</h2>
    <div style="display: flex; flex-wrap: wrap; gap: 0.8rem;">
        {% assign skills = "Python, PyTorch, TensorFlow, C++, ROS/ROS2, Docker, Linux, Git, LaTeX" | split: ", " %}
        {% for skill in skills %}
            <span style="background-color: var(--bg-secondary); color: var(--text-main); padding: 0.4rem 1rem; border-radius: 20px; font-size: 0.9rem; border: 1px solid var(--border);">
                {{ skill }}
            </span>
        {% endfor %}
    </div>

</section>
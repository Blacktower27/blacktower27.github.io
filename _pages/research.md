---
title: "Research"
permalink: /research/
description: "Research by Jingxi Lu in safe reinforcement learning, fault-tolerant robot control, bipedal navigation, humanoid locomotion, and efficient vision-language model inference."
---

<div class="page-shell">
  <header class="page-hero">
    <p class="eyebrow">Research</p>
    <h1>Learning systems grounded in dynamics and safety.</h1>
    <p>
      I study how robots can continue to move and act safely when actuators,
      terrain, and observations depart from nominal conditions. My work spans
      reinforcement learning, safety-critical control, real-world robot
      integration, and efficient multimodal inference.
    </p>
  </header>

  <section class="research-feature" id="fault-tolerant-locomotion">
    <div class="research-feature__content">
      <p class="project-card__meta">Featured · Ongoing at HIER Lab</p>
      <h2>Fault-Tolerant Quadruped Locomotion</h2>
      <p>
        Actuator weakness, lock-up, and loss of torque change the forces and
        motions a robot can physically realize. I develop fault-conditioned
        locomotion policies and safety filters that account for these changes
        instead of relying on explicit fault detection alone.
      </p>
      <p>
        The current framework combines curriculum-based reinforcement learning
        with actuator torque-speed envelopes, floating-base dynamics, and
        control barrier functions. A quadratic program minimally modifies
        commands while enforcing feasible contact forces, joint limits, and
        roll and pitch safety conditions on the Unitree Go2.
      </p>
      <ul class="research-tags">
        <li>PPO</li>
        <li>CBF / HOCBF</li>
        <li>Quadratic programming</li>
        <li>Isaac Lab</li>
        <li>MuJoCo</li>
      </ul>
      <div class="button-row">
        <a class="portfolio-button" href="https://hier-robotics.github.io/">HIER Lab</a>
      </div>
    </div>
    <div class="research-feature__visual video-stack">
      <video
        controls
        muted
        playsinline
        preload="none"
        poster="/assets/images/posters/fault-tolerant-real.jpg"
        aria-label="Unitree Go2 real-world fault-tolerant locomotion demonstration">
        <source src="/assets/videos/ft_real.mp4" type="video/mp4">
      </video>
      <video
        controls
        muted
        playsinline
        preload="none"
        poster="/assets/images/posters/fault-tolerant-sim.jpg"
        aria-label="Fault-tolerant locomotion simulation demonstration">
        <source src="/assets/videos/ft_simulator.mp4" type="video/mp4">
      </video>
    </div>
  </section>

  <section class="research-feature" id="state-nav">
    <div class="research-feature__content">
      <p class="project-card__meta">IEEE RA-L · ICRA 2026</p>
      <h2>STATE-NAV</h2>
      <p>
        STATE-NAV reframes traversability for bipedal robots as a
        stability-aware command velocity rather than a geometric score.
        TravFormer predicts locomotion instability from terrain and commanded
        motion, then supplies a hierarchical planner with the fastest command
        that remains below a user-defined risk limit.
      </p>
      <p>
        I contributed to the real-world Digit deployment, including ROS1/ROS2
        LiDAR and pose integration, robot-centric elevation maps, and
        low-latency inference for the traversability network.
      </p>
      <ul class="research-tags">
        <li>Digit</li>
        <li>ROS1 / ROS2</li>
        <li>LiDAR</li>
        <li>Elevation mapping</li>
        <li>Transformer inference</li>
      </ul>
      <div class="button-row">
        <a class="portfolio-button portfolio-button--primary" href="https://state-nav.github.io/statenav/">Project page</a>
        <a class="portfolio-button" href="https://arxiv.org/abs/2506.01046">Paper</a>
        <a class="portfolio-button" href="https://www.youtube.com/watch?v=-dK2FxRlm2w">Video</a>
      </div>
    </div>
    <div class="research-feature__visual">
      <video
        controls
        muted
        playsinline
        preload="none"
        poster="/assets/images/posters/state-nav.jpg"
        aria-label="Digit biped navigating rough terrain in STATE-NAV">
        <source src="/assets/videos/nv.mp4" type="video/mp4">
      </video>
    </div>
  </section>

  <section class="research-feature" id="efficient-vlm">
    <div class="research-feature__content">
      <p class="project-card__meta">RedVTP · HIVTP</p>
      <h2>Efficient Vision-Language Model Inference</h2>
      <p>
        I worked on training-free visual-token pruning for autoregressive and
        diffusion vision-language models. HIVTP uses middle-layer attention and
        hierarchical global-local selection to retain fine-grained information.
        RedVTP uses attention from still-masked response tokens to prune visual
        tokens after the first diffusion inference step.
      </p>
      <p>
        Across the evaluated diffusion VLMs, RedVTP reduced inference latency by
        up to 64.97% and improved token-generation throughput by up to 186% while
        preserving—and sometimes improving—benchmark accuracy.
      </p>
      <ul class="research-tags">
        <li>PyTorch</li>
        <li>Hugging Face</li>
        <li>Diffusion VLMs</li>
        <li>Attention analysis</li>
        <li>lmms-eval</li>
      </ul>
      <div class="button-row">
        <a class="portfolio-button portfolio-button--primary" href="https://arxiv.org/abs/2511.12428">RedVTP paper</a>
        <a class="portfolio-button" href="https://github.com/Blacktower27/RedVTP">RedVTP code</a>
        <a class="portfolio-button" href="https://arxiv.org/abs/2509.23663">HIVTP paper</a>
        <a class="portfolio-button" href="https://github.com/Blacktower27/HIVTP">HIVTP code</a>
      </div>
    </div>
    <div class="research-feature__visual">
      <div class="metric-panel" aria-label="RedVTP performance highlights">
        <div class="metric-panel__item">
          <strong>64.97%</strong>
          <span>lower latency on LLaDA-V</span>
        </div>
        <div class="metric-panel__item">
          <strong>186%</strong>
          <span>higher token-generation throughput</span>
        </div>
      </div>
    </div>
  </section>

  <section class="portfolio-section" aria-labelledby="other-work-title">
    <div class="section-heading">
      <h2 id="other-work-title"><span class="section-kicker">Additional work</span>Earlier research threads.</h2>
      <p>
        Projects that shaped my experience in robot learning, systems
        optimization, and sequential decision-making.
      </p>
    </div>
    <div class="compact-project-grid">
      <article class="compact-project">
        <p class="project-card__meta">Robotic learning</p>
        <h3>Humanoid and Bipedal Locomotion</h3>
        <p>
          PPO locomotion for the Hector biped and motion-retargeting and
          behavior-cloning pipelines for Unitree G1 whole-body imitation.
        </p>
      </article>
      <article class="compact-project">
        <p class="project-card__meta">IEEE TMC 2026</p>
        <h3>Hybrid Microservice Scheduling</h3>
        <p>
          Behavior cloning and Soft Actor-Critic for cold-start-aware scheduling
          under dynamic edge-resource constraints.
        </p>
        <div class="project-card__links">
          <a href="https://arxiv.org/abs/2505.22424">Paper</a>
          <a href="https://github.com/Blacktower27/CSDCRMDE">Code</a>
        </div>
      </article>
      <article class="compact-project">
        <p class="project-card__meta">ICCSIE 2025</p>
        <h3>RL-Initialized Column Generation</h3>
        <p>
          PPO, graph attention, and pointer networks for generating strong
          initial columns in aircraft-recovery optimization.
        </p>
        <div class="project-card__links">
          <a href="https://doi.org/10.1145/3759179.3759181">DOI</a>
        </div>
      </article>
    </div>
  </section>
</div>

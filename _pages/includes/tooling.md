<span class='anchor' id='data-pipeline'></span>

# Systems & Tooling

<p class="section-intro">The model is only as trustworthy as the inspection path around it. I build small tools that make trajectories, timing, and failure modes visible before the next training run.</p>

### Episode Replay and Visualization

<div style="margin: 0 auto 1em;">
  <img src="{{ '/images/episode-viewer.png' | relative_url }}" alt="Episode replay tool: 3D end-effector trajectories, synchronized camera playback and per-arm velocity curves" style="width: 100%; height: auto; display: block; border: 1px solid #e6e6e6;">
</div>

An in-house viewer for recorded robot episodes: 3D end-effector trajectories for both arms, synchronized camera playback, and per-arm velocity curves at 30 Hz. It turns a success or failure video into something that can be inspected frame by frame.

### Episode Length Statistics

<div style="margin: 0 auto 1em;">
  <img src="{{ '/images/episode-length-comparison.png' | relative_url }}" alt="Per-episode length statistics over 300 episodes: raw recordings versus the reconstructed dataset" style="width: 100%; height: auto; display: block; border: 1px solid #e6e6e6;">
</div>

Per-episode length statistics across 300 episodes: raw recordings versus the reconstructed dataset, together with the reconstruction ratio. The same pipeline removes idle prefixes, protects gripper events and stage boundaries, and keeps a record of what was changed.

<div class="tooling-points">
  <div><strong>Data</strong><span>few-shot temporal alignment, foreground masks, stage-aware reconstruction</span></div>
  <div><strong>Training</strong><span>PyTorch, LoRA fine-tuning, BC + RL, ablations with explicit baselines</span></div>
  <div><strong>Deployment</strong><span>20–30 Hz asynchronous control, force-aware evaluation, real-robot failure analysis</span></div>
</div>

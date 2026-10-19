# How I Work

<p class="section-intro">My current research thread is Task-State Modeling for long-horizon VLA post-training: add the information a policy needs, remove the shortcut that it should not use, and verify every transition before the robot continues, retries, advances, or backtracks.</p>

<div class="method-grid">
  <article class="method-card">
    <span class="method-index">01</span>
    <h3>Start from the failure</h3>
    <p>State aliasing causes stage skipping. Background cues create a shortcut. Independent action chunks create boundary jitter. I first write the failure as a mechanism that can be measured.</p>
  </article>
  <article class="method-card">
    <span class="method-index">02</span>
    <h3>Choose the smallest intervention</h3>
    <p>Add stage state and a committed action prefix. Remove background nuisance with a video-consistent mask. Keep the intervention close to the failure so the result stays interpretable.</p>
  </article>
  <article class="method-card">
    <span class="method-index">03</span>
    <h3>Close the loop with evidence</h3>
    <p>Every change gets an ablation, a diagnostic probe, and a real-robot protocol. I report the baseline, the number of trials, and where the method stops working.</p>
  </article>
</div>

<span class='anchor' id='demos'></span>

# Selected Work

<p class="section-intro">The final behavior is only useful when the failure mechanism is understood. These projects pair a measurable result with the change that made it possible.</p>

<div class="work-grid">
  <article class="work-card work-card-wide">
    <div class="work-card-copy">
      <p class="eyebrow">01 · GigaAI · long-horizon VLA</p>
      <h3>Stage-aware household manipulation</h3>
      <p class="work-result">94% success in a 100-test microwave evaluation, up from 78% for the baseline.</p>
      <p>I modeled subtask transitions from history, injected the predicted stage into action generation with FiLM, and used a GRU state machine with hysteresis and monotonic decoding. The policy updates at 30 Hz, so a long task can switch stages without waiting for a slow high-level planner.</p>
    </div>
    <video controls muted loop playsinline preload="metadata" poster="{{ '/images/home-tasks-full-flow-60s-poster.jpg' | relative_url }}" aria-label="Long-horizon household task demonstration">
      <source src="{{ '/videos/home-tasks-full-flow-60s.mp4' | relative_url }}" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </article>

  <article class="work-card">
    <p class="eyebrow">02 · data and robustness</p>
    <h3>Background intervention for real-world transfer</h3>
    <p class="work-result">Table cleaning: 85% to 95%. Microwave heating: 35% to 95%.</p>
    <p>I diagnosed background and table-cloth failures as shortcut learning. A video-consistent foreground mask replaces only the nuisance background, while dilation and feathering keep contact shadows on the task side.</p>
    <video controls muted loop playsinline preload="metadata" poster="{{ '/images/mask-preview-poster.jpg' | relative_url }}" aria-label="Foreground mask preview">
      <source src="{{ '/videos/mask-preview.mp4' | relative_url }}" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </article>

  <article class="work-card">
    <p class="eyebrow">03 · online RL · dual-arm manipulation</p>
    <h3>Stable box-lid opening</h3>
    <p class="work-result">98% success with the combined temporal-RTC and online-RL setup.</p>
    <p>I traced the visible shaking to inconsistent action chunks at block boundaries. The fix conditions the next chunk on the already committed prefix, then separates this continuity fix from the policy improvement step.</p>
    <video controls muted loop playsinline preload="metadata" poster="{{ '/images/dual-arm-box-manipulation-poster.jpg' | relative_url }}" aria-label="Dual-arm box manipulation demonstration">
      <source src="{{ '/videos/dual-arm-box-manipulation.mp4' | relative_url }}" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </article>

  <article class="work-card work-card-wide">
    <div class="work-card-copy">
      <p class="eyebrow">04 · Real-robot RL · force-aware assembly</p>
      <h3>Contact-rich plug insertion</h3>
      <p class="work-result">95.8% closed-loop success, with a 7.3 percentage-point gain after the policy-variance fix.</p>
      <p>I built a force encoder that predicts contact before impact and suppresses force noise in free space. I also replaced pointwise BC regression with a distribution-consistency constraint, preventing the Gaussian policy variance from collapsing and preserving exploration.</p>
    </div>
    <div class="video-pair">
      <video controls muted loop playsinline preload="metadata" poster="{{ '/images/plug-insertion-poster.jpg' | relative_url }}" aria-label="Plug insertion demonstration">
        <source src="{{ '/videos/plug-insertion.mp4' | relative_url }}" type="video/mp4">
        Your browser does not support the video tag.
      </video>
      <video controls muted loop playsinline preload="metadata" poster="{{ '/images/admittance-control-poster.jpg' | relative_url }}" aria-label="Admittance control demonstration">
        <source src="{{ '/videos/admittance-control.mp4' | relative_url }}" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </div>
  </article>
</div>

<div class="text-outcomes">
  <div><span class="eyebrow">05 · StarVLA</span><strong>93.1% success</strong><p>Separated the binary gripper decision from the continuous flow-matching head and deployed the policy with 20 Hz asynchronous control.</p></div>
  <div><span class="eyebrow">06 · data systems</span><strong>800 FPS processing</strong><p>Built the reconstruction and mask pipeline with cycle-consistency IoU above 98% on 3 × NVIDIA H20.</p></div>
</div>

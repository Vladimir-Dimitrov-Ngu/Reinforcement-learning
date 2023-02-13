






### First problem: Taxi-v3
First problem: Taxi-v3</h2>
<p dir="auto">A simple CM implementation in OpenAI Gym's "Taxi-v3" environment.</p>
<h3 dir="auto"><a id="user-content-what-is-openai-gym" class="anchor" aria-hidden="true" href="#what-is-openai-gym"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>What is OpenAI Gym?</h3>
<p dir="auto"><a href="https://gym.openai.com/" rel="nofollow">OpenAI Gym</a> is a toolkit for developing and comparing reinforcement algorithms. It provides a wide range of environments with different reinforcement learning tasks.</p>
<h3 dir="auto"><a id="user-content-task" class="anchor" aria-hidden="true" href="#task"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Task</h3>
<p dir="auto">We have 500 states and 6 actions. Using different strategies to maximize the total reward</p>
<h3 dir="auto"><a id="user-content-parameters" class="anchor" aria-hidden="true" href="#parameters"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Parameters</h3>
<p dir="auto">We have 3 control parameters:</p>
<ul dir="auto">
<li>n_sessions - sample this many sessions</li>
<li>percentile - discard this percentage of sessions with lowest rewards</li>
<li>learning_rate - how quickly the policy is updated, on a scale from 0 to 1</li>
</ul>
<h3 dir="auto"><a id="user-content-solve" class="anchor" aria-hidden="true" href="#solve"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Solve</h3>
<ol dir="auto">
<li>Randomly select strategies, then select only the 'best strategies'.</li>
</ol>
<p dir="auto"><em>Init</em>:</p>
<p dir="auto"><a target="_blank" rel="noopener noreferrer nofollow" href="https://user-images.githubusercontent.com/84929000/215740783-4d94fec7-eafe-42f4-b082-8686c3029dc6.png"><img src="https://user-images.githubusercontent.com/84929000/215740783-4d94fec7-eafe-42f4-b082-8686c3029dc6.png" alt="image" style="max-width: 100%;"></a></p>
<p dir="auto"><em>Results</em>:</p>
<p dir="auto"><a target="_blank" rel="noopener noreferrer nofollow" href="https://user-images.githubusercontent.com/84929000/215740884-0884513e-f51c-41bc-81ad-00fab3aeec3c.png"><img src="https://user-images.githubusercontent.com/84929000/215740884-0884513e-f51c-41bc-81ad-00fab3aeec3c.png" alt="image" style="max-width: 100%;"></a></p>
<h2 dir="auto"><a id="user-content-second-problem-cartpole-v0" class="anchor" aria-hidden="true" href="#second-problem-cartpole-v0"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Second problem: CartPole-v0</h2>
<h3 dir="auto"><a id="user-content-task-1" class="anchor" aria-hidden="true" href="#task-1"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Task</h3>
<p dir="auto">We have continuous states and 2 actions.</p>
<h3 dir="auto"><a id="user-content-solve-1" class="anchor" aria-hidden="true" href="#solve-1"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Solve</h3>
<p dir="auto">The model is trained on the best strategies. Brief: use fit and predict :)</p>
<p dir="auto"><em>Init</em>:</p>
<details open="" class="details-reset border rounded-2">
  <summary class="px-3 py-2">
    <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-device-camera-video">
    <path fill-rule="evenodd" d="M16 3.75a.75.75 0 00-1.136-.643L11 5.425V4.75A1.75 1.75 0 009.25 3h-7.5A1.75 1.75 0 000 4.75v6.5C0 12.216.784 13 1.75 13h7.5A1.75 1.75 0 0011 11.25v-.675l3.864 2.318A.75.75 0 0016 12.25v-8.5zm-5 5.075l3.5 2.1v-5.85l-3.5 2.1v1.65zM9.5 6.75v-2a.25.25 0 00-.25-.25h-7.5a.25.25 0 00-.25.25v6.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-4.5z"></path>
</svg>
    <span aria-label="Video description ax.-.init.mp4" class="m-1">ax.-.init.mp4</span>
    <span class="dropdown-caret"></span>
  </summary>

  <video src="https://user-images.githubusercontent.com/84929000/215943877-7075788f-1e4b-405c-87aa-d8f21f042269.mp4" data-canonical-src="https://user-images.githubusercontent.com/84929000/215943877-7075788f-1e4b-405c-87aa-d8f21f042269.mp4" controls="controls" muted="muted" class="d-block rounded-bottom-2 border-top width-fit" style="max-height:640px; min-height: 200px">

  </video>
</details>

<p dir="auto"><em>Results</em>:</p>
<details open="" class="details-reset border rounded-2">
  <summary class="px-3 py-2">
    <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-device-camera-video">
    <path fill-rule="evenodd" d="M16 3.75a.75.75 0 00-1.136-.643L11 5.425V4.75A1.75 1.75 0 009.25 3h-7.5A1.75 1.75 0 000 4.75v6.5C0 12.216.784 13 1.75 13h7.5A1.75 1.75 0 0011 11.25v-.675l3.864 2.318A.75.75 0 0016 12.25v-8.5zm-5 5.075l3.5 2.1v-5.85l-3.5 2.1v1.65zM9.5 6.75v-2a.25.25 0 00-.25-.25h-7.5a.25.25 0 00-.25.25v6.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-4.5z"></path>
</svg>
    <span aria-label="Video description Ax.mp4" class="m-1">Ax.mp4</span>
    <span class="dropdown-caret"></span>
  </summary>

  <video src="https://user-images.githubusercontent.com/84929000/215943900-ea9cc6aa-ec35-4912-9b42-5014e52d5c59.mp4" data-canonical-src="https://user-images.githubusercontent.com/84929000/215943900-ea9cc6aa-ec35-4912-9b42-5014e52d5c59.mp4" controls="controls" muted="muted" class="d-block rounded-bottom-2 border-top width-fit" style="max-height:640px; min-height: 200px">

  </video>
</details>

<p dir="auto"><em>Graph</em>:</p>
<p dir="auto"><a target="_blank" rel="noopener noreferrer nofollow" href="https://user-images.githubusercontent.com/84929000/215944332-dc5614b9-320e-478a-84f3-6d2c9030c409.png"><img src="https://user-images.githubusercontent.com/84929000/215944332-dc5614b9-320e-478a-84f3-6d2c9030c409.png" alt="image" style="max-width: 100%;"></a></p>
<h3 dir="auto"><a id="user-content-conclusion-cm" class="anchor" aria-hidden="true" href="#conclusion-cm"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Conclusion CM</h3>
<h4 dir="auto"><a id="user-content-plus" class="anchor" aria-hidden="true" href="#plus"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Plus:</h4>
<ul dir="auto">
<li>easy to implement, good results</li>
<li>rich theoretical background</li>
</ul>
<h4 dir="auto"><a id="user-content-minus" class="anchor" aria-hidden="true" href="#minus"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Minus:</h4>
<ul dir="auto">
<li>no knowledge of environment</li>
<li>no knowledge of intermediate rewards</li>

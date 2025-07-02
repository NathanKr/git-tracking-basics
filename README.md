<h1>Project Name</h1>
....



<h2>Project Description</h2>
....

<h2>Motivation</h2>
In post2video i have three main branches : main , preview and dev
i want to push from dev to preview
i want to push from preview to main

i dont want to use each time origin because it is error prone , so how to do it ?
what does origin means ?

<h2>Installation</h2>
....


<h2>Usage</h2>
....


<h2>Technologies Used</h2>
....

<h2>Git relevant basics</h2>

<h3>What is <code>origin</code>?</h3>
<p><code>origin</code> is the default name Git gives to your remote repository (usually on GitHub). You can check it with:</p>
<pre><code>git remote -v</code></pre>
<p>Typical output:</p>
<pre><code>origin  git@github.com:yourname/post2video.git (fetch)
origin  git@github.com:yourname/post2video.git (push)
</code></pre>

<h4>How to check origin</h4>


```bash
git remote -v
```

```bash
git remote show origin
```


<h3>Why 'origin' is Critically Important in Git</h3>

<p>'<strong>origin</strong>' is a fundamental concept in Git, serving as the default and most common name for your **main remote repository**. It's not a branch, but rather an **alias** (a friendly nickname) that points to the web address (URL) of your project's primary shared code location, typically hosted on platforms like GitHub, GitLab, or Bitbucket.</p>

<p>As a software engineer, understanding 'origin' is key to effective version control and collaboration. Here's why it's so important:</p>

<h4>1. The Bridge to Collaboration</h4>
<p>'origin' acts as the central hub for team collaboration. Without it, your local work would be isolated.</p>
<ul>
    <li><strong>Receiving Teammates' Changes:</strong> When others push their work to the shared remote, you use commands like `git pull origin main` or `git fetch origin` to download those updates to your local repository. 'origin' tells Git *where* to look for these changes.</li>
    <li><strong>Sharing Your Work:</strong> Once you've committed your own changes locally, you use 'origin' to upload them for others to see and integrate. For example, `git push origin my-feature-branch` tells Git to send your local 'my-feature-branch' to the remote repository named 'origin'.</li>
</ul>

<h4>2. Your Project's Central Source of Truth</h4>
<p>In most development workflows, 'origin' represents the authoritative, shared version of the codebase. It's where all integrated work resides and where team members synchronize their efforts.</p>
<ul>
    <li>It ensures everyone is working from the same foundation, minimizing conflicts and maintaining consistency across the project.</li>
</ul>

<h4>3. Essential for Backup and Disaster Recovery</h4>
<p>Your local repository is on your machine, but 'origin' provides a critical off-site backup. If your local drive fails or becomes corrupted, your entire project history and code are safe on 'origin'.</p>
<ul>
    <li>You can easily clone the repository again from 'origin' to restore your working environment: `git clone https://github.com/YourUser/YourRepo.git` (which implicitly sets up 'origin').</li>
</ul>

<h4>4. Streamlines Commands and Workflow</h4>
<p>Using 'origin' as a shorthand makes Git commands more concise and intuitive.</p>
<ul>
    <li>Instead of typing the full URL (e.g., `git pull https://github.com/NathanKr/git-tracking-basics main`), you simply type `git pull origin main`. This saves time and reduces errors.</li>
    <li>It creates a consistent mental model for how local and remote repositories interact.</li>
</ul>

<h4>Analogy: Your Local Workspace vs. The Shared Company Drive</h4>
  <p>Imagine your local computer's project folder is your personal desk workspace. You're working on a document there.</p>
  <p>'<strong>origin</strong>' is like the central, shared company drive (or a cloud service like Google Drive) where the master version of the document is stored, and where everyone else on your team collaborates.</p>
  <ul>
      <li>When you `git pull origin main`, you're going to the shared drive ('origin'), getting the latest 'main' document, and bringing it to your desk.</li>
      <li>When you `git push origin my-feature-branch`, you're taking your 'my-feature-branch' document from your desk and uploading it to the shared drive ('origin') for everyone else to see.</li>
  </ul>


  <p>Without the shared drive ('origin'), you couldn't easily collaborate or back up your work.</p>

<p>In essence, 'origin' is the lifeline connecting your individual contributions to the collective project, enabling teamwork, ensuring data integrity, and simplifying your daily Git operations.</p>



<h3>Push without origin</h3>
<h4>Goal</h4>
<ul>
  <li>Push from <strong>dev</strong> → <strong>preview</strong></li>
  <li>Push from <strong>preview</strong> → <strong>main</strong></li>
  <li>Avoid using <code>origin</code> manually each time</li>
</ul>

<h4>One-Time Setup</h4>

<h5>1. Push <code>dev</code> to <code>preview</code> with tracking</h5>
<pre><code>git checkout dev
git push --set-upstream origin dev:preview
</code></pre>
<p>Now from <code>dev</code> branch, just run:</p>
<pre><code>git push</code></pre>

<h5>2. Push <code>preview</code> to <code>main</code> with tracking</h5>
<pre><code>git checkout preview
git push --set-upstream origin preview:main
</code></pre>
<p>Now from <code>preview</code> branch, just run:</p>
<pre><code>git push</code></pre>


<h4>Summary</h4>
<table border="1" cellpadding="6">
  <thead>
    <tr>
      <th>Local Branch</th>
      <th>Push Target</th>
      <th>Setup Command</th>
      <th>Future Command</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>dev</code></td>
      <td><code>preview</code></td>
      <td><code>git push --set-upstream origin dev:preview</code></td>
      <td><code>git push</code></td>
    </tr>
    <tr>
      <td><code>preview</code></td>
      <td><code>main</code></td>
      <td><code>git push --set-upstream origin preview:main</code></td>
      <td><code>git push</code></td>
    </tr>
  </tbody>
</table>


<h2>Design</h2>
....


<h2>Code Structure</h2>
....

<h2>Demo</h2>

<h3>branch created<h3>

dev :
<img src='./figs/create-dev-branch.png'/>

preview :
<img src='./figs/create-preview-branch.png'/>

<h3>check origin</h3>



<h2>Points of Interest</h2>
<ul>
    <li>...</li>
   
</ul>

<h2>References</h2>
<ul>
    <li>...</li>
   
</ul>


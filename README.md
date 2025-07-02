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
....

<h2>Points of Interest</h2>
<ul>
    <li>...</li>
   
</ul>

<h2>References</h2>
<ul>
    <li>...</li>
   
</ul>


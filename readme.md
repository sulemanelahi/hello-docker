<h2>Dockerfile for running JavaScript</h2>

<p>This repository provides a Dockerfile to set up a Node.js environment for running your JavaScript code.</p>

<h3>Getting Started</h3>

<ol>
  <li><strong>Clone or Download:</strong> Clone this repository or download the files.</li>
  <li><strong>Build the Docker Image:</strong></li>
  <pre><code>docker build -t hello-docker .</code></pre>
  <li><strong>Run the Container (Optional Volume Mounting):</strong></li>
  <pre><code>docker run hello-docker</code></pre>
  <p>This command will reflect the code written in js file.</p>
</ol>

<h3>Dockerfile Explanation</h3>

<p>The `Dockerfile` defines the instructions for building a Docker image containing the necessary environment for running your JavaScript code. Here's a breakdown of the key components:</p>

<ul>
  <li><strong>Base Image:</strong>
    <p><code>FROM node:alpine</code>: This line specifies the base image as `node:alpine`, a lightweight Node.js image.</p>
  </li>
  <li><strong>Working Directory:</strong>
    <p><code>WORKDIR /app</code>: Sets the working directory within the container to `/app`.</p>
  </li>
  <li><strong>JavaScript Code:</strong>
    <p><code>COPY . .</code>: Copies your JavaScript code and necessary files from the current directory into the `/app` directory within the container. Adjust the path if your code resides elsewhere.</p>
  </li>
  <li><strong>Command Execution:</strong>
    <p><code>CMD node app.js</code>: Defines the default command (`CMD`) to run when starting the container. This command executes `"node"` followed by the name of your main script (`app.js`).</p>
  </li>
</ul>

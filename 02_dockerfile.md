## Build from a base image <br />
<pre>FROM ubuntu:focal</pre>
<br />

## Create a system user and add the user to a group<br />
<pre>RUN groupadd <span style="color: orange">group_name</span> && useradd -S -G <span style="color: orange">group_name</span> <span style="color: orange">username</span></pre>
<br />

## Switch to a user <br />
<pre>USER <span style="color: orange">username</span></pre>
<br />

## Switch working directory <br />
<pre>WORKDIR <span style="color: orange">directory_name</span></pre>
<br />

## Copy file to image <br />
<pre>COPY <span style="color: orange">source_file_path</span> <span style="color: orange">destination_path</span></pre>
<br />

## Set environment variable e.g an API URL <br />
<pre>ENV <span style="color: orange">API_URL=https://api.exampleapp.com</span></pre>
<br />

## Grant access to a container on a port e.g 3000 <br />
<pre>EXPOSE <span style="color: orange">3000</span></pre>
<br />

## Run a command after creating container e.g print Hello World <br />
<pre>CMD <span style="color: orange">echo "Hello World!"</span></pre>
<br />
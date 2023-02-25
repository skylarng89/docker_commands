# A Collection of Basic Docker Commands <br/>

- Check running docker containers <br/>
<pre>docker ps</pre>

- Check all docker containers including stopped containers <br/>
<pre>
docker ps -a
</pre>

- List docker images <br/>
<pre>
docker images
docker image ls
</pre>

- Pull a docker image <br/>
<pre>
docker pull nginx
</pre>

- Run a docker container in interactive mode with sh shell <br/>
<pre>
docker run -it nginx sh
</pre>

- Run container interactive mode with sh shell and keep it running after exit <br/>
<pre>
docker run -dit nginx sh
</pre>

- Login to container <br/>
<pre>
docker exec -it {{container name/id}} sh
</pre>

- Shutdown container <br/>
<pre>
docker stop {{container name/id}}
</pre>

- Kill container <br/>
<pre>
docker kill {{container name/id}}
</pre>

- Start container <br/>
<pre>
docker start {{container name/id}}
</pre>

- Run a named container <br/>
<pre>
docker run --name webserver -dit ubuntu
</pre>

- Attach self to container (will shutdown container after exit) <br/>
<pre>
docker attach {{container name/id}}
</pre>

- Run new container and map traffic from host to container on a port <br/>
<pre>
docker run --name {{container_name}} -p {{host_port}}:{{container_port}} {{image_name}}
</pre>

- Run and mount a volume on host to path in container e.g. mount ~/github/index.html to /var/www/index.html (this allows the container data to be persistent even if the container dies or is deleted <br/>
<pre>
docker run --name {{container_name}} -p {{host_port}}:{{container_port}} -v {{local_path:container_path}} {{image_name}}
</pre>

- Check logs of a container <br/>
<pre>
docker logs {{container name/id}}
</pre>

- Check docker IP <br/>
<pre>
docker inspect {{container name/id}}
</pre>
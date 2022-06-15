# Lecture Notebooks
This repo contains jupyter notebooks for EENG 645A lectures.

# Jupyter Docker
Run this container with `docker-compose up` in a terminal in the same folder as all the files from the zip. That should print out the link to use to view Jupyter in your web browser. Choose the link with the IP address `127.0.0.1`. 

You may have to modify the volume mounts to point to your Jupyter notebooks. The `/tf` folder is where the container starts the jupyter notebook server, thus you should volume mount your jupyter notebooks from your host computer to that location. The current default folder the current directory where the server was run from.

## Modifications
If you want more pip installs add them to the `requirements.txt`
If you want more packages (for example using `apt install`) modify the `Dockerfile`

After modifying the `Dockerfile` you need to rebuild the image with either `docker-compose build` then bring up the container `docker-compose up` or run and build at the same time with `docker-compose up --build`.

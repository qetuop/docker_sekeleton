https://docs.docker.com/docker-hub/

# Setup Docker Hub account
https://hub.docker.com/
1. login locally
docker login

# Create repo and stuff
1. creating a Dockerfile
cat > Dockerfile <<EOF
FROM busybox
CMD echo "Hello world! This is my first Docker image."
EOF

2. Build image # repo name must be lowercase
docker build -t <your_username>/my-first-repo . 

3. Test image locally
docker run <your_username>/my-first-repo

4. Push image to Docker Hub
docker push <your_username>/my-first-repo

# Pull image into NAS Docker app
1. Setup Registry
Registry -> Settings -> Add (fill in data with?)

2. Search for image via Registry search bar
or
Image -> Add -> URL = <your_username>/my-first-repo

# Setup Image from NAS Docker
1. Image -> Launch
Setup options
2. Container Name = something useful

Advanced Settings
3. Volume = mount points TBD
3a. 

4. Network = 

5. Port Settings = -p X:Y  X= Host, Y=Container

# Run Container from NAS Docker
1. Container -> switch
Unless it stays running it will swich off.  See the log for what it did

2. Details -> Log
should see a printout if running the above image


# Update image
1. 


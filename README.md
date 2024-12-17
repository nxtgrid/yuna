In order to build this you need to use at least 16GB machine in digital ocean, otherwise the build will get killed.

```git clone``` this directory

```make build-docker-full``` to build it

```docker image list``` to see the result images 

```sudo snap install doctl``` to install doctl 

```doctl auth init``` to authenticate doctl

```sudo snap connect doctl:dot-docker```

```doctl registry login``` to log into docker container registry using doctl

```docker tag <my-image> registry.digitalocean.com/bast/yuna``` to tag image before pushing to docker registry

```docker push registry.digitalocean.com/bast/yuna``` to push the image to docker registry

Now the image is available in the private registry. It can be used in https://github.com/nxtgrid/huli to update the docker image.

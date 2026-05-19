### Modifications

The stock pangeo-notebook image doesn't run on cirrus binder. 2 changes are made to it:

- add gosu into apt.txt
- use the cirrus start entrypoint that adds the user, chowns, and gosu

Build it like anything
docker buildx build --builder=remote -t hub.k8s.ucar.edu/cirrus-jhub/pangeo-notebook:>tag> -f Dockerfile --push .

You may want to modify the base image tag being used. By default it is pangeo/base-image:master. This can be modified in Dockerfile.

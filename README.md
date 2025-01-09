![EPFL Center for Imaging logo](https://imaging.epfl.ch/resources/logo-for-gitlab.svg)
# 🪐 Reference Deployment

Follow the steps below to set up and run a server providing access to several Imaging Server Kit algorithms using Docker.

**Algorithms**

- [StarDist](https://github.com/Imaging-Server-Kit/serverkit-stardist)
- [CellPose](https://github.com/Imaging-Server-Kit/serverkit-cellpose)
- [Spotiflow](https://github.com/Imaging-Server-Kit/serverkit-spotiflow)
- [Rembg](https://github.com/Imaging-Server-Kit/serverkit-rembg)
- [Scikit-image LoG detector](https://github.com/Imaging-Server-Kit/serverkit-skimage-LoG)
- [Orientationpy](https://github.com/Imaging-Server-Kit/serverkit-orientationpy)

## Setup

This repository uses [Git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules) to refer to each algorithm server. 
Clone the repository with all submodules:

```
git clone --recurse-submodules https://github.com/Imaging-Server-Kit/serverkit-deploy-docker
```

Make sure to have [Docker](https://docs.docker.com/engine/install/) and [Docker Compose](https://docs.docker.com/compose/) installed. From inside the repository, run the command:

```
docker compose up
```

This will

- Pull the base `imaging-server-kit` image from [Docker Hub](https://hub.docker.com/r/mallorywittwerepfl/imaging-server-kit).
- Build the algorithm server docker images specified in [docker-compose.yml](./docker-compose.yml)
- Run a server on http://localhost:8000 with all algorithms available

You can then connect to the server and run the algorithms from [Python](https://github.com/Imaging-Server-Kit/imaging-server-kit#python-client), [Napari](https://github.com/Imaging-Server-Kit/napari-serverkit), or [QuPath](https://github.com/Imaging-Server-Kit/qupath-extension-serverkit).

## Contributing

Contributions are very welcome.

## License

This project is distributed under the terms of the [BSD-3](http://opensource.org/licenses/BSD-3-Clause) license.

## Issues

If you encounter any problems, please file an issue along with a detailed description.

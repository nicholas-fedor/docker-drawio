# Changelog

## 2024-09-20

- Created `Changelog.md` for tracking changes
- Updated `./main/Dockerfile` to reflect the use of `nicholas-fedor/drawio`
  repository for building the container image
- Removed literal carriage returns from `./main/docker-entrypoint.sh`
  Shell command used: `cat docker-entrypoint.sh | tr -d '\r' >
  docker-entrypoint-fixed.sh`
- Added `./main/Makefile` for using `make` command to script out building the
  image and pushing to Docker Hub, GitHub, and my local Gitea registry

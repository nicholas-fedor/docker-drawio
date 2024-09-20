# Build Docker image, push to Docker Hub, tag for GitHub, push to GitHub, tag
# for local Gitea registry, and push to local Gitea registry
all: build-docker push-docker tag-ghcr push-ghcr tag-gitea push-gitea

build-docker:
	@docker build --tag=nickfedor/drawio:latest .

push-docker:
	@docker push nickfedor/drawio

build-ghcr:
	@ docker build . -t ghcr.io/nicholas-fedor/drawio:latest

push-ghcr:
	@ docker push ghcr.io/nicholas-fedor/drawio:latest

tag-ghcr:
	@docker tag nickfedor/drawio:latest ghcr.io/nicholas-fedor/drawio:latest

build-gitea:
	@ docker build . -t gitea.nickfedor.dev/nick/drawio:latest

push-gitea:
	@ docker push gitea.nickfedor.dev/nick/drawio:latest

tag-gitea:
	@ docker tag nickfedor/drawio:latest gitea.nickfedor.dev/nick/drawio:latest
IMAGE_REPOSITORY = koderover.tencentcloudcr.com/koderover-public
VERSION = v0.0.1

build: MAKE_IMAGE ?= ${IMAGE_REPOSITORY}/jira-updater:${VERSION}-amd64
build:
	@CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -v -o jira-updater main.go
	@docker build -f Dockerfile --tag ${MAKE_IMAGE} .
none:
	@echo ""

all: login build tag push

login:
	aws ecr get-login-password --region eu-west-2 | docker login --username AWS --password-stdin 772383167786.dkr.ecr.eu-west-2.amazonaws.com

build:
	docker build -t ecs-imagen .
tag:
	docker tag ecs-imagen:latest 772383167786.dkr.ecr.eu-west-2.amazonaws.com/ecs-imagen:latest
push:
	docker push 772383167786.dkr.ecr.eu-west-2.amazonaws.com/ecs-imagen:latest

default:
	@echo ""
	@echo "Targets for service '{{ cookiecutter.service_name }}':"
	@echo ""
	@echo "  version          Print Crossbar.io Docker image version ({{ cookiecutter.image }})"
	@echo "  version_host     Print Crossbar.io on host version"
	@echo "  start            Start Crossbar.io Docker image ({{ cookiecutter.image }})"
	@echo "  start_host       Start Crossbar.io on host"
	@echo ""

build:
	@echo "nothing to build here"

version:
	docker run -it --rm \
		--entrypoint /usr/local/bin/crossbar \
		{{ cookiecutter.image }} \
		version --personality community --loglevel debug

start:
	docker run -it --rm \
		--name {{ cookiecutter.service_name }} \
		--user {{ cookiecutter.uid }} \
		--net host \
		-v ${PWD}:/node \
		--entrypoint /usr/local/bin/crossbar \
		{{ cookiecutter.image }} \
		start --personality community --cbdir /node/.crossbar/

version_host:
	crossbar version --personality community --loglevel debug

start_host:
	crossbar start --personality community --cbdir ./.crossbar/

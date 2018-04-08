# {{cookiecutter.service_title}}

[Crossbar.io OSS](https://crossbar.io/) based service:

* service title: **"{{cookiecutter.service_title}}"**
* service name: **{{cookiecutter.service_name}}**
* service UUID: **"{{cookiecutter.service_uuid}}"**
* architecture: **{{cookiecutter.architecture}}**
* run-time: **{{cookiecutter.runtime}}**
* image: **{{cookiecutter.image}}**
* realm: **"{{cookiecutter.realm}}"**
* port: **{{cookiecutter.port}}**
* webdir: **"{{cookiecutter.webdir}}"**
* uid: **"{{cookiecutter.uid}}"**
* generated: **"{{cookiecutter.generated}}"**

> This service was generated using [cookiecutter](https://cookiecutter.readthedocs.io/) and [crossbar-fabric-shell](https://github.com/crossbario/crossbar-fabric-shell).

---


## Running

The [Makefile](Makefile) in this folder contains a number of targets to run this service. Type `make` to get a list of those:

```console
(cpy365_1) oberstet@thinkpad-t430s:~/test/crossbar$ make

Targets:

  version          Run Crossbar.io Docker image and print version
  version_host     Run Crossbar.io on host and print version
  run              Start Crossbar.io Docker image
  run_host         Start Crossbar.io on host
```

Usually however, you will want to run the service as part of a multi-container Docker Compose setup. See the next section.

---


## Running with Docker Compose

*Try [http://localhost:{{cookiecutter.port}}](http://localhost:{{cookiecutter.port}}).*

---

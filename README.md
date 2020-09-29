Notes on how to setup a jenkins server.

## Containerized jenkins

Create a directory on the host.

```bash
mkdir jenkins_home
```

Pull the docker image
```bash
docker pull jenkins/jenkins
```

Run the image
```bash
docker run --name myjenkins --publish 8080:8080 --publish 50000:50000 --volume ${PWD}/jenkins_home:/var/jenkins_home jenkins/jenkins
```

Connect to the interface and copy the generated admin password into the page.

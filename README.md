<b>+++ Task +++</b>

Create a simple microservice in any programming language of your choice, as follows:

The application should be a web server that returns a JSON response, when its / URL path is accessed: <b>
```json
{
  "timestamp": "<current date and time>",
  "hostname": "<Name of the host (IP also accepted)>",
  "engine": "<Name and/or version of the engine running>",
  "visitor ip": "<the IP address of the visitor>"
}
```
Create a Dockerfile for this microservice and publish the image to Docker Hub. Your application must be configured to run as a non-root user in the container.

Create a Kubernetes manifest in YAML format, containing a Deployment and a Service, to deploy your microservice on Kubernetes. Your Deployment must use your public Docker image.

Publish your code, Dockerfile, and Kubernetes manifests to a public Git repository in a platform of your choice (e.g. GitHub, GitLab, Bitbucket, etc.), so that it can be cloned and tested by the team.


<b>+++ Instructions +++</b>

A small micro service has been written in Go, so we can get results as you want and you can see as below .

[{"timestamp":"2022","hostname":"test","engine":"docker","visitor ":"192.168.1.1"}]

After that I containerized the application with Dockerfile .

Finally I developed a manifest file and then deploy application in kubernetes and call curl as below  ,

ubuntu@bastion-node:~$ curl http://127.0.0.1:8081/
[{"timestamp":"2022","hostname":"test","engine":"docker","visitor ":"192.168.1.1"}]

By the way , 8080 works but I did port forward because another 8080 system is running.

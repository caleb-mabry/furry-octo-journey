# Furry-Octo-Journey
This repository will show all of the steps required to bring all of my applications up in the event of losing my VPS. 

#
## Requirements
For this setup I'm going to be using Helm and Kubernetes. Considering most of this development is going to be happening locally until I can figure out HTTPS with NGINX-ingress, you can follow along with me on Windows.

* [Helm Installation](https://helm.sh/docs/intro/install/)
* [Chocolatey Installation](https://chocolatey.org/install)
* [Docker Desktop](https://www.docker.com/products/docker-desktop)

Docker Desktop has the ability to enable Kubernetes in the settings, so there's no need to do that.

**WARNING** If you were poking around and installed Minikube before Kubernetes, you'll run into some issues trying to run `kubectl` commands for Kubernets. [I found a solution that worked for me and seems to be issues others are having](https://stackoverflow.com/questions/57297337/docker-for-desktop-kubernetes-unable-to-connect-to-the-server-dial-tcp-164)
# 
# Starting everything up

1. `kubectl apply -f the-next-chapter.yaml`
2. `kubectl apply -f ripping-resource.yaml`
3. `kubectl apply -f ingress.yaml`
4. Make sure to install the ingress controller: `helm install quickstart ingress-nginx/ingress-nginx`

#
# Contributing
At the time, I'm not really accepting any pull requests. If you have suggestions, feel free to mention them in the issues section of the repository. As this is a learning experience, I can't imagine anyone would want to contribute to this repository. I'm hoping that this repo may serve as a guide to anyone who stumbled across it.


## License
[MIT](https://choosealicense.com/licenses/mit/)
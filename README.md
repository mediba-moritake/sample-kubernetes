# sample-kubernetes

# Docker for Mac [Edge] で Kubernetes を試してみる

## 前提
- [Docker for Mac [Edge]](https://docs.docker.com/docker-for-mac/install/#download-docker-for-mac)
- 
```shell
$ docker -v
Docker version 18.03.0-ce-rc4, build fbedb97

$ kubectl version
Client Version: version.Info{Major:"1", Minor:"9", GitVersion:"v1.9.2", GitCommit:"5fa2db2bd46ac79e5e00a4e6ed24191080aa463b", GitTreeState:"clean", BuildDate:"2018-01-18T10:09:24Z", GoVersion:"go1.9.2", Compiler:"gc", Platform:"darwin/amd64"}
Server Version: version.Info{Major:"1", Minor:"9", GitVersion:"v1.9.2", GitCommit:"5fa2db2bd46ac79e5e00a4e6ed24191080aa463b", GitTreeState:"clean", BuildDate:"2018-01-18T09:42:01Z", GoVersion:"go1.9.2", Compiler:"gc", Platform:"linux/amd64"}

$ helm version
Client: &version.Version{SemVer:"v2.8.1", GitCommit:"6af75a8fd72e2aa18a2b278cfe5c7a1c5feca7f2", GitTreeState:"clean"}
Server: &version.Version{SemVer:"v2.8.1", GitCommit:"6af75a8fd72e2aa18a2b278cfe5c7a1c5feca7f2", GitTreeState:"clean"}
```

## git clone
```shell
$ git clone git@github.com:mediba-moritake/sample-kubernetes.git
```

## Deployment, Service, Ingress 作成
```shell
$ kubectl create -f deployment.yml -f service.yml -f ingress.yml
```

## 確認
```shell
$ curl localhost
Hello k8s!
```

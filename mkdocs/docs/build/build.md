# **Jenkins 빌드**
---
## 1. 빌드 방법
### 1) amazon linux2 서버 빌드
> /workspace/ami/packer/build_awslinux2 <br>
> directory 하위에 원하는 json 이미지를 실행한다.
~~~
$ cd ~/workspace/ami/packer/build_awslinux2
$ packer build jenkins-ami.json
~~~
### 2) ubuntu 서버 빌드
> /workspace/ami/packer/build_ubuntu <br>
> directory 하위에 원하는 json 이미지를 실행한다.
~~~
$ cd ~/workspace/ami/packer/build_ubuntu
$ packer build jenkins-ami.json
~~~

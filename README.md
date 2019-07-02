# Docker User Guide

## Docker 설치 가이드

[Tensorflow Docker 설치 가이드](https://github.com/deeplearningzerotoall/TensorFlow/blob/master/docker_user_guide.md)

## 도커 이미지 설치 및 학습용 코드 Clone 하기

- hub.docker.com 에서 도커 이미지를 받아서 설치 합니다.(회원 가입이 필요 합니다.)

- docker 설치가 완료되면, tensorflow docker 이미지를 다운로드 합니다.

    `docker pull deeplearningzerotoall/tensorflow`

- 설치된 docker images를 확인 합니다.

    `docker images`

- 도커 이미지로부터 컨테이너를 생성하고 실행합니다.(jupyter notebook이 실행 됩니다.)

    `docker run -i -t --name tf -p 8888:8888 -p 6006:6006 deeplearningzerotoall/tensorflow`

    - 위 명령 실행 후 나타나는 URL 주소를 웹 브라우저에 붙여넣기 하면 jupyter notebook에 접속 됩니다.( http://localhost:8888/?token=...)

- 명령 창을 하나 더 띄워서 docker 프로세스를 확인 합니다.

    `docker ps -a`

    - status가 "Up 2 minutes"와 같이 나타나면 실행중인 상태 입니다.

- 아래 명령으로 종료된 컨테이너를 다시 실행할 수 있습니다.(docker run 명령은 한번 만 실행하면 됩니다.)

    `docker start tf`

- docker 터미널(bash 명령창)에 접속하려면 아래 명령을 실행하면 됩니다.

    `docker exec -it tf /bin/bash`

- bash 프롬프트에서 아래 명령으로 github의 tensorflow 코드를 내려 받으세요. (이제 docker 이미지가 실행중인 상태에서, jupyter notebook에서 deeplearningzerotoall/TensorFlow를 사용할 수 있습니다.)

    `git clone https://github.com/deeplearningzerotoall/TensorFlow.git`

# Cloud

전체 프로젝트에서 클라우드 가 맡은 부분중에 하나인 웹부분의 Front-end, Back-end 부분입니다.

마이크로서비스 형식으로 로그인, 광고등록, 메인서버, 데이터베이스를 활용한 시각화 서버 4개를 활용하여 제작하였습니다.

서버간 IP 통신을 Consul을 사용하여 제작하였고 JWT Access Token을 사용하여 로그인, 로그아웃 기능과 페이지 권한, 역할 들을 설정하였습니다.

도메인[http://focuson-me.site]을 구입하여 서비스 완성을 하였고 전체적인 완성부분은 영상파일과 PPT파일을 통해 보여드리도록 하겠습니다.  PPT 파일은 Git에 올려져 있습니다.

[시연영상](https://youtu.be/ilDDUEYq-VQ)

▶ Tool

- Language : Python
- IDE : VScode
- Library : boto3 / JWT / Consul / Pymysql / Restful API
- Web Tool : HTML / CSS / JS
- Web Framework : Flask



## Collaborators

- Bigdata : [장희연](https://github.com/hiiiiyeon), [최예슬](https://github.com/yschoi9930)
- AI : [이성렬](https://github.com/leesungryul)
- IoT : [도시영](https://github.com/dsy-sw)



![image-20210602155556065](README.assets/image-20210602155556065.png)

저는 웹 서비스의 프론트엔드와 백엔드 부분과 AWS EC2, RDS, SDK 등을 이용하여 전제적인 서비스 부분을 관리하였습니다. EC2내에서 IP관리는 Consul을 통해 관리를 하였습니다.



# 배경

![image-20210602161811659](README.assets/image-20210602161811659.png)



![image-20210602161920700](README.assets/image-20210602161920700.png)



# Architecture

![image-20210602160215706](README.assets/image-20210602160215706.png)

처음 광고주가 도메인으로 접속을 하면 EC2에서 실행중인 서비스에 ELB를 통하여 접속을 하고 웹 서비스에서 광고를 등록합니다. 그 다음 엘리베이터에 탑승객이 들어오면 그 사람을 인식하고 특정 광고를 송출합니다.

모든 데이터들은 RDS에 저장하도록 하였습니다.
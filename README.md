# Curator Drone
**2021-1st semester**

**Python, yolo, olympe**

## 예시 사진
[![self-walking_robot](http://img.youtube.com/vi/J8ql7rU-jMM/0.jpg)](https://www.youtube.com/watch?v=J8ql7rU-jMM)

## Procedure

### Tracking

* 사람을 인식하는데 Yolo를 사용하였다.
* red box dhk simple algorithm을 이용해 사람들을 추적할 수 있었다.

  
![ex_screenshot1](./img/1.png)

### AR-Marker

* 그림을 인식하는데 AR-Marker을 사용하였다.
* 각각의 그림이 특정 AR-Marker을 가르킨다.

![ex_screenshot2](./img/2.png)


### crawling

* 그림이 인식되면 드론이 자동적으로 위키피디아에서 그림에 대한 정보를 찾는다.
* 그리고 오디오 파일에 정보를 담아서 사용자에게 이메일로 전송한다.

![ex_screenshot3](./img/3.png)

## 프로젝트를 하면서 어려웠던 점
1. yolo를 통해 사람을 인식할때 이미지 단위로 인식한다. 그런데 드론은 실시간으로 영상을 카메라에서 받기 때문에 시간당 이미지를 몇개 받느냐를 조절하는 부분이 어려웠다. 우리는 드론이 사람을 인식하면 그 사람과의 거리를 유지하기 위해 드론이 동서남북으로 움직이게 하였는데, 이미지를 실시간으로 받다 보면 yolo에서 이미지를 처리하는데 에러가 생겨서 드론이 한쪽 방향으로만 계속 가는 오류가 있었다. 그렇게 되면 인명피해가 날 수도 있는 위험한 상황이다. 그래서 카메라가 드론을 인식하는 코드를 찾아 카메라에서 실시간으로 받는 프레임을 적절히 조절하여 욜로에서 이미지를 받는 속도를 개선하여 드론이 사람과의 거리를 조절하여 움직이는데 성공하였다.
2. 네트워크 문제. wifi로 드론과 연결하면서 동시에 email로 전송하기 위해서는 유선 랜을 꼽아야 하였다. 실내에서 데스크탑이 있는 환경에서 하여 문제를 해결하였지만, 만약 실외거나 유선 랜을 사용할 수 없는 환경이라면 불가능하였다.

## Limitations
* yolo-tiny의 정확도가 높지 않아 사용자 주위에서 drone rotate을 하지 못하였다.
* Drone 과 laptop이 wifi로 연결되있기 때문에 서로 가까이 있어야 했다. 그래서 드론과 서버를 연결하는 다른 방법을 찾아야 했다.
* 드론이 정보를 찾을 때 끝까지 수행할 때까지 드론은 멈춰있었다.


## What I've learned
* Yolo framework를 embedded system에서 어떻게 이용하는지
* 다른 개발자들과 협력하는 법






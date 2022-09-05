# gigacha-vision-master
## How to use
1. git clone --recursive https://github.com/sh-song/gigacha-vision-master.git
2. ./run_all.sh
3. ./kil_all.sh

All modules(lidar, fusion, yolo, ...) are in 'modules' directory as github submodules.

Each module should contain:
1. Dockerfile
2. docker_build.sh
3. run.sh
on its uppermost directory.

Container name in 'run.sh' >> module_list.json in this repo

TODO
1. add submodules in 'modules' directory


```
├─ README.md
├─ run_all.sh => shells 폴더 안에 있는 모든 sh파일 실행(각각 컨테이너 생성)
├─ kill_all.sh => run_all.sh으로 실행한 모든 컨테이너 종료
├─ module_list.json => 모듈별 레포지토리 이름, 컨테이너 이름 등이 기록돼있음
├─ modules => 안에 git submodule로 각 모듈의 레포지토리 존재. 다른 모듈들 추가 필요.
│  ├─ gigacha_sensorfusion
│  └─ obstacle-tracker
└─ shells
   ├─ run_camera.sh => 카메라 센서 실행
   ├─ run_fusion.sh => 카메라-라이다 퓨전 실행
   ├─ run_lidar.sh => 라이다 센서 실행
   ├─ run_tracker.sh => 라이다 클러스터 트래커 실행
   └─ run_yolo.sh => 욜로 실행
```

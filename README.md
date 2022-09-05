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



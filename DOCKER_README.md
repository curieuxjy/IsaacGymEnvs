docker build . -t avery/isaacgymenvs -f docker/Dockerfile --build-arg UID=$UID --no-cache

docker run -ti --name="gymenvs" --privileged -e DISPLAY=:0 -e TERM=xterm-256color -v /tmp/.X11-unix:/tmp/.X11-unix:ro --network host -v /home/avery/Documents:/home/user/Documents --gpus all isaacgym/isaacgymenvs /usr/bin/zsh

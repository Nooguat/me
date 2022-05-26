# GUI in chroot
Easily done using X11
`mkdir -p /Lab/tmp/.X11-unix` create new socket in chrooted env
`mount --bind /tmp/.X11-unix /Lab/tmp/.X11-unix` link your own socket to the chrooted one
`xhost + local:` let the chroot connect to the server
`export DISPLAY=:0` (in the chrooted env) connect to the server
**java will not work OOB** it needs another env var :  _JAVA_AWT_WM_NONREPARENTING=1 



[Sources]

# How to destroy a system

rm -rf / does not work, just delete the kernel file
Remove file completely using shred
can use $ dd if=/dev/null of=/dev/sdX or mv /*/** /dev/null

[Sources]

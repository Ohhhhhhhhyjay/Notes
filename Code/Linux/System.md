## Useful packages
`aptitude`: Use `sudo aptitude install <package>` to better build dependencies.
`anaconda`: See [Anaconda](Anaconda.md)
`laptop-mode-tools`: If have trouble waking the system from sleep.

## Often used commands
### Download & install
`sudo dpkg -i <.deb filename>`: -i means install
`bash anaconda...sh`: install anaconda
`curl -C - --retry 10 <url> -o ./WST.zip`: download the file, continue automatically and retry 10 times if failed

### Run scripts
`source <filename>`

### ls
`ls -lh` to list files


## System information
`top` : CPU status Press 1 to see individual cores, press t to see graph
`watch -n 1 nvidia-smi` : GPU usage
`lscpu` : short for list cpu, CPU info
`df -h <dir>` : check disk space
`du -hc --max-depth=0 <dir>` : Check the size of the directory size
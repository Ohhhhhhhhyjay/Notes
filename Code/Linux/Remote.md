## ssh
Log in using `ssh` command

```shell
ssh ohhhhhhhhjay@appalachia.astro.columbia.edu
```

Transfer files using `scp` command

```shell
scp -r ohhhhhhhhjay@appalachia.astro.columbia.edu:/appalachia/d6/yujie/save ./ # save data
scp -r ohhhhhhhhjay@appalachia.astro.columbia.edu:~/Test_GaussianFieldsClassification ./ # save code and plots
```

To config ssh, the configuration file is at `~/.ssh/config`
Use `sudo vim ~/.ssh/config` to edit it.

Creating key pairs

https://carpentries-incubator.github.io/shell-extras/02-ssh/index.html

注意，`authorized_keys`文件的权限要设为`644`，即只有文件所有者才能写。如果权限设置不对，SSH 服务器可能会拒绝读取该文件。

```shell
chmod 644 ~/.ssh/authorized_keys
```

## Screen: keep running when logged off

```shell
screen -S <session_name> # open a new screen session
Ctrl+A+D # detach
exit # quit
screen -r # resume
screen -r 37672.pts-17.appalachia # something like that, if there are more than one screens
```

- To navigate in screen

press Ctrl + A then Esc to enter copy mode.

In the copy mode, you should be able to move your cursor around using the Up/Down arrow keys (↑ and ↓) as well as Ctrl + F (page forward) and Ctrl + B (page back).

To exit the copy mode and get back to the shell, press Q or Esc

- To rename an existing session

Ctrl + a, : sessionname <session_name>, Enter
## Starting jupyter

```shell
jupyter notebook --no-browser --port=8080 # on the server
ssh -L 8080:localhost:8080 ohhhhhhhhjay@appalachia.astro.columbia.edu # in local terminal
```

## About the server
Some information about the machine we used at CU.

CPU: Intel® Xeon® Gold 5220 Processor 18 Cores 2.20 GHz
GPU: Nvidia Quadro P1000
DISK: 412 G
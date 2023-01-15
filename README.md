# How to build
For example, if you want to install the hello command, execute the following commands.

```bash
$ mkdir ws && cd ws
$ repo init -u https://gerrit.automotivelinux.org/gerrit/AGL/AGL-repo
$ repo sync
$ git clone https://github.com/ktact/AGL-repo-build.git
$ source meta-agl/scripts/aglsetup.sh -m qemux86-64 -b qemux86-64 agl-demo agl-devel
$ bitbake-layers add-layer ../meta-tutorial
$ bitbake hello
```

After the build is complete, you can find the rpm files under `ws/{machine}tmp/deploy/rpm/{arch}`.
```bash
$ ls tmp/deploy/rpm/corei7_64
hello-0.1-r0.corei7_64.rpm  hello-dbg-0.1-r0.corei7_64.rpm  hello-dev-0.1-r0.corei7_64.rpm  hello-src-0.1-r0.corei7_64.rpm
```

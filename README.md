# My own notes for diplomas thesis

When I want to fetch new things from the original repostitory I can use the next
article:
https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork

But before I need to verify if I have set up the upstream (original ReaR):
```
$ git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git
```
more here: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/configuring-a-remote-for-a-fork


## TMT
### Sanity tests via tmt
There I returned the original name for REBOOTCOUNT variable.
Before it didn't work with the REBOOTCOUNT, because tmt expects REBOOT_COUNT name.
https://github.com/antonvoznia/rear-testing/commit/d2d1c40e26984bb6bc35394dab5f6bd9ccab5ebb

### TMT connect
https://tmt.readthedocs.io/en/latest/spec/plans.html#connect

example
```
provision:
    how: connect
    guest: hostname or ip address
    user: username
    password: password

provision:
    how: connect
    guest: hostname or ip address
    key: private-key-path
```


## Make check
### Via Packit
There is guide how to setup the .packit.yaml file:
https://packit.dev/docs/testing-farm/

I added the make validate into rear.spec file:
https://github.com/antonvoznia/rear/commit/ddc8551bd9e32488c9cede7361f198cdfb8b0a4a
Now before the build it validates the ReaR's code.

The example of pull request with the validating on:
https://github.com/antonvoznia/rear/pull/38


## CentOS CI

CentOS CI one of few infrastructures I should study and examine if it matches
needs for the ReaR CI testing.
There is an example for systemd ci tes:
https://github.com/systemd/systemd-centos-ci

There is information about providing hardware:
https://wiki.centos.org/QaWiki/PubHardware
As we can see every machine support only 1 disk.
* Is it problem for us? Where we can place backup?...


## Configure NFS
### Configure NFS server
https://www.server-world.info/en/note?os=Fedora_31&p=nfs&f=1
### Configure NFS client
https://www.server-world.info/en/note?os=Fedora_31&p=nfs&f=2


In my case:
* server: 192.168.124.252
* client: 192.168.124.66

### Uboot
https://developer.toradex.com/knowledge-base/boot-from-a-tftpnfs-server

https://developer.toradex.com/knowledge-base/distro-boot-linux


## DUMP and notes
### Provision and prepare

upravit
ISO_DEFAULT=unattended
USB_DEFAULT=
git push -f
git reset --hard
git branch mymaster

how to change reference in tmt
https://fmf.readthedocs.io/en/latest/concept.html#identifiers

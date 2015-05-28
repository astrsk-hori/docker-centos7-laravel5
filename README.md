# docker-centos7-laravel5
dockerでlaravel5が動く環境を作成

centos7でlaravel5

とりあえずdockerでlaravel5が動くとこまでメモ予定

現在はphpが動くとこまで。

## build

```bash
docker build -t horie/centos7:1.0 ./centos7
docker build -t horie/laravel5:1.0 ./php54-laravel5
```

## ハマったところ

dockerのバージョン1.3を使っていたらphpのインストールが失敗した。

`yum install php`

```bash
error: unpacking of archive failed on file /usr/sbin/suexec: cpio: cap_set_file                                                                                                 │~
error: httpd-2.4.6-31.el7.centos.x86_64: install failed
```

dockerのバージョンアップで動くようになった



## docker version up

installerでインストールしてる場合は最新のインストーラーで最新にする。

それだけだと以下のようなエラーが出る。

```bash
$ docker version
Client version: 1.6.2
Client API version: 1.18
Go version (client): go1.4.2
Git commit (client): 7c8fca2
OS/Arch (client): darwin/amd64
FATA[0000] Error response from daemon: client and server don't have same version (client : 1.18, server: 1.15)
```

`boot2docker upgrade`実行でserver側もバージョンアップされる。

```bash
docker version
Client version: 1.6.2
Client API version: 1.18
Go version (client): go1.4.2
Git commit (client): 7c8fca2
OS/Arch (client): darwin/amd64
Server version: 1.6.2
Server API version: 1.18
Go version (server): go1.4.2
Git commit (server): 7c8fca2
OS/Arch (server): linux/amd64
```

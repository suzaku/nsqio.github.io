--- 
title: Installing
layout: post
category: deployment
permalink: /deployment/installing.html
---

### <a name="binary">Binary Releases</a>

Pre-built binaries for linux, darwin, freebsd and windows are available for download:

#### Current Stable Release: **`v0.3.7`**

 * [nsq-0.3.7.darwin-amd64.go1.6.tar.gz][0.3.7_darwin_go16]
 * [nsq-0.3.7.linux-amd64.go1.6.tar.gz][0.3.7_linux_go16]
 * [nsq-0.3.7.freebsd-amd64.go1.6.tar.gz][0.3.7_freebsd_go16]
 * [nsq-0.3.7.windows-amd64.go1.6.tar.gz][0.3.7_windows_go16]

#### Older Stable Releases

 * [nsq-0.3.6.darwin-amd64.go1.5.1.tar.gz][0.3.6_darwin_go151]
 * [nsq-0.3.6.linux-amd64.go1.5.1.tar.gz][0.3.6_linux_go151]
 * [nsq-0.3.5.darwin-amd64.go1.4.2.tar.gz][0.3.5_darwin_go142]
 * [nsq-0.3.5.linux-amd64.go1.4.2.tar.gz][0.3.5_linux_go142]
 * [nsq-0.3.2.darwin-amd64.go1.4.1.tar.gz][0.3.2_darwin_go141]
 * [nsq-0.3.2.linux-amd64.go1.4.1.tar.gz][0.3.2_linux_go141]
 * [nsq-0.3.1.darwin-amd64.go1.4.1.tar.gz][0.3.1_darwin_go141]
 * [nsq-0.3.1.linux-amd64.go1.4.1.tar.gz][0.3.1_linux_go141]

### Docker

See [the docs][docker_docs] for deploying NSQ with [Docker][docker].

### OSX

     $ brew install nsq

### Building From Source

#### Pre-requisites

 * **[golang](http://golang.org/doc/install)** (version **`1.4+`** is required)
 * **[gpm](https://github.com/pote/gpm)** (dependency manager)

#### Compiling

NSQ uses **[gpm](https://github.com/pote/gpm)** to manage dependencies and produce reliable
builds.  **Using `gpm` is the preferred method when compiling from source.**

{% highlight bash %}
$ gpm install
$ go get github.com/nsqio/nsq/...
{% endhighlight %}

NSQ remains `go get` compatible but it is not recommended as it is not guaranteed to
produce reliable builds (pinned dependencies need to be satisfied manually).

#### Testing

{% highlight bash %}
$ ./test.sh
{% endhighlight %}

[0.3.7_darwin_go16]: https://s3.amazonaws.com/bitly-downloads/nsq/nsq-0.3.7.darwin-amd64.go1.6.tar.gz
[0.3.7_linux_go16]: https://s3.amazonaws.com/bitly-downloads/nsq/nsq-0.3.7.linux-amd64.go1.6.tar.gz
[0.3.7_freebsd_go16]: https://s3.amazonaws.com/bitly-downloads/nsq/nsq-0.3.7.freebsd-amd64.go1.6.tar.gz
[0.3.7_windows_go16]: https://s3.amazonaws.com/bitly-downloads/nsq/nsq-0.3.7.windows-amd64.go1.6.tar.gz

[0.3.6_darwin_go151]: https://s3.amazonaws.com/bitly-downloads/nsq/nsq-0.3.6.darwin-amd64.go1.5.1.tar.gz
[0.3.6_linux_go151]: https://s3.amazonaws.com/bitly-downloads/nsq/nsq-0.3.6.linux-amd64.go1.5.1.tar.gz

[0.3.5_darwin_go142]: https://s3.amazonaws.com/bitly-downloads/nsq/nsq-0.3.5.darwin-amd64.go1.4.2.tar.gz
[0.3.5_linux_go142]: https://s3.amazonaws.com/bitly-downloads/nsq/nsq-0.3.5.linux-amd64.go1.4.2.tar.gz

[0.3.2_darwin_go141]: https://s3.amazonaws.com/bitly-downloads/nsq/nsq-0.3.2.darwin-amd64.go1.4.1.tar.gz
[0.3.2_linux_go141]: https://s3.amazonaws.com/bitly-downloads/nsq/nsq-0.3.2.linux-amd64.go1.4.1.tar.gz

[0.3.1_darwin_go141]: https://s3.amazonaws.com/bitly-downloads/nsq/nsq-0.3.1.darwin-amd64.go1.4.1.tar.gz
[0.3.1_linux_go141]: https://s3.amazonaws.com/bitly-downloads/nsq/nsq-0.3.1.linux-amd64.go1.4.1.tar.gz

[docker]: https://docker.io/
[docker_docs]: {{ site.baseurl }}/deployment/docker.html

你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
# go-kinesis
[![Build Status](https://travis-ci.org/sendgridlabs/go-kinesis.png?branch=master)](https://travis-ci.org/sendgridlabs/go-kinesis)

GO-lang library for AWS Kinesis API.

## Documentation

* [Core API](http://godoc.org/github.com/sendgridlabs/go-kinesis)
* [Batch Producer API](http://godoc.org/github.com/sendgridlabs/go-kinesis/batchproducer)

## Example

Example you can find in folder `examples`.

## Command line interface

You can find a tool for interacting with kinesis from the command line in folder `kinesis-cli`.

## Testing

### Local Kinesis Server

The tests require a local Kinesis server such as [Kinesalite](https://github.com/mhart/kinesalite)
to be running and reachable at `http://127.0.0.1:4567`.

To make the tests complete faster, you might want to have Kinesalite perform stream creation and
deletion faster than the default of 500ms, like so:

    kinesalite --createStreamMs 5 --deleteStreamMs 5 &

The `&` runs Kinesalite in the background, which is probably what you want.

### go test

Some of the tests are marked as safe to be run in parallel, so to speed up test execution you might
want to run `go test` with [the `-parallel n` flag](https://golang.org/cmd/go/#hdr-Description_of_testing_flags).

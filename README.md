# Keys and Values App

此repository是[Apache Mesos(7)-Marathon的高级应用](https://andyyoung01.github.io/2016/08/03/Apache-Mesos-7-Marathon%E7%9A%84%E9%AB%98%E7%BA%A7%E5%BA%94%E7%94%A8/)的示例代码。对Mesos in Action的[keys-values-app](https://github.com/rji/mesos-in-action-code-samples/tree/master/keys-values-app)的Bundle源进行了替换，替换为阿里云镜像，使国内下载速度更快。

A simple Ruby web application (implemented using the Sinatra framework) that
stores key/value pairs in a Redis database.

## Prerequisites

Each of the machines running this web app must have the following already
installed:

  - Ruby - tested with versions 1.9.3, 2.0.0, and 2.1.5
  - Bundler - tested with version 1.8.4

## Usage

The listening port for the application will use the environment variable
`$PORT`, as set by Marathon. If the variable isn't set, it will fallback to
8080.

Furthermore, the following environment variables must be set:
  - `REDIS_HOST`
  - `REDIS_PORT`

Install the necessary Ruby gems:

```
$ bundle install
```

Run the app:

```
$ bundle exec ruby app.rb
```

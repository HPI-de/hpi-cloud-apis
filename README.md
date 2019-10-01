# hpi-cloud-apis

[![Build Status](https://travis-ci.com/HPI-de/hpi-cloud-apis.svg?branch=dev)](https://travis-ci.com/HPI-de/hpi-cloud-apis)
[![GitHub Release](https://img.shields.io/github/v/release/hpi-de/hpi-cloud-apis?include_prereleases&sort=semver&label=Release)](https://github.com/HPI-de/hpi-cloud-apis/releases)
[![Bintray](https://img.shields.io/bintray/v/hpi/hpi-cloud-mvn/hpi-cloud?label=Bintray)](https://bintray.com/hpi/hpi-cloud-mvn/hpi-cloud/_latestVersion)

This repository contains the original interface definitions of public HPI Cloud APIs that support the gRPC protocol. Reading the original interface definitions can provide a better understanding of HPI Cloud APIs and help you to utilize them more efficiently. You can also use these definitions with open source tools to generate client libraries, documentation, and other artifacts.

These [Protocol Buffers](https://developers.google.com/protocol-buffers/) define the structure used for persistence.


> **Note:** All of the following commands should be executed from within this folder.


## Generate source code

> **Note:** The following guide was only tested on Linux (Ubuntu).

<details>
<summary>Install protoc</summary>

Download release `protoc-<VERSION>-linux-x86_64.zip` from https://github.com/protocolbuffers/protobuf/releases

```sh
sudo apt install autoconf automake libtool curl make g++ unzip
unzip protoc-<VERSION>-linux-x86_64.zip -d protoc3
sudo mv protoc3/bin/* /usr/local/bin/
sudo mv protoc3/include/* /usr/local/include/
sudo chown $USER /usr/local/bin/protoc
sudo chown -R $USER /usr/local/include/google
```
</details>

<details>
<summary>Install Dart</summary>

Source: <https://dart.dev/get-dart>

```sh
sudo apt update
sudo apt install apt-transport-https
sudo sh -c 'curl https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -'
sudo sh -c 'curl https://storage.googleapis.com/download.dartlang.org/linux/debian/dart_stable.list > /etc/apt/sources.list.d/dart_stable.list'
sudo apt update
sudo apt install dart
export PATH=$PATH:/usr/lib/dart/bin
```
</details>

<details>
<summary>Install protoc plugin for Dart</summary>

Source: <https://grpc.io/docs/quickstart/dart>

```sh
pub global activate protoc_plugin
export PATH=$PATH:$HOME/.pub-cache/bin
```
</details>

<details>
<summary>Download Google Common Protos</summary>

```sh
git clone https://github.com/googleapis/api-common-protos.git ../api-common-protos
```
</details>


### Dart

```sh
shopt -s globstar
rm -rf ./lib/proto
mkdir -p ./lib/proto
protoc --proto_path=. \
    --proto_path=../api-common-protos \
    --dart_out=grpc:./lib/proto \
    ./hpi/**/*.proto \
    ../api-common-protos/**/*.proto
```


## License

Copyright 2019 hpi-cloud-apis

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

---
id: quickstart
sidebar_position: 2
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import ReactPlayer from 'react-player'

# Quickstart

In this post, we'll guide you through setting up a Kanthor system on your local machine, allowing you to interact with its exposed interfaces. Additionally, we've included screenshots and a demo video to demonstrate how to utilize these interfaces once you've completed the installation successfully.

## Installation

The easiest way to set up the Kanthor system on your machine is through Docker Compose

```bash
# create project directory
mkdir -p kanthor-project
# navigate to our root project directory
cd kanthor-project
# download the latest docker-compose.yaml
curl https://raw.githubusercontent.com/scrapnode/kanthor/master/docker-compose.latest.yaml -o docker-compose.yaml
# start the project
docker compose up -d
```

You can access the Kanthor system through various interfaces:

- [Kanthor Playground](http://localhost:9081): Utilize the Kanthor Playground, built on the [Kanthor SDK for Golang](https://github.com/scrapnode/kanthor-sdk-go), to experiment with functionalities or refer to it as a guide on how to use the Kanthor SDK.
- [Kanthor Console](http://localhost:9082): Access the Kanthor Console UI to configure the customer portal. The default credentials are:

  - Username: `admin@kanthorlabs.com`
  - Password: `changemenow`

- [Kanthor SDK OpenAPI](http://localhost:8180/swagger/index.html): Explore the OpenAPI document UI containing all available APIs in the Kanthor SDK service.
- [Kanthor Portal OpenAPI](http://localhost:8280/swagger/index.html): Access the OpenAPI document UI featuring all available APIs in the Kanthor Portal service.

## Interaction

To interact with the Kanthor System, the most convenient approach is utilizing the official Kanthor SDKs compatible with your preferred programming language. We support a range of languages, including Golang, JavaScript, Python, and .NET. However, if you're unable to locate an SDK for your language, you can also access the system through the REST API interface.

### SDK

<Tabs
defaultValue="go"
values={[
{label: "Go", value: "go"},
{label: "Javascript", value: "javascript"},
]}>
<TabItem value="go">

```bash
go get github.com/scrapnode/kanthor-sdk-go
```

</TabItem>

<TabItem value="javascript">

```bash
# comming soon
```

</TabItem>

</Tabs>

### REST

[Kanthor SDK API](https://sdk.kanthorlabs.com/swagger/index.html)

## Screenshots

<Tabs
defaultValue="playground"
values={[
{label: "Playground", value: "playground"},
{label: "Console", value: "console"},
{label: "SDK OpenAPI", value: "sdk"},
{label: "Portal OpenAPI", value: "portal"},
]}>
<TabItem value="playground">

![Playground](./assets/img/quickstart/playground.png)

</TabItem>

<TabItem value="console">

![Console](./assets/img/quickstart/console.png)

</TabItem>

<TabItem value="sdk">

![SDK OpenAPI](./assets/img/quickstart/sdk.png)

</TabItem>

<TabItem value="portal">

![Portal OpenAPI](./assets/img/quickstart/portal.png)

</TabItem>
</Tabs>

## Demo Video

There is a demo video showcasing the functionality of the Kanthor Webhook System using Kanthor Playground and Kanthor Console.

<ReactPlayer controls url="https://assets.kanthorlabs.com/docs/video/demo.webm" width="100%" />

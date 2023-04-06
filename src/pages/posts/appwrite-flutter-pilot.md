---
layout: ../../layouts/MarkdownPostLayout.astro
title: "Appwrite + Flutter: The Pilot Blog."
pubDate: 2023-04-06
description: "Let's learn to work with the best of the BaaS world and undoubtedly the best cross-platform UI toolkit."
author: "Chandram Dutta"
tags: ["life-update", "blog", "letter"]
---

Hello, let's fasten our seatbelts cause this blog series will take you through creating your next billion-dollar startup full-stack app based on the best of the Open-source World. We will be learning to use [Appwrite](https://appwrite.io/), the Open-source Backend-as-a-Service, with Flutter, the almighty UI toolkit to build an app which we will talk about in a moment.

But first, let's install Appwrite and Flutter.

## Appwrite Installation

To install Appwrite, make sure you have [Docker](https://www.docker.com). Here are the links to download and install Docker properly

- [On a Mac](https://docs.docker.com/desktop/install/mac-install/)
- [On Windows](https://docs.docker.com/desktop/install/windows-install/) (make sure you have WSL2 installed)
- [On Linux](https://docs.docker.com/desktop/install/linux-install/) for Docker Desktop, tho I personally prefer downloading the [Docker Engine for Linux](https://docs.docker.com/engine/install/ubuntu/) (and don't forget the [post-installation steps](https://docs.docker.com/engine/install/linux-postinstall/))

Once installed, let's install Appwrite image which is pasting just one line of script on your terminal!

- Linux/Mac
  ```bash
  docker run -it --rm \
      --volume /var/run/docker.sock:/var/run/docker.sock \
      --volume "$(pwd)"/appwrite:/usr/src/code/appwrite:rw \
      --entrypoint="install" \
      appwrite/appwrite:1.2.0
  ```
- CMD
  ```bash
  docker run -it --rm ^
      --volume //var/run/docker.sock:/var/run/docker.sock ^
      --volume "%cd%"/appwrite:/usr/src/code/appwrite:rw ^
      --entrypoint="install" ^
      appwrite/appwrite:1.2.0
  ```
- Powershell
  ```bash
  docker run -it --rm `
      --volume /var/run/docker.sock:/var/run/docker.sock `
      --volume ${pwd}/appwrite:/usr/src/code/appwrite:rw `
      --entrypoint="install" `
      appwrite/appwrite:1.2.0
  ```

Note: This scripts are for Appwrite version 1.2.0 which we will be using for the project! For the latest versions go to [Appwrite](https://appwrite.io) and click on Get Started.

At the end of the installation, it will prompt you to many inputs, going for the default options is my recommendation and if you did it, go to your http://localhost:80 and voila! you will be greeted with the beautiful Appwrite Console(made using [Svelte](https://svelte.dev),my favourite). Create an account and sign in.

## Flutter Installation

As for flutter, installing it through its [official documentation](https://docs.flutter.dev/get-started/install) is the best way!

- [macOS](https://docs.flutter.dev/get-started/install/macos)
- [Linux](https://docs.flutter.dev/get-started/install/linux) (Don't install the snap version)
- [Windows](https://docs.flutter.dev/get-started/install/windows)

Now, run `flutter doctor` and you should see all ticks green, if not, copy the red text and paste it on stack overflow and you should get your answers

## The app

So, a couple of days ago, I posted an app I was building as a side project on Twitter

%[https://twitter.com/chandramdutta/status/1609575130832965632?s=61&t=J-V5dlTHyy6puGQryDxvgg]

and realised there aren't any great Tutorials for the appwrite+flutter community. One resource worth mentioning is the [React Bits (Damodar Lohani) Flutter + Appwrite Tutorial Series on YouTube](https://youtube.com/playlist?list=PLUiueC0kTFqI9WIeUSkKvM-a_3fyaIiuk) however it's based on a very old version of Appwrite which isn't compatible with the latest version. The other and best resource is the [Official Appwrite Docs](https://appwrite.io/docs) which is the main source of knowledge in this blog series. To create a strong resource on integrating Appwrite perfectly with Flutter, I decided to document the entire process of developing the **Recipe App**, a social media for sharing your mouthwatering recipes to the world, in this blog series and mind you, I am still building the app at the time of writing this blog so let's learn together and build in public.

That's all to get you started with this blog series! In the next blog, we will talk about setting up our flutter apps, discussing the architecture and things like state management (will be Riverpod 2.0). Hope, the blog series will succeed in the prime objective of becoming the go-to resource for creating Flutter+Appwrite apps. See y'all soon in the next blog and do share it for the greater good of the community😁😁!

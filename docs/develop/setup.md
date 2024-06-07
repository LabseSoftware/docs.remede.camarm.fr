---
layout: default
title: Setup
nav_order: 0
has_children: true
permalink: /docs/develop/setup
---

# Setting up development environment

Follow these steps before developing on Remède.
{: .fs-6 .fw-300 }

## Setting up Ionic framework
Remède uses Ionic. You will install npm dependencies and requirements to start developing with Ionic.
{: .fs-6 .fw-300 }

1. Make sure you have **node 18** installed.
2. Move to the `app/` folder
3. Install dependencies
```shell
npm install
```
4. Install Ionic
```shell
npm install -g @ionic/cli
```

## Setting up mobile development - Android
Ionic framework let us build Remède for native platforms with Capacitor.
{: .fs-6 .fw-300 }

Developing for Android does not need special requirements. Just install npm dependencies.

See [Capacitor documentation](https://capacitorjs.com/docs/android) for more information.

{. :note}
> Make sure you have Android Studio installed.

## Setting up mobile development - iOS
IonicFframework let us build Remède for iOS.
{: .fs-6 .fw-300 }

We do not build Remède for iOs yet. Follow the [official Ionic documentation](https://ionicframework.com/docs/developing/ios).

{: .danger}
> Remède has not been tested yet on iOS ! Build and use it at your own risks...

## Fetch database
Remède latest database is not served by git because it is too large... We host our database on our own servers.
{: .fs-6 .fw-300 }

To fetch the latest database, you can use `curl` or `wget` as you prefer...

{: .warning}
> Execute these commands at project root.

- With `curl`
```shell
curl -o data/remede.db https://api-remede.camarm.fr/download?variant=remede
```

- With `wget`
```shell
wget -O data/remede.db https://api-remede.camarm.fr/download?variant=remede
```

{: .note}
> Remède used to store its databases on **Github LFS servers** but our quota has been exceeded... The databases which 
> are still stored in git lfs are **outdated**


---
title: macOS에 Azure CLI 2.0 설치하기
date: 2018-02-20 10:16:43
categories:
    - dev
    - azure.log
tags:
    - azure
thumbnail: /images/dev/azure.log/azure-cli-mac.png
---

![](/images/dev/azure.log/azure-cli-mac.png)

맥을 이용하는 유저는 Azure CLI를 [Homebrew](https://brew.sh/) 통해서 설치할수 있습니다.

## 1. 설치하기
`Homebrew` 통해서 설치하는 것이 가장 쉽습니다. `Homebrew` 통해 업데이트와 삭제도 쉽게 할수 있으니 [`Homebrew`가 없으면 설치](https://docs.brew.sh/Installation.html)하길 바랍니다.

```bash
brew update && brew install azure-cli
```

설치가 되면 `az` 명령을 이용하여 Azure CLI를 이용할수 있습니다.

### 1.1 설치시 발생되는 문제

#### Python 패키지를 찾을 수 없음
맥에 설치된 `Python`이 버전이 일치하지 않을 경우나 설치하는 과정에서 다른 문제가 발생할 수 있습니다. 
그래서 `Python` 버전을 찾게 다음과 같이 연결하면 됩니다.
```bash
brew link --overwrite python3
```
#### `Azure CLI 1.x`가 설치됨
낮은 버전이 설치된 경우 `Homebrew` 업데이트 안해서 발생하는 문제입니다. `Homebrew`를 업데이트한 후 `azure-cli`를 업그레이드하면 됩니다.
```bash
brew update && brew upgrade azure-cli
```

## 2. 업데이트
`azure-cli`는 약 2주마다 새 릴리즈를 한다고 합니다. 주기적인 업데이트를 받을 수 있습니다.
```bash
brew update && brew upgrade azure-cli
```

## 3. 삭제
```bash
brew uninstall azure-cli
```

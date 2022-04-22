---
layout: post
title: install docker for win10 home
categories: docker
tags: docker
---

* content
{:toc}


# install docker for win10 home

参照サイト：

```
https://docs.docker.jp/docker-for-windows/install-windows-home.html
```



### Windows 上で WSL2 機能の有効化

###### WSL(Windows Subsystem for Linux )[参照](https://docs.microsoft.com/en-us/windows/wsl/install)ーー最新のバージョンをインストール

```powershell
wsl --install
```

###### WLS2設定[参照２](https://docs.microsoft.com/ja-jp/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package)ーー指定のバージョンをインストール

- linux用windowsサブシステムを有効する

  ```powershell
  dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
  ```

- 仮想マシン機能有効する

  ```powershell
  dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
  ```

- linuxカーネル更新プログラムパッケージをダウンロード

  - [最新のパッケージをダウンロード](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)
  - ダブルクリックでインストール

- WSL2を既定のバージョンとして設定

  ```
  wsl --set-default-version 2
  ```

  

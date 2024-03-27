---
title: 解决WslRegisterDistribution failed with error 0x8007019e
author: ge2k
date: 2023-11-30 01:03:40 +0800 
categories: [Blogging, tools]
tags: [wsl]

---

![wsl.png](https://i.ibb.co/qgLVL4Q/2023-11-30-005237.png)

### 问题：安装并打开Ubuntu 22.04.2 LTS 报错 WslRegisterDistribution failed with error: 0x8007019e

![question.png](https://i.ibb.co/swCckN3/1.png)

### 步骤一：完善电脑设置

![check.png](https://i.ibb.co/tx1rYpT/2.png)

### 步骤二：安装WSL更新包

You can fix this issue by install this package: https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

More detail here:

https://learn.microsoft.com/zh-cn/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package

### 问题解决
![result.png](https://i.ibb.co/zQFDwCd/2023-11-30-004327.png)


## 资料来源

https://learn.microsoft.com/en-us/answers/questions/1152199/wslregisterdistribution-failed-with-error-0x800701

https://www.bilibili.com/video/BV1cP41137bV/?spm_id_from=333.337.search-card.all.click&vd_source=890879be0041154ef8107bc3fadcc7c4
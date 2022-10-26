# ASRock-Z370-QTJ2-Hackintosh

这是一个我自用的黑苹果 OpenCore EFI 配置，目前已支持 macOS 13.0(Ventura)

如果你有需要可以自行 Clone 到你的电脑上运行以及测试

### 配置清单

| 规格     | 详细信息                                     |
| -------- | ---------------------------------------- |
| 主板 | ASRock Z370M Pro4 |
| CPU | Inter Core ES 2.4GHz (QTJ2) |
| iGPU | Inter UHD 630 |
| GPU | Radeon RX 590 |

### 注意事项

## 安装需知

请打开你的主板 `BIOS` 菜单修改相关的设置，这是必须的一步。由于我懒得折腾所以你可以参考 [国光大佬的 BIOS 设置教程](https://apple.sqlsec.com/3-%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C/3-1.html)，基本上没太大问题。

## 关于 CPU 型号

由于我已经在 `PlatformInfo` 里写入了自定义 CPU 型号，所以在 MacOS 设置里可以看到 `2.4 GHz 六核Intel Core i9` 这样的一个 CPU 型号，如果不喜欢可以自行修改。

## 关于机型及序列号

该EFI没有序列号，所以你需要自行生产一个序列号并写入后方可使用。

## 一些小问题

EFI 内置的 itlwm Kext 目前处于预览版本，不太稳定。且从 macOS 12 升级的用户需要在安装前先 disabled 后使用，全新安装无需操作

### 结尾

由于我的技术有限导致这个 EFI 配置文件十分粗糙，还请大家谅解。

最后也欢迎大家关注我的 [Telegram 频道](https://t.me/keiko_gugu)

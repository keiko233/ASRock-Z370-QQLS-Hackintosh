# ASRock-Z370-QTJ2-Hackintosh

这是一个我自用的黑苹果 OpenCore EFI 配置

如果你有需要可以自行 Clone 到你的电脑上运行以及测试

### 配置清单

| 规格     | 详细信息                                     |
| -------- | ---------------------------------------- |
| 主板 | ASRock Z370M Pro4 |
| CPU | Inter Core 0000 2.4GHz 6C 12T (QTJ2) |
| iGPU | Inter UHD 630 |
| GPU | Radeon RX 590 |

### 注意事项

## 安装需知

请打开你的主板 `BIOS` 菜单修改相关的设置，这是必须的一步。由于我懒得折腾所以你可以参考 [国光大佬的 BIOS 设置教程](https://apple.sqlsec.com/3-%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C/3-1.html)，基本上没太大问题。

你需要基本的黑苹果安装流程，如果这个你都不会，建议自己去谷歌好好学习一趟（

## 关于显卡

经过我的不严谨测试，显卡这方面使用 `RX 460/470/480/550/560/570/580` 等一堆的免驱显卡都是可以正常使用的。但是！记得去 `config.plist` 的 `Devicd` 里的 `PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x0)` 修改 `model` 值以正确的显示你的显卡型号，默认是 `Radeon RX 590` 。不改的话也不是不能用（

如果你只使用核心显卡的话，可以删除 `config.plist` 的 `Devicd` 里的 `PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x0)` ，然后修改 `PciRoot(0x0)/Pci(0x2,0x0)` 里的 `AAPL,snb-platform-id` 值为 `0900A53E` 或 `00009B3E` 。

## 关于 CPU 型号

由于我已经在 `PlatformInfo` 里写入了自定义 CPU 型号，所以在 MacOS 设置里可以看到 `2.4 GHz 六核Intel Core i9` 这样的一个 CPU 型号，如果不喜欢可以自行修改。

### 结尾

由于我的技术有限导致这个 EFI 配置文件十分粗糙，还请大家谅解。

最后也欢迎大家关注我的 [Telegram 频道](https://t.me/keiko_gugu)# ASRock-Z370-QTJ2-Hackintosh

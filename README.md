# Adguard Home For Android模块

本项目是基于 [Adguard-Home-For-Magisk-Mod](https://github.com/liuzq2002/Adguard-Home-For-Magisk-Mod) 的修改分支。

## 📌 项目简介

本模块将 Adguard Home 以 Magisk 形式运行于 Android 系统。与原版相比，**核心区别在于移除了中对 `/data/system/ifw` 目录的删除操作**，以保留系统原有的防火墙规则配置。

## 🔄 与原版的主要差异

* **移除操作**：删除了原项目中 `customize.sh` 及服务脚本里针对 `/data/system/ifw` 目录的 `rm -rf` 命令。
* **保留策略**：安装/升级模块时，将**不再主动清理**该目录下的 `ifw.xml` 等策略文件。

> ⚠️ *特别声明*：虽然本模块代码已移除模块运行时对ifw的删除逻辑，但不保证其他外部因素（如 模块安装、系统 OTA 或并发脚本）会对此目录造成影响。强烈建议安装前手动备份 `/data/system/ifw` 目录。

## 📝 手动备份建议（重要）

若您担心规则丢失，请在刷入模块前自行备份ifw（虽然我自己安装是没有删除ifw，但不保证你们安装时不会删，因为我压根就看不懂shell的语法）

## 🙏鸣谢项目

[Adguard-Home-For-Magisk-Mod](https://github.com/liuzq2002/Adguard-Home-For-Magisk-Mod)
[AdguardHome](https://github.com/AdguardTeam/AdguardHome)


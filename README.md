# IMX6ULL_Linux_Learning

基于 i.MX6ULL 开发板的嵌入式 Linux 长期学习记录。最终目标是完成
**OCPP 云平台 + i.MX6ULL 模拟充电桩**项目，并作为学习记录与作品集长期维护。

## 开发环境

| 环节 | 选型 |
| --- | --- |
| 主机 | Windows |
| 编辑器 | VS Code + Remote - SSH |
| 开发机 | VMware Ubuntu 24.04（用户 `bk201`） |
| 目标板 | i.MX6ULL |

工作流：Windows 上的 VS Code 通过 Remote SSH 连到 Ubuntu，**所有代码、构建与
Git 操作都在 Ubuntu 上完成**，Windows 侧不保留第二份代码副本；仓库托管在 GitHub。

## 长期目标

1. Linux 基础
2. Linux C 应用开发
3. GPIO、设备树、字符设备驱动
4. Linux 网络编程、多线程、进程
5. OCPP 云平台 + i.MX6ULL 模拟充电桩

## 目录结构

```
IMX6ULL_Linux_Learning/
├── README.md        项目说明
├── .gitignore       忽略规则
├── .gitattributes   统一换行符
├── docs/            学习笔记与文档
├── labs/            分阶段练习代码
└── projects/        综合项目（最终充电桩项目放这里）
```

目录按需增长。`bsp/`、`scripts/`、`tools/`、`hardware/` 等到实际学到对应内容时
再创建，不做提前设计。

## 仓库约定

- 只存放**手写内容**：代码、笔记、脚本、配置、补丁。
- **不入库**：Linux 内核源码、U-Boot 源码、交叉编译工具链、rootfs、SD 卡镜像、
  编译产物。它们体积大且可重新获取，统一放在仓库之外，用脚本或文档记录获取方式与版本。
- 提交信息使用清晰的动词开头，例如 `docs: 补充字符设备驱动笔记`。
- 默认分支为 `main`。

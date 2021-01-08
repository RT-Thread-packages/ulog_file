# 基于文件系统的 ulog 插件

## 1、介绍

该软件包基于 ulog 组件，主要实现 ulog 文件系统后端工功能，并且支持配置参数存储功能 。

支持功能如下：

- 支持 ulog 日志存储到文件后端；

- 支持设置日志文件名，最大数量和大小；
- 支持日志文件循环存储功能；

### 1.1 许可证

本软件包遵循 MIT 许可，详见 `LICENSE` 文件。

### 1.2 依赖

- RT-Thread ulog 组件

## 2、如何打开

使用本软件包需要在 RT-Thread 的包管理器中选择它，具体路径如下： 

```c
RT-Thread online packages
    tools packages --->
        [*] ulog_file: The ulog file backend by filesystem.
            Version (latest)  --->
```

## 3、使用说明

### 3.1 文件后端初始化

```c
int ulog_file_backend_init(void);
```

需要在应用层调用 `ulog_file_backend_init()` 初始化函数，即可初始化 ulog 日志文件后端，开启日志输出到文件系统指定文件中；

### 3.1 文件后端取消初始化

```c
int ulog_file_backend_deinit(void);
```

需要在应用层调用 `ulog_file_backend_deinit()` 函数，可以注销 ulog 文件后端，取消日志输出到文件系统指定文件中；

## 4、联系方式

- 维护：ChenYong
- 主页：<https://github.com/RT-Thread-packages/ulog_file.git>
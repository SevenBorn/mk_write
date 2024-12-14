# Win11 卸载 linux 子系统 WSL2 及去掉 linux 图标。

Win11 卸载 linux 子系统 WSL2 及去掉 linux 图标。
1.使用 wsl 命令 删除安装的 Ubuntu 子系统
查看当前 windows 系统 安装的子系统
`wsl --list`

卸载 unbuntu-20.04 ，注意名字匹配（第一步你查询的安装的子系统名）
`wsl --unregister Ubuntu-20.04`

再次查看 当前 windows 系统 安装的子系统
`wsl --list`



2.卸载 ubuntu 完成，发现 explorer 资源管理器界面还有 linux 图标，只是里面为空。 根据自己需要，可以彻底删除 WSL2
1）卸载 Windows Sybsystem for Linux Update

按【WIN + I】，打开【设置】，

依次点击 【应用】–> 【应用和功能】

找到 Windows Sybsystem for Linux Update 卸载即可。

2）关闭 【适用于 linux 的 windows 子系统】。

按【WIN + I】，打开【设置】，

依次点击 【应用】–> 【可选功能】–> 【更多 windows 功能】

找到 【适用于 linux 的 windows 子系统】去掉 勾选，点击【确定】。

3）重启系统。


————————————————

                            版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。

原文链接：https://blog.csdn.net/qfyh_djh/article/details/137564578

---

# 注销（卸载）当前安装的Linux的Windows子系统

##### 1、查看当前环境安装的[wsl](https://so.csdn.net/so/search?q=wsl&spm=1001.2101.3001.7020)

```shell
wsl --list
```

##### 2、注销（卸载）当前安装的Linux的Windows子系统

```shell
wsl --unregister Ubuntu
```

##### 3、卸载成功，查看当前安装的Linux的Windows子系统

```shell
wsl --list
```

##### 4、查看可安装的Linux的Windows子系统

```shell
wsl --list --online
```

---

# wsl卸载重装

## 1. 卸载WSL

Note： 以下命令需使用[管理员权限](https://so.csdn.net/so/search?q=管理员权限&spm=1001.2101.3001.7020) PowerShell 执行。

### 1.1 搜索

```bash
Get-AppxPackage -AllUsers | Where-Object { $_.Name -like "*Linux*" }
```

结果样例，检查是否包含 `MicrosoftCorporationII.WindowsSubsystemForLinux` 。

```
Name                   : MicrosoftCorporationII.WindowsSubsystemForLinux
Publisher              : CN=Microsoft Corporation, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
Architecture           : X64
ResourceId             :
Version                : 2.2.4.0
```

### 1.2 卸载

```sh
Get-AppxPackage MicrosoftCorporationII.WindowsSubsystemForLinux | Remove-AppxPackage
```

## 2. 安装WSL

### 2.1 发行版下载地址：https://github.com/microsoft/WSL/releases

### 2.2 下载 [Microsoft.WSL_2.2.4.0_x64_ARM64.msixbundle](https://github.com/microsoft/WSL/releases/download/2.2.4/Microsoft.WSL_2.2.4.0_x64_ARM64.msixbundle) 或更新版本。

### 2.3 安装

`wsl --install --web-download` 


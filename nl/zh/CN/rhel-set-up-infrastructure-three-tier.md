---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-26"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 1. 为三层设置订购 256 GB 和 32 GB 服务器
{: #install_three_tier}

## 订购服务器
{: #order_servers}

执行[订购 32 GB 服务器](/docs/infrastructure/sap-netweaver-rhel-qrg/rhel-set-up-infrastructure-32GB.html#order_32GB)中的步骤以订购 SAP NetWeaver 应用程序服务器。以下步骤将指导您执行订购数据库服务器的过程。

1. 使用您的唯一凭证登录到 [{{site.data.keyword.cloud_notm}} 基础架构客户门户网站](https://control.softlayer.com)。
2. 单击“帐户汇总”页面上的**设备**图标。
3. 在“设备”页面上的 **{{site.data.keyword.baremetal_long}}** 下单击**每月**。将显示“服务器列表”对话框。
4. 单击**每月的起始价格**下的超链接以选择服务器 **BI.S1.NW256（操作系统选项）**。

## 选择服务器选项
{: #options_32GB}

1. 在**数量**字段中保留 **1** 不变。
2. 选择 **TOR01** 作为**数据中心**。
3. **服务器**缺省为基于所选服务器的预定义值，并且无法更改。
4. 单击 **32 GB RAM**，尽管 **RAM** 选择缺省为基于所选服务器的预定义值并且无法更改。
5. 选择 **Red Hat Enterprise Linux for SAP Business Application 6.X** 作为操作系统。
6. 在**硬盘驱动器**下，选择第二个 2 TB SATA 磁盘，从这两个磁盘创建 RAID1 的 RAID 存储器组（覆盖存储器总量），并选择 **Linux Basic** 作为**分区模板**。将 **LVM** 保持未选中状态。
7. 为**公用带宽**选择 **500 GB**。
8. 为**上行端口速度**选择 **1 Gbps 冗余公用和专用网络上行链路**。
9. 对于本示例，将其他所有字段保持缺省值。您可以参阅[设置裸机服务器](https://console.bluemix.net/docs/bare-metal/configuring.html#setting-up-your-bare-metal-servers)以获取各个选项的详细描述。
10.	单击页面底部的**添加到订单**。在验证订单后，您将重定向到“结帐”页面。

## 设置高级系统配置
{: #adv_config}

1. 将表 1 中的值用于“高级系统配置”下的字段。[高级系统配置](https://console.bluemix.net/docs/bare-metal/configuring.html#advanced-system-configuration)准则中提供了更多信息。

|              字段                |      值                                                              |
| -------------------------------- | -------------------------------------------------------------------- |
|后端 VLAN                         | 从下拉列表中进行选择，例如，`tor01.bcr01a.1241`     |
|子网                              | 从下拉列表中进行选择，例如，`10.114.63.64/26`       |
|前端 VLAN                         | 从下拉列表中进行选择，例如，`tor01.fcr01a.1199`     |
|子网                              | 从下拉列表中进行选择，例如，`169.55.137.160/27`     |
|供应脚本                          | 缺省为“无”                                                         |
|SSH 密钥                          | 缺省为“无”                                                         |
|主机名                            | 例如，`e2e2690`                                     |
|域                                | 例如，`saptest.com`                                 |
{: caption="表 1. 高级配置值" caption-side="top"}  

## 确认您的选择
{: #confirm_selections}

1. 在“结帐”页面上确认您的选择，然后单击页面右侧的**云服务条款**和**第三方软件协议**。
2. 单击**提交订单**。您将重定向到带有您的订单号的屏幕。可以打印此屏幕，因为这也是您的订单回执。

提交订单后，服务器将在一到四个小时（具体取决于您的订单）内可供使用。您可以在 {{site.data.keyword.slportal}} 主页面上的“设备详细信息”屏幕（**设备 > 设备列表**）中检查供应步骤的状态。单击与您的给定“主机名”和“域”匹配的**设备名称**以查看其状态。

## 后续步骤

  [2. 准备服务器以用于 SAP 安装](/docs/infrastructure/sap-netweaver-rhel-qrg/rhel-prepare-server-256GB.html)
  
  [3. 分区和文件系统](/docs/infrastructure/sap-netweaver-rhel-qrg/rhel-partition-256GB.html)
  
  [4. 准备网络](/docs/infrastructure/sap-netweaver-rhel-qrg/rhel-prepare-network.html#network)

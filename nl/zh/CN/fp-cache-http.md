---



copyright:
  years: 2017
lastupdated: "2018-11-12"

keywords: cache, configure, configuration, http, traffic

subcollection: citrix-netscaler-vpx


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:tip: .tip}
{:note: .note}
{:important: .important}

# 为 HTTP(S) 流量配置高速缓存重定向
{: #configure-cache-redirection-for-http-traffic}

要为 HTTP 或 HTTPS 流量配置高速缓存重定向，请执行以下步骤：

1. 转至**流量管理 > 高速缓存重定向 > 虚拟服务器**，然后单击**添加**。
2. 指定正向代理虚拟服务器的名称。从其相应的下拉列表中选择 **HTTP** 协议和**正向**高速缓存类型。然后，从专用子网中为此虚拟服务器分配 IP 地址。

	<img src="images/fp12.png" alt="图样" style="width: 300px;"/>

	单击**确定**以继续。

3. 查看摘要页面，然后单击**确定**。  
4. 单击**流量设置**以查看其他配置设置。
5. 根据您的需求，从“流量设置”中选择以下三个重定向选项中的一个选项：
	* **高速缓存** - 将所有出站请求定向到本地高速缓存服务器池。
	* **策略** - 检查高速缓存重定向策略，以确定请求是应该转发到高速缓存服务器池还是转发到目标服务器（源）。
	* **源** - 将所有出站请求定向到各自的目标服务器（源）。

6. 从 **DNS 虚拟服务器名称**下拉列表中，选择先前配置的 DNS 虚拟服务器，然后将**重定向**选项设置为**源**。

	<img src="images/fp13.png" alt="图样" style="width: 300px;"/>

	**注：**出站流量要定向到本地高速缓存服务器池时，将使用**目标虚拟服务器**设置。如果要将所有出站流量定向到源服务器，请使此设置保留为空。

7. 单击**确定**，然后单击**完成**。
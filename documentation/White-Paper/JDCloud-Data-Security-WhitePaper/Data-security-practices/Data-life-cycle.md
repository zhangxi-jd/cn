## 4.数据全生命周期安全保障
  为保障用户安全的处理云上数据，京东云对数据全生命周期的数据生产、数据存储、数据传输、数据访问、数据使用、数据销毁各阶段应用不同安全措施，配合京东云全流程数据安全保护体系，提供系统化的安全防护，并通过友好的操作界面和接口，方便用户使用与集成，满足不同行业用户对数据安全的个性化需求。

![Life-Cycle](https://user-images.githubusercontent.com/51605713/59327713-f0cbce80-8d1c-11e9-8a91-6dc90a53f555.jpg)
  
  ### 4.1 数据生产
  数据生产是用户产生新的内容，或对已有内容的替换、更新或修改。针对这一阶段，京东云建议用户首先做好数据分类，并进行风险分析，再根据风险分析结果，明确防护数据的存储位置、存储服务和安全防护措施，在数据全生命周期的起始阶段就做好数据的区分与隔离。
  
  - 数据分类分级
  
  在使用京东云服务时，用户是其数据的控制者、拥有者，建议由用户自行对其数据资产进行分类分级管理。用户可依据数据安全需求，对数据进行分类分级化管理，识别敏感数据，对各类别级别的数据实施差异化的保护、细粒度的管控，有助于满足合规要求，防止敏感数据泄露。
  
  建议每一个用户对其云端数据进行完整的风险评估。对于识别出的重要或敏感数据，用户可以按需要选择额外的数据保护措施。基于敏感数据发现的结果，京东云可以帮助用户进一步分析数据间的关系，输出数据分类和风险定级的信息，并推荐数据分类分级的架构方案。
  
  - 区域与隔离
  
  用户自主选择内容数据存储区域，可根据自己对地理位置的具体要求选择地点部署京东云服务。用户在区域中复制和备份自己业务数据，京东云未经用户授权，不会跨区域移动或复制用户的内容数据。
  
  用户数据一般存储于数据库中，为保障账户数据安全，基于数据库存储对用户数据进行隔离存储，即与用户业务数据及京东云平台自身数据等不同类别的数据相隔离，并等同享受数据库存储数据的安全保障措施。
  
  ### 4.2 数据存储
  数据存储是将数据提交到某种存储库中，通常在数据生产时发生。对于云端存储的敏感及重要数据，建议用户使用加密措施进行防护，降低数据泄露的风险。京东云通过安全策略及工具让用户拥有和控制自己的数据，确定内容的存储位置、保护动态和静态内容，并为用户管理对云服务和资源的访问权限。京东云为用户提供符合国家商用密码管理要求的加密服务，用户可轻松构建其安全应用。
  
  - 密钥管理
  
  京东云密钥管理服务KMS（Key Management Service）帮助用户管理及备份其加密密钥，提供云上密钥创建、禁用、轮换、删除等全生命周期管理。KMS与云上多种产品集成，用户可以使用自己的 CMK 对云上EBS云硬盘、OSS对象存储、RDS关系型数据库进行加密，即可实现云端数据的加密存储。KMS通过完善的技术方案，保障服务的高可用性，并且拥有完善的容灾与备份措施，以保障密钥不会因为不可抗力而丢失。
  
  - 存储加密
  
  云硬盘加密对存储在云硬盘上的数据进行加密，从而保障云硬盘中静态数据的安全性和数据在云主机实例和云硬盘间传输的安全性。
  
  保护存储在对象存储服务（OSS：Object Storage Service）数据中心的磁盘上数据，用户可以对存储空间设置默认加密，从而对其中默认加密生效期间存储的对象进行服务器端加密。在使用服务器端加密时，OSS 将对象保存到其数据中心的磁盘上之前对其进行加密，并在下载对象时对其进行解密。
  
数据库RDS支持使用透明数据加密 (TDE) 来加密运行 Microsoft SQL Server 的数据库实例中存储的数据。TDE会在数据写入存储前自动加密这些数据，并在从存储中读取时自动解密这些数据。数据库文件的加密在页级别执行，已加密数据库中的页在写入磁盘之前会进行加密，在读入内存时会进行解密。

- 存储备份

京东云的存储容灾服务为弹性云服务器、云硬盘和专属存储等服务提供容灾能力，通过存储复制、数据冗余和缓存加速等多项技术，为用户存储数据提供可跨区域复制功能并实时同步到指定区域，实现数据异地容灾，从容应对极端灾难并保证业务流畅，为重要数据加上多重保险。

数据备份服务拥有完善的数据备份机制，支持自动备份和手动备份，每个实例默认每天自动备份一次，也可以根据业务情况随时创建备份，备份文件以三副本的形式保存在京东云对象存储中，无需担心数据丢失。

### 4.3 数据传输

京东云对于数据的交换、转移和分享提供标准的传输加密协议，满足云平台以及系统间传输敏感数据的需求。

- 网络加密传输

针对用户业务混合云部署和全球化布局的场景，可以使用京东云提供的虚拟专用网络（VPN）、云专线服务，实现不同区域之间业务的互联互通和数据传输安全。

 ·  VPN连接利用公网架设专用网络，VPN使用IPSEC、IKE、预共享密钥方式对数据进行加密，基于公网提供安全可靠的通信隧道，实现外部用户内网访问、跨地域内网互通等。
 
 ·  专线服务(Direct Connection)提供高速、安全、稳定的网络接入服务。实现京东云网络与用户的IDC、合作伙伴等网络环境进行内网通信、数据备份及跨机房容灾，为用户提供混合云解决方案。
 
 - 应用加密传输
 
 京东云支持HTTPS安全数据加密传输，并使用传输层安全性 (TLS) 协议，在云服务和用户之间传输数据时提供保护。TLS提供严格的身份验证，消息隐私性和完整性强（允许检测消息篡改、拦截和伪造），具有良好的互操作性，算法灵活，易于部署和使用。
 
 当用户通过互联网提供Web网站业务时，可以使用京东云联合全球知名证书服务商提供的证书管理服务。通过给Web网站申请并配置证书，实现网站的可信身份认证以及基于加密协议的安全传输。
 
### 4.4 数据访问

数据访问是指用户对云端数据的访问。建议用户对数据的访问和传输进行严格的管控及安全防护。为保证数据的合法访问，京东云提供身份鉴别、授权管理、权限鉴别三合一的用户业务访问控制。

 - 访问控制
 
京东云提供了用户身份管理与访问控制服务（Identity and Access Management，IAM）。用户可以通过 IAM 服务创建、管理子用户账号，并控制这些子用户访问京东云资源的权限。

 - SSH密钥
 
对于用户登录使用Linux主机，SSH 服务可以对所有传输的数据进行加密，提供比传统 Telnet服务更高的安全性。而基于密钥认证的 SSH 自动化登录，在保障用户安全性的同时，可以简化登录过程，降低运维成本。

 - 多因素认证
 
MFA (Multi-Factor Authentication) 是一种简单有效的最佳安全实践，它能够在用户名和密码之外再额外增加一层安全保护，并且在京东云进行敏感操作时，进行身份验证防止误删。启用 MFA 后，用户登录京东云时，系统将要求输入用户名和密码，然后要求输入来自其 MFA 设备的6位动态验证码，即使他人盗取用户的密码，也无法登陆用户的账号，多因素的安全认证将最大限度地保障用户的账户安全。

### 4.5 数据使用

数据使用过程中，对其中的敏感数据进行数据脱敏、水印等处理可以确保数据合规使用，并规避信息泄露和法律法规遵从风险。

 - 敏感数据脱敏
 
针对用户敏感数据，采用适当的脱敏算法进行处理，防止敏感数据被滥用和泄露，实现敏感隐私数据的可靠保护。

 - 数据处理服务
 
用户上传文件到对象存储后，京东云提供丰富的数据处理服务，可以在云端实现图片的缩放、裁剪、水印、鉴黄、格式转化和样式管理，视频转码工作流等丰富的数据处理功能，满足各网络场景下多终端设备的访问需求，同时提供数据安全性、透明性、可溯源性。

### 4.6 数据销毁

在用户提出请求和合同终止时，京东云会严格遵循数据销毁标准与用户之间的协议约定，执行用户注销和数据删除。

 - 用户注销
 
京东云账户注销后，用户个人信息会在京东云系统中去除，使其保持不可被检索、访问的状态，或对其进行匿名化处理。根据相关法律规定，相关交易记录须在京东云后台保存一定时间。用户在操作之前，将自行备份京东云账户相关的所有信息和数据。

 - 数据删除

当用户删除数据或离开京东云时，京东云会对指定的数据及其所有副本进行全面的清除，包括删除用户与数据之间的索引关系，并将内存、块存储等存储空间进行清零操作。在一定条件下，对退役的磁性存储设备进行消磁和物理销毁，确保其数据无法恢复。

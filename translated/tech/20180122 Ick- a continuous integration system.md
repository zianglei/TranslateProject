Ick：一个连续集成系统
======

**TL;DR:** Ick 是一个连续集成或者 CI 系统。访问 <http://ick.liw.fi/> 获取跟多信息。

更加详细的版本随后会出

### 首个公开版本发行

世界可能还不需要另一个连续集成系统（CI）但是我需要。我已对我尝试过或者看过的连续集成系统感到不满意了。更重要的是，几样我感兴趣的东西比我所听说过的连续集成系统要强大得多。因此我开始编写我自己的 CI 系统。

我的新个人业余项目叫做 ick。它是一个 CI 系统，这意味着他可以运行自动化的步骤来搭建、测试软件。它的主页是<http://ick.liw.fi/>，[下载][1]页面有导向源码、.deb 包和用来安装的 Ansible 脚本的链接。

我现已发布了首个公开版本，绰号 ALPHA-1，版本号0.23。它现在是 alpha 品质，这意味着它并没拥有所有期望的特性，如果任何一个它已有的特性工作的话，你应该感到庆幸。

### 诚邀英才

Ick 目前是我的个人项目。我希望能让它不仅限于此，同时我也诚邀英才。访问[管理][2]页面查看章程，[开始][3]页面查看如何开始贡献的的小贴士，[联系][4]页面查看如何联络。

### 架构

Ick 拥有一个由几个通过 HTTPS 协议通信使用 RESTful API 和 JSON 处理结构化数据的部分组成的架构。访问[架构][5]页面查看细节。

### 宣言

连续集成（CI）是用于软件开发的强大工具。它不应枯燥、易溃或恼人。它搭建起来应简单快速，除非正在测试、搭建中的码有问题，不然它应在后台安静地工作。

一个连续集成系统应该简单、易用、清楚、干净、可扩展、快速、综合、透明、可靠并推动你的生产力。搭建它不应花大力气、不应需要专门为 CI 而造的硬件、不应需要频繁留意以使其保持工作、开发者永远不必思考为什么某样东西不工作。

一个连续集成系统应该足够灵活以适应你的搭建、测试需求。只要 CPU 架构和操作系统版本没问题，它应该支持各式操作者。

同时像所有软件一样，CI 应该彻彻底底的免费，你的 CI 应由你做主。

（目前的 Ick 仅稍具雏形，但是它会尝试着有朝一日变得完美，在最理想的情况下。）

### 未来的梦想

长远来看，我希望 ick 拥有像下面所描述的特性。落实全部特性可能需要一些时间。

* 多种多样的事件都可以触发搭建。时间是一个明显的事件因为项目的源代码仓库改变了。更强大的是不管依赖是来自于 ick 搭建的另一个项目或则包比如说来自 Debian，任何用于搭建的依赖都会改变：ick 应当跟踪所有安装进一个项目搭建环境中的包，如果任何一个包的版本改变，都应再次触发项目搭建和测试。

* Ick 应该支持搭建任何合理的目标，包括任何 Linux 发行版，任何免费的操作系统，以及任何一息尚存的收费操作系统。

* Ick 应当不需要安装任何专门的代理，就能支持各种它能够通过 ssh 或者串口或者其它这种中性交流管道控制的操作者。Ick 不应默认它可以有比如说一个完整的 Java Runtime，如此一来，操作者就可以是一个微控制器了。

* Ick 应当能轻松掌控一大批项目。我觉得不管一个新的 Debian 源包何时上传，Ick 都应该要能够跟得上在 Debian 中搭建所有东西的进度。（明显这可行与否取决于是否有足够的资源确实用在搭建上，但是 Ick 自己不应有瓶颈。）

* 如果有需要的话 Ick 应当有选择性地补给操作者。如果所有特定种类的操作者处于忙碌中且 Ick 被设置成允许使用更多资源的话，它就应该这么做。这看起来用虚拟机、容器、云提供商等做可能会简单一些。

* Ick 应当灵活提醒感兴趣的团体特别是关于其失败的方面。它应允许感兴趣的团体通过 IRC，Matrix，Mastodon， Twitter， email， SMS 甚至电话和语音合成来接受通知。例如“您好，感兴趣的团体。现在是四点钟您想被通知 hello 包什么时候为 RISC-V 搭建好。”




### 请提供反馈

如果你尝试 ick 或者甚至你仅仅是读到这，请在上面分享你的想法。[联系][4]页面查看如何发送反馈。相比私下反馈我更偏爱公开反馈。但如果你偏爱私下反馈，那也行。

--------------------------------------------------------------------------------

via: https://blog.liw.fi/posts/2018/01/22/ick_a_continuous_integration_system/

作者：[Lars Wirzenius][a]
译者：[tomjlw](https://github.com/tomjlw)
校对：[校对者ID](https://github.com/校对者ID)

本文由 [LCTT](https://github.com/LCTT/TranslateProject) 原创编译，[Linux中国](https://linux.cn/) 荣誉推出

[a]:https://blog.liw.fi/
[1]:http://ick.liw.fi/download/
[2]:http://ick.liw.fi/governance/
[3]:http://ick.liw.fi/getting-started/
[4]:http://ick.liw.fi/contact/
[5]:http://ick.liw.fi/architecture/
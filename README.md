# ShoppingLikeLocal

作者：[atlasharry](https://github.com/atlasharry)。

以小红书使用证据为主，结合B站关键片段、同款价格和送达条件，衔接到按授权购买。适合在中国大陆选购家居、日化、数码等消费品。

第一版包含网页、原生电脑和手机操作后备流程。Skill提供方法和路由，需要宿主已经具备相应控制工具；它本身不提供手机连接服务。

## 能做什么

- 区分具体使用证据与推广信号，核对正文、实物图和评论所指的款式。
- 通过章节、字幕和关键片段了解B站视频，区分口述、画面与观众复验。
- 匹配型号、地区配方、容量、件数和配件，回零售商核实实付总价。
- 比较相同配送地区下的送达承诺，给出现在买或等待的依据及覆盖范围。
- 在网页缺失关键内容时，检测并使用已授权、可交互的手机工具或镜像。
- 沿用用户当前授权核对加购、订单和支付状态。

## 安装

将本仓库目录放入宿主的技能目录。Codex默认位置为：

    ~/.codex/skills/china-shopping-research/

保持SKILL.md、agents和references的相对目录结构。重载技能列表或在新会话调用：

    用 $china-shopping-research 帮我选一款浴室清洁剂，
    主要看小红书和B站，核对京东同款价格与送达，
    最后先加购物车，不付款。

也可以明确指定“仅调研”“包含手机App比价”“预算及最晚送达日期”“按已授权金额购买”等范围。

## 第一版验证状态

本版本完成了一次小红书、B站和京东加购／确认订单流程的案例。手机连接与真机控制尚未在该编写环境验证；全平台零售商结算未全部跑通。按用户选择，案例停在加购，未支付。

当前可用能力由宿主现场检测，不能把案例状态当成未来会话的能力。具体检查见 [validation.md](validation.md)。

## 文件

- [SKILL.md](SKILL.md)：入口与工作流程。
- [来源与视频](references/sources-and-video.md)：推广、评论及视频证据。
- [价格、履约与购买](references/price-delivery-purchase.md)：同款、实付、送达与交易阶段。
- [手机控制](references/mobile-control.md)：设备能力、接入、App操作与交接。
- [证据结构](references/evidence-schema.md)：研究、报价与跨设备记录。
- [匿名案例](examples/bathroom-cleaner.md)：真实调研中的具体错配及加购核验。

## 方法参考与许可

参考了 [xhs-research](https://github.com/kunhai1994/xhs-research) 的查询和争议引用、[easybuy-skill](https://github.com/chen8696/easybuy-skill) 的推广信号维度、[shopping-aggregator](https://github.com/DaizeDong/shopping-aggregator) 的同规格和价格证据，以及 [xiaohongshu-skill](https://github.com/chang-zy/xiaohongshu-skill) 的评论读取范围。

本仓库独立撰写方法，未复制上述项目的代码或完整技能文本，未自动安装其MCP、扩展或采集服务。发布内容采用 [MIT License](LICENSE)。外部网站、第三方资料及其商标仍归各自权利人。

## 第二版扩展

可补充新的零售平台、手机控制后端、历史价来源及排序偏好。定时监测、自动提醒和额外账户接入按用户明确请求另行实施。

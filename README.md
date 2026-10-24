# ShoppingLikeLocal

作者：[atlasharry](https://github.com/atlasharry)、[rsun17](https://github.com/rsun17) · MIT

从当地使用证据出发，核对准确产品、真实报价与送达条件。面向中国及国际购物平台，可通过浏览器、原生电脑或已连接手机继续同一项研究。

ShoppingLikeLocal是研究与执行方法，不是独立采集服务。实际覆盖由宿主工具、登录状态、地区和页面能力决定；支持某种工作流不等于每个平台已经实测跑通。

## 能力

- 小红书、B站及当地社区：阅读原帖和相关评论，区分推广信号、使用证据、共同引用与搬运。
- 参数与版本：核对完整SKU、地区、套装、耗材组合和测试口径，避免拿系列名或广告数字替代具体款式。
- 同款比价：商品身份与卖家报价分开，核本次数量、可用优惠、必要附件、税运费和区域售后。
- 送达比较：统一配送地区，区分发货、到货、安装和付款截止条件。
- 手机接续：验证真实画面与输入，分别记录淘宝、拼多多等App的已完成环节；保留Android及其他后端接入路径。
- 授权执行：研究、加购、提交订单和支付分别核验，沿用当次用户授权。

中国平台通常以小红书体验、B站测试与零售商核价组合开展；Amazon、Temu等市场使用相同记录框架，并补购买国家、币种、税费、进口及地区版本。本版不宣称已经打通全部平台。

## 安装与调用

把完整仓库放入技能目录，目录名与技术标识均为 `shopping-like-local`：

```bash
git clone https://github.com/atlasharry/ShoppingLikeLocal.git ~/.codex/skills/shopping-like-local
```

如果目标目录已有内容，先检查并更新已有安装，不重复克隆或覆盖本地修改。重载技能列表或在新会话使用：

> 用 $shopping-like-local 帮我选一台4000–7000元的客厅投影仪，重点核实小红书使用体验和B站测试，再比较京东、淘宝和拼多多准确款式的含运价格。只调研，不购买。

也可用于简短追问、已选商品比价或其他国家购物。已知国家和偏好不反复询问。

### 从第一版迁移

展示名统一为 **ShoppingLikeLocal**，技术标识由 `china-shopping-research` 改为 `shopping-like-local`。更新安装目录、调用示例和快捷指令后，只保留一个启用版本，避免重复触发。旧名仅用于说明历史迁移，不作为新调用入口。若旧安装目录本身是Git仓库且有关联worktree，先按Git的worktree迁移/修复流程处理，不直接移动后继续依赖失效路径。

## 内容导航

- [SKILL.md](SKILL.md)：入口与研究深度选择。
- [产品与证据](references/product-evidence.md)：准确款式、参数和条件。
- [来源与视频](references/sources-and-video.md)：推广信号、评论覆盖、视频片段。
- [价格与履约](references/price-delivery-purchase.md)：实付、配送和交易阶段。
- [平台与地区](references/platforms.md)：平台差异和能力覆盖。
- [全球与多品类反例](references/expansion-notes.md)：Amazon/Temu、历史比价、床品、印花洗护、直板夹和安装配件的公开资料边界。
- [手机控制](references/mobile-control.md)：接入、输入回读、恢复和交接。
- [记录约定](references/evidence-schema.md)：产品、主张、报价和访问状态。
- [验证记录](validation.md)、[离线评测](evals/README.md)：区分格式、离线和真实操作证据。
- [24个并行工作包](evals/results/parallel24/summary.md)：公开调查、品类反例及独立审查，保留中间评分而非只报最好结果。
- [投影仪报告](examples/living-room-projector.md)、[便携游戏本报告](examples/portable-gaming-laptop.md)、[真实平台覆盖](examples/platform-validation-2026-10-22.md)。
- [拼多多手机补验](examples/mobile-comparison-2026-10-23.md)：两个真实选款、报价及配送对比，含系列起价和拆封商品的处理。
- [百元内舒适耳机实测流程](examples/comfortable-earphones-under-100.md)：需求帖与部分评论、视频抽看、京东与淘宝官方同款核价及重庆配送，明确保留未完成项。
- [本轮Review](REVIEW.md)：改动、方法参考、评测结果和发布缺口。
- [第一版清洁剂案例](examples/bathroom-cleaner.md)：历史匿名案例，价格不代表现在。

## 方法参考与许可

本项目独立撰写。方法参考包括 [xhs-research](https://github.com/kunhai1994/xhs-research)、[xiaohongshu-skill](https://github.com/chang-zy/xiaohongshu-skill)、[shopping-aggregator](https://github.com/DaizeDong/shopping-aggregator) 和 [easybuy-skill](https://github.com/chen8696/easybuy-skill)；评测参考 [Agent Skills](https://agentskills.io/skill-creation/evaluating-skills)。没有复制整套技能或引入默认返佣配置。

聚合商品API可提供线索，但不能替代登录账号的实付和配送，也不能把商品库当作原帖评论。第三方代码、服务及依赖链的许可证单独核对，MIT仅适用于本仓库自有内容。手机镜像和控制后端不是本仓库附带服务。

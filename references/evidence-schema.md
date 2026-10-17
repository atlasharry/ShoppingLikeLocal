# 证据表与交接

按实际任务采用表格、CSV或结构化文件，不必为简单问题创建全部字段。用户要求完整调研、多人协作或跨设备时，保留能恢复工作的记录。

## 研究简要

用途与场景、硬约束、预算、数量、配送地区、最晚需要时间、已回答信息、允许平台与工具、当前购物授权、尚缺条件。

## 一条使用主张

    source_url
    platform
    query
    published_at
    observed_at
    author
    product_variant
    use_conditions
    claim
    evidence_type: author_said | image_observed | video_observed | user_replication
    video_time_range
    continuous_or_sampled
    comments_read_scope
    unexpanded_replies
    promotion_signals
    independent_source_group
    supports
    contradicts
    material_limitations

只填实际取得的信息，缺项明确未知。不要为了填字段推断用量、持续时间或商业关系；短摘录和必要事实足够，不保存整篇转载。

## 一条可购买报价

    platform
    product_url
    observed_at
    exact_variant
    seller
    fulfiller
    quantity
    listed_price
    usable_discounts_and_conditions
    shipping_and_tax
    checkout_total
    price_stage: listing | cart | checkout | paid
    destination_scope
    ships_by
    estimated_arrival
    order_deadline
    history_window_and_variant_match
    coverage_and_unknowns

价格、物流时段和历史数据分别标注核验范围。不能把聚合记录填进paid，不能用发货时长填estimated_arrival。

## 跨设备交接

保留当前访问路线、目标App或页面、已登录状态、产品键、已选规格、读取范围、比较结果、待解决问题和下一步。手机另记设备别名、操作后端、能力状态及最近一次可逆输入验证。卡住时让接手者知道停在哪个可见环节，不仅记录“失败”。

在宿主提供的安全会话内使用当前链接或标签句柄；公开版本去除Cookie、xsec_token、xsec_source、追踪与会话参数。不要把私有链接、账户资料、完整地址、支付资料或订单号作为公开恢复上下文。

## 输出与验收

推荐及理由；匹配与未匹配的硬约束；同款价格和送达表；关键正反证据；购买时机；实际购物阶段。来源不足会影响关键决策时才注明限制，并说明对选择的影响。

验证状态分别记录：格式校验、离线场景、真实网页、真实手机、真实订单、实际支付。一个阶段通过不能替代另一个阶段。

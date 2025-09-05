# hlm-miner 分配器记录存储库

## 分配器 JSON 链接

[hlm-miner 分配器 JSON](https://github.com/filecoin-project/Allocator-Registry/blob/main/Allocators/recLhrJ8U6TbIpbwp.json)

## 客户端尽职调查

hlm-miner 通过严格的流程验证客户端并建立信任：

- **申请流程**：客户端通过安全门户提交正式申请，需包含：
  - 法人实体名称、注册信息和联系方式。
  - 数据集描述（类型、规模、预期用途）。
  - 数据所有权或许可证明（例如证书、合同、同意书）。
- **验证**：
  - 使用第三方 KYC 服务（例如 Onfido、Jumio）确认法人实体身份及授权代表。
  - 通过公共记录和网络搜索进行背景调查，确保无之前的法律或道德问题。
  - 在 [datacapstats.io](https://datacapstats.io/) 上交叉核查客户端信息，检测重复或可疑申请。
- **初始信任**：
  - 为每位客户端分配唯一 ID，用于在 [datacapstats.io](https://datacapstats.io/) 和 [GitHub](https://github.com/Acumes/hlm-miner-bookkeeping) 日志中跟踪。
  - 客户端需签署协议，承诺遵守数据法律（例如 GDPR、CCPA、PIPL）和计划规则。
  - 初始 DataCap 分配上限为 0.5 PiB，后续分配（最高 1 PiB）基于使用情况和合规性。
- **防范 Sybil 攻击**：
  - 速率限制：每法人实体或 IP 地址每 30 天限提交 1 次申请。
  - 确定性检查：交叉核查客户端 ID、钱包地址和数据集元数据；要求唯一数据集指纹（例如加密哈希）。
  - 智能合约标记匹配的钱包地址或数据集哈希。
  - 在达到多样性目标（10+ 客户端）之前，单一客户端不得获得超过总 DataCap 的 10%（初始 0.5 PiB）。
  - 每月随机审计 10% 的申请，检测 Sybil 模式。
- **企业/付费客户端**：需提供公司章程、数据获取协议、第三方审计、直接访谈和财务记录验证。
- **拒绝标准**：拒绝未验证所有权、盗版内容或违反法律的数据集。
- **审计证据**：
  - 安全数据库存储客户端申请、KYC 结果和合规记录。
  - 匿名化日志发布在 [GitHub](https://github.com/Acumes/hlm-miner-bookkeeping) 上。
  - 每季度发布审计摘要，详细说明验证的客户端数量、拒绝情况和 Sybil 尝试，治理团队可通过只读审计门户访问。

## 数据尽职调查

hlm-miner 确保数据集符合计划范围、法律合规性和客户端所有权：

- **计划范围**：
  - 数据集需为公共或私有，符合网络目标（例如科学、档案、媒体、开源），并支持多样性（5+ 数据集类型、10+ 客户端、≥4 个地区）。
  - 客户端提交数据集描述（类型、规模、用途、来源、所有权证明）。
  - 审查数据集以确保多样性（单一数据集类型占 DataCap 比例 <50%）和网络价值；拒绝低质量或无关数据。
- **法律合规性**：
  - 要求文档：
    - 公共数据集：开源许可（例如 CC0、MIT）或公共领域确认。
    - 私有数据集：合同、同意书或数据创建记录。
    - 敏感数据集：符合 GDPR、CCPA、PIPL、HIPAA 要求。
  - 法律专家审查高风险数据集（例如医疗、金融）。
  - 验证存储提供商（SP）的处理协议（例如加密）符合地区法律。
  - 每月审计 10% 的活跃数据集。
- **所有权验证**：
  - 通过来源 URL、许可、数据创建记录或第三方审计验证所有权。
  - Filecoin 内容标识符（CID）验证数据集完整性和所有权。
  - 企业客户端的声明与外部记录交叉核查。
- **数据抽样**：
  - 每月随机抽样：抽取每个客户端 DataCap 的 10%（例如每 0.5 PiB 抽样 0.05 PiB）。
  - 每季度分层抽样：涵盖所有数据集类型和地区。
  - 使用加密哈希（例如 SHA-256）验证数据集类型、规模和完整性。
- **工具**：
  - [Datacapstats.io](https://datacapstats.io/)：跟踪交易元数据并验证客户端声明。
  - Go-swan-client/Lotus：验证交易提案并提取样本数据。
  - Filecoin CID：确认数据集完整性。
  - 第三方工具（例如 Chainalysis）验证区块链或敏感数据。
- **审计证据**：
  - 安全数据库存储数据集描述、所有权证明和抽样结果。
  - 匿名化审计追踪发布在 [GitHub](https://github.com/Acumes/hlm-miner-bookkeeping) 上。
  - 每季度报告详细说明验证的数据集、抽样结果和合规问题，治理团队可通过安全审计门户访问。
- **不合规处理**：拒绝未验证所有权或违反法律的数据集；重复交易不匹配将导致 DataCap 暂停。

## 客户端通道简述

hlm-miner 提供安全、透明的 DataCap 分配通道，注重法律合规性、数据集多样性和高检索率。我们通过严格的 KYC、所有权验证和持续审计，确保信任和全球法规（例如 GDPR、CCPA）的遵守。支持多样化数据集（科学、媒体、开源）并覆盖多个地区，hlm-miner 是寻求可靠、去中心化 Filecoin 存储的客户端的理想选择。

## 联系方式

- **邮箱**： [finance@grandhelmsman.com](mailto:finance@grandhelmsman.com)
- **Slack**： acumes

## 详细分配器政策、流程和要求

在 [GitHub](https://github.com/Acumes/hlm-miner-bookkeeping) 上发布的 hlm-miner 政策涵盖：

- **客户端尽职调查**：KYC、所有权验证、通过速率限制、确定性检查和审计防范 Sybil 攻击。
- **数据尽职调查**：范围验证、法律合规性、所有权检查、每月随机抽样和每季度分层抽样，使用 [datacapstats.io](https://datacapstats.io/)、go-swan-client 和 CID。
- **报告**：每两月 RSR、每月利用率和每季度多样性报告，包含合规详情。
- **后果**：不合规将导致 DataCap 暂停。
- **更新**：根据治理团队反馈更新政策，确保透明度。

## 风险缓解策略

hlm-miner 通过以下措施保护其通道：

- **运营安全（OpSec）**：安全申请门户、加密记录、第三方 KYC。
- **用户协议**：签署遵守数据法律和计划规则的承诺。
- **限制/警报**：智能合约标记重复申请；速率限制每实体/IP 每 30 天限一次提交。
- **审计**：每月 10% 随机审计和每季度全面审查，检测滥用或 Sybil 尝试。
- **声誉评分**：优先考虑有可验证记录的客户端。
- **后果**：不合规客户端将面临 DataCap 暂停。

## 争议解决

- **内部争议**：客户端可向 [finance@grandhelmsman.com](mailto:finance@grandhelmsman.com) 提交问题。合规团队在一周内使用 [datacapstats.io](https://datacapstats.io/) 数据进行审查。不合规客户端收到警告；未解决问题将导致 DataCap 暂停。
- **外部争议**：对于与其他分配器或治理团队的冲突，hlm-miner 提供审计追踪（客户端 ID、数据集元数据、合规记录），通过 [GitHub](https://github.com/Acumes/hlm-miner-bookkeeping) 和安全审计门户。争议在两周内解决，必要时升级至治理团队。
- **透明度**：所有争议和解决情况记录在 [GitHub](https://github.com/Acumes/hlm-miner-bookkeeping) 上。

## 合规审计检查

hlm-miner 通过以下方式确保合规：

- **客户端验证**：分配前进行 KYC、所有权和法律文档检查。
- **SP 合规性**：SP 的数据处理协议（例如加密）符合地区法律。
- **数据尽职调查**：每月 10% 抽样和每季度审计，使用 [datacapstats.io](https://datacapstats.io/) 和 Filecoin 工具验证范围、合法性和所有权。
- **报告**：每两月 RSR、每月利用率和每季度多样性报告在 [GitHub](https://github.com/Acumes/hlm-miner-bookkeeping) 上包含合规摘要。
- **审计**：每月 10% 随机审计客户端/SP，治理团队通过安全门户访问加密记录。
- **后果**：不合规的客户端/SP 将面临 DataCap 暂停，直到问题解决。

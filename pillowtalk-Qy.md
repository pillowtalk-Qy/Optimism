---
timezone: Asia/Shanghai
---

> 请在上边的 timezone 添加你的当地时区，这会有助于你的打卡状态的自动化更新，如果没有添加，默认为北京时间 UTC+8 时区
> 时区请参考以下列表，请移除 # 以后的内容

timezone: Pacific/Honolulu # 夏威夷-阿留申标准时间 (UTC-10)

timezone: America/Anchorage # 阿拉斯加标准时间 (UTC-9)

timezone: America/Los_Angeles # 太平洋标准时间 (UTC-8)

timezone: America/Denver # 山地标准时间 (UTC-7)

timezone: America/Chicago # 中部标准时间 (UTC-6)

timezone: America/New_York # 东部标准时间 (UTC-5)

timezone: America/Halifax # 大西洋标准时间 (UTC-4)

timezone: America/St_Johns # 纽芬兰标准时间 (UTC-3:30)

timezone: America/Sao_Paulo # 巴西利亚时间 (UTC-3)

timezone: Atlantic/Azores # 亚速尔群岛时间 (UTC-1)

timezone: Europe/London # 格林威治标准时间 (UTC+0)

timezone: Europe/Berlin # 中欧标准时间 (UTC+1)

timezone: Europe/Helsinki # 东欧标准时间 (UTC+2)

timezone: Europe/Moscow # 莫斯科标准时间 (UTC+3)

timezone: Asia/Dubai # 海湾标准时间 (UTC+4)

timezone: Asia/Kolkata # 印度标准时间 (UTC+5:30)

timezone: Asia/Dhaka # 孟加拉国标准时间 (UTC+6)

timezone: Asia/Bangkok # 中南半岛时间 (UTC+7)

timezone: Asia/Shanghai # 中国标准时间 (UTC+8)

timezone: Asia/Tokyo # 日本标准时间 (UTC+9)

timezone: Australia/Sydney # 澳大利亚东部标准时间 (UTC+10)

timezone: Pacific/Auckland # 新西兰标准时间 (UTC+12)

---

# {Qy}

1. 自我介绍：我是Qy

2. 你认为你会完成本次残酷学习吗？会的

## Notes

<!-- Content_START -->

### 2025.01.06

1.在 Bedrock 中，sequencer 确实有一个内存池，类似于以太坊的 L1，但内存池是私有的，以避免为 MEV 提供机会。在 OP 主网中，每两秒生成一次区块，无论它们是空的（没有交易）、用交易填充到区块 gas 限制，还是介于两者之间。
交易通过两种方式到达排序器：
a.交易直接提交给排序器。这些交易的提交成本要低得多，因为它们不需要单独的 L1 交易。然而，它们无法抗审查，因为排序器是唯一知道它们的参与者。
b.在 L1 上提交的交易（称为存款）包含在相应的 L2 块中的链中。每个 L2 块都由“纪元”（它对应的 L1 块，通常在 L2 块之前几分钟发生）及其在该纪元内的序列号标识。纪元的第一个块包括它对应的 L1 块中发生的所有存款。如果序列器试图忽略合法的 L1 交易，它最终会得到与验证者不一致的状态，就像序列器试图通过其他方式伪造状态一样。这为 OP Mainnet 提供了 L1 以太坊级别的审查阻力。

2.Optimism 的设计目的是让用户可以在 L2（OP Mainnet、OP Sepolia 等）和底层 L1（以太坊主网、Sepolia 等）上的智能合约之间发送任意消息。这使得在两个网络之间转移 ETH 或代币（包括 ERC20 代币）成为可能。这种通信发生的确切机制因消息发送的方向而异。OP Mainnet 在标准桥中使用此功能，允许用户将代币从以太坊存入 OP Mainnet，并允许将相同的代币从 OP Mainnet 提取回以太坊。在 Optimism 术语中，从以太坊（L1）到 OP 主网（L2）的交易称为存款。您使用L1CrossDomainMessenger或者L1StandardBridge。存款交易在与存款发生的 L1 块对应的“纪元”的第一个 L2 块中成为规范区块链的一部分。此 L2 块通常会在相应的 L1 块之后几分钟创建。

3.故障证明
在 Optimistic Rollup 中，状态承诺会发布到 L1（OP 主网的情况下为以太坊），而无需任何直接证明这些承诺的有效性。相反，这些承诺在一段时间内（称为“挑战窗口”）被视为待定。如果提议的状态承诺在挑战窗口期间（目前设置为 7 天）没有受到质疑，则该承诺被视为最终承诺。一旦承诺被视为最终承诺，以太坊上的智能合约就可以安全地接受基于该承诺的有关 OP 主网状态的提款证明。
当国家承诺受到质疑时，可以通过“过错证明”（以前称为“欺诈证明”）使其无效) 流程。如果成功挑战了承诺，则将其从列表中移除，StateCommitmentChain最终由另一个提议的承诺替换。需要注意的是，成功的挑战不会回滚 OP Mainnet 本身，只会回滚已发布的有关链状态的承诺。交易的顺序和 OP Mainnet 的状态不会因故障证明挑战而改变。

### 2024.01.06

### 2025.01.07

笔记内容

### 2024.01.07

### 2025.01.08

笔记内容

### 2024.01.08

### 2025.01.09

笔记内容

### 2024.01.09

### 2025.01.10

笔记内容

### 2024.01.10

### 2025.01.11

笔记内容

### 2024.01.11

### 2025.01.12

笔记内容

### 2024.01.12

### 2025.01.13

笔记内容

### 2024.01.13

### 2025.01.14

笔记内容

### 2024.01.14

### 2025.01.15

笔记内容

### 2024.01.15

### 2025.01.16

笔记内容

### 2024.01.16

### 2025.01.17

笔记内容

### 2024.01.17

<!-- Content_END -->

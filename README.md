# 一. 门限签名

门限签名是一种分布式多方签名协议，包含有分布式密钥生成，签名和验签算法。其允许多个参与方联合生成合法的签名而不需要生成私钥，同时任何人都能对签名进行认证。这种去中心化的签名方式非常适合应用于区块链等领域。近几年，伴随区块链技术的快速发展，门限签名算法在学术研究和商业应用中获得广泛关注。

因为区块链技术和签名算法之间紧密而又重要的连结，签名算法的发展和新范式的引入都将直接影响区块链网络的特性和效率。另外，由分布式账本激发的机构和个人账户密钥管理需求也催生了诸多钱包应用，这种改变甚至波及到传统企业。

无论在区块链还是传统金融机构中，门限签名方案都可带来多种场景下的安全性和隐私性提升。门限签名方案具有如下所示的通用算法模型：

- 密钥生成：所有参与者联合在一起，执行两件事情： 1）为每一个参与者生成一个私钥的秘密份额；2）参与者根据自己所拥有的私钥的秘密份额共同计算出与秘密私钥对应的公钥。

- 签名算法：参与某次签名的参与方分别将自己的私钥的秘密份额作为隐私输入，需要签名的信息作为公共输入，进行一次联合签名运算，得到签名。在这个过程中，门限签名的隐私性保证了参与方并不能获得其他方的私钥信息，但都可以得到秘密私钥的合法签名。正确性和健壮性保证了签名的不可伪造。

- 验签算法：利用对应于秘密私钥的公钥，按照传统签名算法的验签方式即可完成对联合签名的验证。在验签过程中，不涉及秘密信息，因此，任何人（拥有公钥）都能对签名进行验证。

总之，门限签名 (Threshold Signatures, TSS) 在区块链等领域具有重大的发展和应用的潜力，值得我们去深入的研究。

下面是关于 TSS 的学习资料，仅供参考。

# 二. 阅读材料

## 2.1 Papers

* [The Elliptic Curve Digital Signature Algorithm (ECDSA) ](https://link.springer.com/article/10.1007/s102070100002)
* [The Security of DSA and ECDSA](https://link.springer.com/chapter/10.1007/3-540-36288-6_23)
* [Fast Multiparty Threshold ECDSA with Fast Trustless Setup](https://eprint.iacr.org/2019/114.pdf)
* [Threshold ECDSA from ECDSA Assumptions: The Multiparty Case](https://ieeexplore.ieee.org/abstract/document/8835354)
* [Fast Threshold ECDSA with Honest Majority](https://dl.acm.org/doi/abs/10.1145/3243734.3243859)
* [One Round Threshold ECDSA with Identifiable Abort](https://eprint.iacr.org/2020/540.pdf)
* [Threshold-Signatures-whitepaper-nchain](https://nakasendoproject.org/Threshold-Signatures-whitepaper-nchain.pdf)
* [Hierarchical Threshold Secret Sharing](https://www.openu.ac.il/lists/mediaserver_documents/personalsites/tamirtassa/hss_conf.pdf)
* [(扩展阅读) Blazing Fast OT for Three-Round UC OT](https://eprint.iacr.org/2020/110.pdf)
* (WhitePaper) https://github.com/ZenGo-X/gotham-city/blob/master/white-paper/white-paper.pdf

## 2.2 Github repos

* (Rust) https://github.com/cryptochill/tss-ecdsa-cli
* (Rust) https://github.com/ZenGo-X/multi-party-ecdsa
* (C++) https://github.com/unboundsecurity/blockchain-crypto-mpc
* (Go) https://github.com/coinbase/kryptology
* (Go) https://github.com/bnb-chain/tss-lib
* (Go) https://github.com/getamis/alice

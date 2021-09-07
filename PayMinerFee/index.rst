USDT 矿工费代付功能
====================

USDT 是由 Tether 发行的基于美元的稳定币代币（Token），当前主要活跃在如下几条公链上：

- 以太坊（ETH）：  USDT-ERC20
- 波场（TRX）   ：  USDT-TRC20
- 比特币（BTC）：  USDT-Omni


由于区块链的特性，在各条链上发送 USDT 时，都需要支付小额的 ETH/TRX/BTC 作为矿工费，这对于小白用户来说理解和使用门槛都很高。


为了方便用户的使用，比特派专门设计了矿工费代付功能，在用户发币时自动的完成矿工费的代付，让用户无需理解 ETH/TRX/BTC 就能轻松发送 USDT，这样用户钱包里只要有 USDT 就能发送了，无需再额外准备 ETH/TRX/BTC 等数字货币，发送时会自动扣除 USDT 作为矿工费，用户理解起来会非常容易。

该功能的实现方式是比特派会从官方矿工费支付地址将 ETH/TRX/BTC 发送到用户地址，然后用户会将作为矿工费的 USDT 发送到比特派官方 USDT 接收地址，然后再将要发送的 USDT 发送给目的地址，这些步骤都是自动完成的，对于用户来说看起来就是只做了一笔发送 USDT 的操作。

由于该功能需要构造多笔交易，因此耗费的矿工费会高于直接用 ETH/TRX/BTC 作为矿工费的成本，针对这种情况，我们还设计了加油包的功能，用户可以在发币时选择代付一笔交易的矿工费，还是代付多笔交易的矿工费，代付多笔时相关成本就能平摊，平均成本就能降低到比较合理的水平。

矿工费代付功能及加油包选项的钱包界面截图参见图1和图2。



..  image:: ../img/pay_miner_fee_1.jpg
    :scale: 50%
    :align: center

..  image:: ../img/pay_miner_fee_2.jpg
    :scale: 50%
    :align: center

USDT-ERC20 矿工费代付功能视频：https://v.qq.com/x/page/a325377sh38.html

USDT-TRC20 矿工费代付功能视频：https://v.qq.com/x/page/u32535clb5z.html


当前我们用于提供矿工费代付功能的 ETH 地址如下：
- `0xf64edd94558ca8b3a0e3b362e20bb13ff52ea513 <https://etherscan.io/address/0xf64edd94558ca8b3a0e3b362e20bb13ff52ea513>`_ （etherscan 上标注为 Bitpie: Bitpie 1）
- `0x5c9f3fff6ee846a83080f373f8cea1451bb4a3d9 <https://etherscan.io/address/0x5c9f3fff6ee846a83080f373f8cea1451bb4a3d9>`_ （etherscan 上标注为 Bitpie: Bitpie 2）
- `0x8979d1e0ecab3cf5ae8a5a7b2d792aa119f34be1 <https://etherscan.io/address/0x8979d1e0ecab3cf5ae8a5a7b2d792aa119f34be1>`_ （etherscan 上标注为 Bitpie: Bitpie 3）
- `0x346b46826be175c943a45cdbec2e9d95dc52fb38 <https://etherscan.io/address/0x346b46826be175c943a45cdbec2e9d95dc52fb38>`_ （etherscan 上标注为 Bitpie: Bitpie 4）
- `0xb685d0daea607fe75e02c1a7679261eac661b9bc <https://etherscan.io/address/0xb685d0daea607fe75e02c1a7679261eac661b9bc>`_ （etherscan 上标注为 Bitpie: Bitpie 5）
- `0xadef6b2c5e848a4f04145ee88f20ac079f17beab <https://etherscan.io/address/0xadef6b2c5e848a4f04145ee88f20ac079f17beab>`_ （etherscan 上标注为 Bitpie: Bitpie 6）


当前我们用于提供矿工费代付功能的 TRX 地址如下：
- `TMuPWRhYxXvL2PSyiaKhASefaCv5daiRHK <https://tronscan.io/#/address/TMuPWRhYxXvL2PSyiaKhASefaCv5daiRHK>`_ （tronscan 上标注为 Bitpie1）
- `TJKTuEuJSwdJpz8oeDpLTh9VniWrUeZzdZ <https://tronscan.io/#/address/TJKTuEuJSwdJpz8oeDpLTh9VniWrUeZzdZ>`_ （tronscan 上标注为 Bitpie2）
- `TFBVumaHsaJm2ea8JFaa3yjFL1geLQXiEj <https://tronscan.io/#/address/TFBVumaHsaJm2ea8JFaa3yjFL1geLQXiEj>`_ （tronscan 上标注为 Bitpie3）
- `TXuv9XdcizJ62whVqYxFdA6sByzzKhx6Bw <https://tronscan.io/#/address/TXuv9XdcizJ62whVqYxFdA6sByzzKhx6Bw>`_ （tronscan 上标注为 Bitpie4）

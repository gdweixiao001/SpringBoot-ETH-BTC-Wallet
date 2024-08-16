<p align="center">
 	    <img src="https://img.shields.io/badge/助记词-碰撞器-brightgreen.svg">
      <img src="https://img.shields.io/badge/密钥-碰撞器-brightgreen.svg">
      <img src="https://img.shields.io/badge/助记词-破解-green.svg">
      <img src="https://img.shields.io/badge/助记词-找回-green.svg">
      <img src="https://img.shields.io/badge/BTC助记词-碰撞器-blue.svg">
      <img src="https://img.shields.io/badge/ETH助记词-碰撞器-blue.svg">
 </p>

**演示地址**

　　　　在线体验：<a href='http://eth.wechatqun.cn' target="_blank" >[http://insc.wechatqun.cn](http://eth.wechatqun.cn) </a>

## 实现原理
**密钥碰撞系统实现原理**
1. 动态钱包地址监控
我们的系统定期从Oklink平台获取最新的交易数据，自动筛选并提取交易中使用的钱包地址。这些地址随后被添加到我们的监控钱包数据库中，以便于进一步的分析和跟踪。

2. 地址与密钥生成
利用BIP39标准助记词，系统能够随机生成钱包地址及其对应的私钥。这一过程确保了地址和密钥的随机性和安全性，为后续的密钥碰撞检测提供了基础。

3. 布隆过滤器集成
生成的监控钱包地址被集成到布隆过滤器中。布隆过滤器是一种高效的数据结构，用于检测一个元素是否在一个集合中。在我们的系统中，它被用来快速判断一个地址是否已经被监控。

4. 地址存在性检测
当系统通过BIP39生成新的钱包地址后，它会立即在布隆过滤器中进行查询，以检查该地址是否已经存在于我们的监控列表中。

5. 碰撞检测与通知
如果布隆过滤器检测到地址已经存在，这意味着发生了密钥碰撞。在这种情况下，系统会自动触发一个通知机制，通过短信等方式立即通知相关用户，确保他们能够及时采取行动。

### 界面展示

##### 首页页面

<img src="https://ai.oss.mj.ink/chatgpt/eth/sy.png" />

##### 钱包地址页面

<img src="https://ai.oss.mj.ink/chatgpt/eth/qbdz.png" />
<img src="https://ai.oss.mj.ink/chatgpt/eth/qbdz2.png" />

##### 监控地址页面

<img src="https://ai.oss.mj.ink/chatgpt/eth/jkdz.png" />


## 合作（广告勿扰）：
    
 <div align=center >
    <td ><img height="350" width="250" src="https://ai.oss.mj.ink/chatgpt/insc/wx.jpg"/></td>
 </div>

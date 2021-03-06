# SM4CCM

1、SM4算法与MAC结合诞生了GCM，CCM等高级模式。该脚本是SM4CCM。
CCM是Cipher Block Chaining Message Authentication Code (CBC-MAC)和Counter模式（CTR）的组合。可以同时生存认证信息和对数据加密。CCM广泛用于互联网和物联网中对传输数据进行保护，比如WiFi安全中的WPE协议，它就使用了AES-CCM模式

2、相关资料

资料参考 rfc3610

3、输入参数要求

| 数据项            | 输入参数要求                                                 |
| ----------------- | ------------------------------------------------------------ |
| 原文数据HEX       | 输入需要加密的原文数据，格式为HEX格式，可以为空              |
| 密钥HEX(32)       | 密钥的长度是32个<br/>密钥是一种参数，它是在明文转换为密文或将密文转换为明文的算法中输入的参数。 |
| IV向量HEX(13-26)  | IV格式为HEX格式，长度最少14个最大不超过26个。<br/>IV本质上是一个noce，即在指定上下文中唯一的一个值。<br/>在密码学的领域里，初始向量（英语：initialization vector，缩写为IV），或译初向量，又称初始变量（starting variable，缩写为SV)，是一个固定长度的输入值。一般的使用上会要求它是随机数或伪随机数（pseudorandom）。使用随机数产生的初始向量才能达到语义安全（消息验证码也可能用到初始向量），并让攻击者难以对原文一致且使用同一把密钥生成的密文进行破解。在区块加密中，使用了初始向量的加密模式被称为区块加密模式。 |
| 附加认证数据      | 附加认证数据格式为HEX格式，可以为空，最大长度小于264个，这些附加数据经过身份验证但未加密，并且不包括在此模式的输出中。它可用于验证明文数据包报头或影响消息解释的上下文信息。 |
| SM4CCM加密结果HEX | SM4CCM将数据加密后的结果，格式为HEX格式                      |
| SM4CCM解密结果HEX | SM4CCM将数据解密后的原文，格式为HEX格式                      |

4、功能演示

| 数据项            | 测试参数内容                                                 |
| ----------------- | ------------------------------------------------------------ |
| 原文数据HEX       | FEDCBA98765432100123456789ABCDEF                             |
| 密钥HEX(32)       | 0123456789ABCDEFFEDCBA9876543210                             |
| IV向量HEX(13-26)  | 0123456789ABCDEFFEDCBA9876543210                             |
| 附加认证数据      | 0123456789ABCDEFFEDCBA9876543210                             |
| SM4CCM加密结果HEX | 3AA9F2DA912421A3E371BC5E526A9D8972E1541FDEA1A0D28B0C3DFE9EEA96D9 |

根据上述测试数据，点击商用密码应用与检测工具箱中“SM4CCM加密结果HEX"、 “SM4CCM解密结果HEX”按钮，会计算出相应结果，同时右侧会显示出该过程的输入输出参数及计算结果，可见下图所示：

![SM4CCM](../image/SM4CCM.png)




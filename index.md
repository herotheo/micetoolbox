---
layout: home
---

商用密码应用与检测工具箱集成网络上大部分的密码类工具，并且还支持网络上密码类工具中没有的算法和功能，全部符合国家标准，操作简单快捷。

## 适用范围

用于密码设备选型阶段的产品确认；软件设计阶段的安全架构设计；开发阶段工程师接口调试；测试阶段对密码模块功能、接口和数据的分析测试；协助密码工程师进行流量深度分析；协助安全工程师进行数据识别、分析、破解；还可用于了解密码基础知识、密码应用、密码协议，并做为日常工作、学习、竞赛等的辅助工具。

## 与互联网工具的不同

#### 互联网工具

1. 在互联网上搜集的140款密码类软件或在线工具，90%没有准确描述其输入参数的格式要求。70%在100轮重复测试中包含错误的结果输出。50%仅在特定格式的输入时有效。
2. 互联网工具在使用过程中存在数据伪造、泄漏等安全问题。
3. 功能普遍单一，无法用于复杂的密码分析、网络场景中。
4. 标准不统一，不同的工具检测出的结果不一样。

#### 商用密码应用与检测工具箱

1. 国密算法的支持，如SM1、SM2、SM3、SM4、SM9、SSF33、ZUC。
2. 基于密码算法，流量分析和数据分析的融合，实现交叉引用，快速分析。
3. 程序包括规范的参数定义，标准的输入输出格式，丰富的功能选项，全面的算法支持，并经过大量的计算结果验证。
4. 流量分析支持数据包导入分析和实时监听分析，可自动绘制网络拓扑图、会话重组、协议分析、鉴别信息识别和破解、文件提取等。
5. 流量分析可以进行动态密码分析，并将密码运算过程还原、结合密码数据上下文关联分析，并解决增加相应功能后的性能降低问题。
6. 数据分析支持文件内容分析、数据格式分析、数据类型推测。

## 模块功能介绍

* #### 密码应用

  1. 基础算法

     > 对称密钥算法、分组密码的模式、非对称密钥算法、哈希算法、消息认证码MAC、签名验签等

  2. 应用场景

     > 密钥协商、秘密共享、密码协议、数字信封、口令加密、密码文件、时间戳协议、JWT解析、证书操作等。

  3. 周边功能

     > 编码算法、压缩算法、格式转换、Padding填充算法、ASN.1抽象语法标记的数据解析、OID对象标识符的识别、TLV 格式解析等。

  4. 客户端模拟器

     > TLS客户端模拟与检测、SSH客户端模拟与检测、WireGuard模拟与检测、SFTP模拟与检测等。

* #### 流量分析

  1. 流量导入

     > 支持直接抓包或数据包导入的方式。直接抓包支持包过滤语法，支持混杂模式；支持流量动态分析。

  2. 分析插件

     > 通过勾选分析插件的方式进行流量分析，已有的插件包括文件提取插件，鉴别信息提取插件，协议分析插件等

  3. 展示插件

     > 支持分析结果的图形化展示功能，如自动化绘制网络拓扑图，会话自动分组展示，文件内容展示，鉴别信息列表展示等。

  4. 关联分析

     > 支持分析结果关联分析功能，如涉及密码应用功能的信息可直接关联密码应用模块，涉及数据分析功能的信息可直接关联数据分析模块

* #### 数据分析

  1. 数据格式

     > 支持密码应用的各种数据格式的分析功能，OID信息翻译，数据类型猜测（后续提供）等。

  2. 文件格式

     > 支持对文件哈希分析，文件格式分析，文件格式转换等日常功能。

  3. 分组分析

     > 支持将同类型或关联类型的数据分析功能合并执行。便于快速确定数据类型，缩小分析范围。

  4. 帮助信息

     > 工具箱中包含大量的参考资料，标准文件，对于了解密码应用，了解数据定义等，帮助很大。

## 部署方式

程序支持灵活的部署方式，包括单机模式和C/S模式。单机模式在授权的电脑中运行。C/S模式支持脱机使用。

![部署](image/部署-16484510463671.png)

## Code highlight

The code highlight style is configurable the following entry in `_config.yaml`:

```yaml
syntax_highlighter_style: colorful
```

The default code highlight style is `colorful`, the full supported styles can be found from [the rouge repository][6]. Customized
style can be added to [./gitbook/rouge/](./gitbook/rouge/).

## How to generate TOC

The jekyll-gitbook theme leverages [jekyll-toc][4] to generate the *Contents* for the page.
The TOC feature is not enabled by default. To use the TOC feature, modify the TOC
configuration in `_config.yml`:

```yaml
toc:
    enabled: true
```

## License

This work is open sourced under the Apache License, Version 2.0.

Copyright 2019 Tao He.

[1]: https://pages.github.com
[2]: https://pages.github.com/themes
[3]: https://github.com/sighingnow/jekyll-gitbook/fork
[4]: https://github.com/allejo/jekyll-toc
[5]: https://github.com/gitbook-plugins/gitbook-plugin-search-pro
[6]: https://github.com/rouge-ruby/rouge/tree/master/lib/rouge/themes

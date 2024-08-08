# 大语言模型服务价格汇总

2024年5月，各大模型厂商打起了“价格战”，意图拉拢更多开发者参与应用开发和模型落地探索。本仓库用于收集各大云服务厂商的大语言模型服务价格，方便用户对比。价格单位按照输入/输出每百万词元（Token）需要花费的人民币价格进行计算，美元到人民币汇率按最近一年的平均汇率7.2计算。

本仓库只是一个速查表，更详细的信息请参考各个厂商的官方价格文档。例如闲时价格、预付费价格、Batch调用价格等。

由于最近一年不同厂商的免费试用权益变动较多，获得免费权益的门槛变动也多，有效期也短，因此本仓库不收集免费试用权益包信息。


**统计模型和平台范围**：
- 只选取应用较为广泛，使用的应用数和人数较多，较为典型和具有代表性的模型和平台。以及服务价格较为便宜的平台。
- 由于本速查表主要面向翻译和中英双语应用，对于闭源且不支持中文（例如LLaMa系列）或中文支持较差的模型（例如Gemma-7B、mixtral系列）不会被纳入统计。
- 如果某开源模型在其官方平台已经十分便宜，那第三方平台的价格不会被纳入统计。
- 主要面向企业用户，个人用户难以申请使用的平台和模型不会被纳入统计。
- 在官方出了新模型且新模型性能提升较大，且价格相较旧模型更便宜或者持平的情况下，不再额外统计旧模型。（例如只统计LLaMa3不统计LLaMa2）
- 官方宣布即将被弃用的模型，或者描述为Older/Legacy的模型不会被纳入统计。
- 由于模型太小和/或性能不佳，连一篇完整新闻文章都翻译不下来的模型（例如qwen1.5-0.5b-chat）不会被纳入统计。


**统计数据范围**：
- 模型提供平台及定价页面
- API调用格式是否兼容OpenAI格式
- 审查情况（要求翻译[BBC政治新闻](https://www.bbc.com/news/world-asia-66727459)检查是否存在截断和拒绝回复的情况），不统计对暴力、色情、种族主义等内容的审查。
- 价格



## GPT系列
模型提供平台：[OpenAI](https://openai.com/pricing) / [Azure](https://azure.microsoft.com/zh-cn/pricing/details/cognitive-services/openai-service/)（定价基本一致）

API是否兼容OpenAI格式：OpenAI的天然兼容；Azure的有自定义格式，不兼容

审查情况：无审查

价格：

最后更新日期：2024-07-23

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| gpt-4o-mini      | 1.08                   | 4.32                  | 128            |        |
| gpt-4o-2024-08-06      | 18                   | 72                  | 128            |        |
| gpt-4o      | 36                   | 108                  | 128            |        |
| gpt-4-turbo | 72                   | 216                  | 128            |        |
| gpt-4       | 216                  | 432                  | 8              |        |
| gpt-4-32k   | 432                  | 864                  | 32             |        |
|gpt-3.5-turbo| 3.6                  | 10.8                 | 16             |        |


## Claude系列
模型提供平台： [Anthropic](https://docs.anthropic.com/en/docs/models-overview#model-comparison) / [AWS](https://aws.amazon.com/cn/bedrock/pricing/) 价格类似

API是否兼容OpenAI格式：否，自定义格式

审查情况：无审查

价格：

最后更新日期：2024-06-21

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| claude-3.5-sonnet | 21.6 | 108 | 200 |  |
| claude-3-opus | 108 | 540 | 200 |  |
| claude-3-sonnet | 21.6 | 108 | 200 |  |
| claude-3-haiku | 1.8 | 9 | 200 |  |

## Gemini系列
模型提供平台： [谷歌](https://ai.google.dev/pricing?hl=zh-cn) / [openrouter](https://openrouter.ai/docs#models)

API是否兼容OpenAI格式：否，自定义格式

审查情况：无审查

**谷歌官方平台随用随付**方案价格（注：以下价格为输入输出在128K以内的情况，超过128K翻倍）：

最后更新日期：2024-05-23

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| gemini-1.5-pro | 25.2 | 75.6 | 1000 |  |
| gemini-1.5-flash | 2.52 | 7.56 | 2800 |  |
| gemini-1.0-pro | 3.6 | 10.8 | 32 |  |

**openrouter**平台价格（有批发价）：

最后更新日期：2024-05-23

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| gemini-1.5-pro | 18 | 54 | 2800 |  |
| gemini-1.5-flash | 1.8 | 5.4 | 2800 |  |
| gemini-1.0-pro | 0.9 | 2.7 | 32 | 上下文窗口大小众说纷纭，建议以实际使用情况为准 |


## GLM闭源系列
模型提供平台： [智谱AI](https://open.bigmodel.cn/pricing)

API是否兼容OpenAI格式：兼容，参见[文档](https://open.bigmodel.cn/dev/api#openai_sdk)。

审查情况：平台对API输出有审查，参见[审查文档](https://open.bigmodel.cn/dev/howuse/securityaudit)。

价格：

最后更新日期：2024-06-05

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| GLM-4-0520 | 100 | 100 | 128 | 当前智谱AI最先进的模型，指令遵从能力大幅提升，发布于20240605 |
| GLM-4-Air | 1 | 1 | 128 | 性价比最高的版本，综合性能接近GLM-4，速度快，价格实惠。 |
| GLM-4-Airx | 10 | 10 | 128 | GLM-4-Air 的高性能版本，效果不变，推理速度达到其2.6倍。 |
| GLM-4-Flash | 0.1 | 0.1 | 128 | 即开源的GLM4-9B模型，适用简单任务，速度最快，价格最实惠的版本。 |

注：由于ChatGLM开源版本商用API较少，计费通常也比GLM-4-Air贵，性能也和GLM-4-Air差不多，所以不统计。


## Deepseek系列
模型提供平台： [deepseek官方开放平台](https://platform.deepseek.com/api-docs/zh-cn/pricing)
API是否兼容OpenAI格式：是

审查情况：平台对API输出有审查

价格：

最后更新日期：2024-05-23

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| deepseek-chat（基于DeepSeek-V2） | 1 | 2 | 128 |  |


## 零一万物Yi系列
模型提供平台： [零一万物大模型开放平台](https://platform.lingyiwanwu.com/docs)

API是否兼容OpenAI格式：是

审查情况：平台对API输入和输出有审查

价格：

最后更新日期：2024-05-23

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| yi-large | 20 | 20 | 16 |  |
| yi-large-turbo | 12 | 12 | 16 |  |
| yi-medium-200k | 12 | 12 | 200 |  |
| yi-medium | 2.5 | 2.5 | 16 |  |
| yi-spark | 1 | 1 | 16 |  |

## 通义千问开源系列
模型提供平台： [阿里云](https://help.aliyun.com/zh/dashscope/developer-reference/tongyi-qianwen-7b-14b-72b-metering-and-billing) / [together.ai](https://api.together.xyz/models?filter=serverless) / [openrouter](https://openrouter.ai/docs#models) / [siliconflow](https://siliconflow.cn/zh-cn/pricing)

API是否兼容OpenAI格式：是，参见[阿里云文档](https://help.aliyun.com/zh/dashscope/developer-reference/compatibility-of-openai-with-dashscope/)；[together.ai文档](https://docs.together.ai/docs/openai-api-compatibility)；[openrouter文档](https://openrouter.ai/docs#requests)；[siliconflow文档](https://siliconflow.readme.io/)

审查情况：开源模型本身不存在审查；together.ai等境外平台对输入输出无审查；阿里云平台存在审查，见[文档](https://help.aliyun.com/document_detail/2712216.html)

**阿里云平台价格**：

最后更新日期：2024-05-23

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| qwen2-72b-instruct | 5 | 10 | 32 |  |
| qwen2-57b-a14b-instruct | 3.5 | 7 | 32 |  |
| qwen2-7b-instruct | 1 | 2 | 32 |  |
| qwen1.5-110b-chat | 7 | 14 | 32 |  |
| qwen1.5-72b-chat | 5 | 10 | 32 |  |
| qwen1.5-32b-chat | 3.5 | 7 | 32 |  |
| qwen1.5-14b-chat | 2 | 4 | 8 |  |
| qwen1.5-7b-chat | 1 | 2 | 8 |  |


**together.ai平台价格**（输入输出一致，适合翻译等输出文本较多的任务）：

最后更新日期：2024-06-09

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| qwen1.5-110b-chat | 12.96 | 12.96 | 32 |  |
| qwen2-72b-instruct | 6.48 | 6.48 | 32 |  |
| qwen1.5-72b-chat | 6.48 | 6.48 | 32 |  |
| qwen1.5-32b-chat | 5.76 | 5.76 | 32 |  |
| qwen1.5-14b-chat | 2.16 | 2.16 | 32 |  |
| qwen1.5-7b-chat | 1.44 | 1.44 | 32 |  |


使用openrouter调用会路由至together.ai，价格一致，但是由于有批发价，目前暂时提供9折优惠。

**siliconflow平台价格**：

最后更新日期：2024-06-09

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| Qwen2-72B-Instruct | 4.13 | 4.13 | 32 |  |
| Qwen2-57B-A14B-Instruct | 1.26 | 1.26 | 32 |  |
| Qwen2-7B-Instruct | 0.35 | 0.35 | 32 |  |
| Qwen1.5-110B | 4.13 | 4.13 | 32 |  |
| Qwen1.5-32B | 1.26 | 1.26 | 32 |  |
| Qwen1.5-14B | 0.7 | 0.7 | 32 |  |
| Qwen1.5-7B | 0.35 | 0.35 | 32 |  |


## 通义千问闭源系列
模型提供平台： [阿里云](https://help.aliyun.com/zh/dashscope/developer-reference/tongyi-thousand-questions-metering-and-billing)

API是否兼容OpenAI格式：是，参见[文档](https://help.aliyun.com/zh/dashscope/developer-reference/compatibility-of-openai-with-dashscope/)

审查情况：无审查

价格：

最后更新日期：2024-05-23

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| qwen-long | 0.5 | 2 | 10000 |  |
| qwen-turbo | 2 | 6 | 8 |  |
| qwen-plus | 4 | 12 | 32 |  |
| qwen-max | 40 | 120 | 8 |  |
| qwen-max-longcontext | 120 | 120 | 32 |  |


## 百川系列
模型提供平台： [百川智能开放平台](https://platform.baichuan-ai.com/price)

API是否兼容OpenAI格式：是，参见[官方调用文档](https://platform.baichuan-ai.com/docs/api)

审查情况：未知，未测试

价格：

最后更新日期：2024-05-23

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| Baichuan4 | 100 | 100 | 未见公开报道 |  |
| Baichuan3-Turbo | 12 | 12 | 未见公开报道 |  |
| Baichuan3-Turbo-128k | 24 | 24 | 128 |  |
| Baichuan2-Turbo | 8 | 8 | 未见公开报道 |  |
| Baichuan2-Turbo-192k | 16 | 16 | 192 |  |
| Baichuan2-53B | 20 | 20 | 4 |  |


## 豆包系列
模型提供平台： [字节跳动火山引擎](https://www.volcengine.com/docs/82379/1099320)

API是否兼容OpenAI格式：否，自定义格式

审查情况：存在，见[官方文档错误码](https://www.volcengine.com/docs/82379/1263483)，搜索“敏感”

价格：

最后更新日期：2024-05-23

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| Doubao-lite-32k | 0.3 | 0.6 | 32 |  |
| Doubao-lite-128k | 0.8 | 1 | 128 |  |
| Doubao-pro-32k | 0.8 | 2 | 32 |  |
| Doubao-pro-128k | 5 | 9 | 128 |  |


## 文心Ernie系列
模型提供平台： [百度千帆大模型平台](https://cloud.baidu.com/doc/WENXINWORKSHOP/s/hlrk4akp7)

API是否兼容OpenAI格式：否，自定义格式

审查情况：对输出存在审查。

价格：

最后更新日期：2024-05-23

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| ERNIE 4.0系列 | 120 | 120 | 8 |  |
| ERNIE 3.5系列 | 12 | 12 | 最大128 |  |
| ERNIE-3.5-128k | 12 | 12 | 128 |  |
| ERNIE Speed系列 | 0 | 0 | 最大128 |  |
| ERNIE Lite系列 | 0 | 0 | 最大128 |  |
| ERNIE Tiny系列 | 0 | 0 | 8 |  |


## 腾讯混元系列
模型提供平台： [腾讯云](https://cloud.tencent.com/document/product/1729/97731)

API是否兼容OpenAI格式：否，自定义格式，而且签名方法很难用

审查情况：未知，未测试

价格：

最后更新日期：2024-05-23

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| hunyuan-pro | 30 | 100 | 32 |  |
| hunyuan-standard-32k | 4.5 | 5 | 32 |  |
| hunyuan-standard-256k | 15 | 60 | 256 |  |
| hunyuan-lite | 0 | 0 | 256 |  |


## cohere/command系列
模型提供平台： [cohere官方平台](https://cohere.com/pricing) / [openrouter](https://openrouter.ai/docs#models) / [Azure](https://azuremarketplace.microsoft.com/en/marketplace/apps/cohere.cohere-command-r-plus-offer?tab=PlansAndPrice)

API是否兼容OpenAI格式：官方平台和Azure不兼容，为自定义格式；第三方平台例如openrouter兼容。

审查情况：无审查

（三个平台统一）价格：

最后更新日期：2024-05-23

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| command-r-plus | 21.6 | 108 | 128 |  |
| command-r | 3.6 | 10.8 | 128 |  |


## 月之暗面系列
模型提供平台： [moonshot开放平台](https://platform.moonshot.cn/docs/pricing)

API是否兼容OpenAI格式：是，参见[文档](https://platform.moonshot.cn/docs/api/chat)

审查情况：未测试，未知

价格：

最后更新日期：2024-05-24

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
| moonshot-v1-8k | 12 | 12 | 8k |  |


## 模板
模型提供平台： []() / []() / []()

API是否兼容OpenAI格式：

审查情况：

价格：

最后更新日期：YYYY-MM-DD

| **模型**      | **输入价格（元/M Tokens）** | **输出价格（元/M Tokens）** | **上下文窗口大小（K）** | **备注** |
|:-----------:|:--------------------:|:--------------------:|:--------------:|:------:|
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

## 其他

由于看不懂讯飞星火的定价策略和接口调用，故没有收录。
minimaxi也没有收录，因为看不出来有什么优势。

---
layout: post
title: "软件测试介绍"
date: 2018-5-11 20:37:10 
description: "软件测试入门"
tag: Software Testing
---

这里将介绍软件测试的一些基本概念！

### 软件测试

#### 定义
* 软件测试是有计划的、系统性的不可缺少的步骤
* 这是一项经验性的工作，目的在于向利益相关者提供关于产品质量和测试服务质量的信息
* 判断软件是否满足用户期望
* 软件测试是软件质量保证的关键步骤

#### 目的
* 发现软件中存在的错误，好的测试应能在第一时间发现程序中存在的错误。
* 降低软件无法工作的风险，好的测试应能发现至今尚未发现的错误。

#### 测试通过标准
* 所有测试用例是否执行完
* 功能是否设计完毕
* 是否找到足够的Bug

#### 基本功能

| 功能 | 描述                    |
| ------------- | ----------------------------------------- |
| 验证(verification) | 软件应该满足规格说明文档    |
| 确认(vaildation)  | 软件应该满足用户真正的需求  |

#### 与Debug区别

| Test | Debug                   |
| ------------- | ----------------------------------------- |
|检验|推理过程|
|  条件已知，规程可定义，结果可预知 | 条件未知，结果不可预知|
| 可自动化| 无法自动化 |
|可不了解设计细节|必须了解细节|
|表明程序正确还要验证程序如何处理失败|表明正确|

### 软件测试的必要性
> 1. 大多数的安全漏洞都是由于软件缺陷造成的。
> 2. 由于糟糕的软件，导致世界范围内的金钱的损失是惊人的。
> 3. 强有力的测试可以解决大部分的问题。
> 4. 我们想让我们的程序可靠。

#### 例证
* Aerobus 747-400 由1000000个零件组成，每个零件的合格率为99.9999%，那么该产品的合格率为(99.9999%)^1000000 = 36.79%.
* 每行代码的合格率为99%，一个程序有10000行代码，该程序的合格率为(99%)^10000=2.25x10^(-44).

### 软件缺陷

#### 定义
* 不符合用户的期望
* 软件功能可以被不正确的执行
* 所有类型的软件问题，如不一致性，用户界面错误
* Bug

在软件测试中，我们将下述的名词都统称为软件缺陷(Defect)，软件缺陷可能在软件开发的各个阶段被引入，且有可能被放大。

| 名词 | 描述                    |
| ------------- | ----------------------------------------- |
| 错误(Error) | 出现在写程序的过程中     |
| 故障(Fault)  | 一个或多个错误的表现 |
| 失效(Failure) |  发生在由于错误代码导致一个不正确的状态传播到程序的输出    |
| 事故(Incident)  | 在失效发生的时候没有消息提示 |

#### 缺陷出现
1. 软件没有实现需求规格说明文档明确要求必须实现的功能。
2. 软件实现了需求规格说明文档明确要求不要实现的功能。
3. 软件实现了需求规格说明文档没有提到的功能
4. 软件没有实现需求规格说明文档没有提到但应该实现的功能
5. 软件难以理解，难以使用，缓慢

### 测试类型
* C1. 按照测试生成的来源
* C2. 按照生命周期的阶段
* C3. 按照测试活动的目的
* C4. 按被测对象的特征
* C5. 按测试过程的模型

#### 举例
> 问题：考虑要测试的Web服务W。当被执行时，W将一个给定的温度值从一个尺度转换到另一个尺度，例如从华氏温标到摄氏温标。
>
> 情景一：假设测试人员通过提供样例输入和检查输出来测试W，但没有用于生成输入的特定方法。
> 解答：C1的黑盒测试，C2的单元测试，C3的GUI测试（如果有界面）
>
> 情景二：假设测试人员B使用Z语言为W写一组正式的规范，测试人员从规范中生成并使用测试。
> 解答：C1的黑盒测试
>
> 情景三：假设测试人员C使用W.C的正式规范生成测试，然后使用几个代码覆盖率标准之一来测试W并评估代码覆盖率，C发现代码覆盖率不是百分之百
> 解答：C1的黑盒测试和白盒测试
>
> 情景四：假设测试人员D测试W作为一个更大的应用程序的组件。测试人员D无法访问W的代码，因此只使用其接口和接口突变来生成测试
> 解答：C1的黑盒测试
>
> 补充：无论如何都会使用C4的web服务测试

### 测试用例

#### 定义
如果系统按照其规范运行，则需要对系统的输入和预期输出进行测试

#### 原则
* 避免模糊的测试用例
* 类似的功能应该被抽象和分类
* 避免复杂测试用例

#### 设计特性
* 有效性

测试用例是测试人员测试过程中的重要参考依据。不同的测试人员根据相同的测试用所得到的输出是一致的，对于准确的测试用例的计划、执行和跟踪是测试的有效性的有力证明。

* 可复用性

良好的测试用例具有可重复使用的功能，能够节约时间，提高效率，事半功倍。

* 易组织性

正确的测试计划会很好地组织这些测试用例并提供给测试人员或其他项目的人参考和有效使用。

* 可评估性

测试用例的通过率是检验代码质量的保证，测试用例的通过率和软件错误的数目就是检查代码质量的量化标准。

* 可管理性

测试用例可作为检验测试人员进度、工作量以及跟踪/管理测试人员的工作效率因素，尤其是比较适用于对新的测试人员的检验，从而做出测试安排和计划。

### 设计方法
1. 测试人员需要对产品的设计、规格说明文档、用户场景以及程序/模块的结构有比骄傲透彻的理解
2. 测试用例尽可能覆盖一种或多种情况
3. 测试用例需要很确切地反映功能设计，但最好不要完全复制规格说明文档
4. 软件测试本地化
5. 测试过程中，测试用例的状态是惟一的。良好的测试用例一般有三种状态：通过、未通过和未进行测试
6. 测试用例避免复杂的目的就是为了保证测试用例的惟一性


### 回归测试
测试用例就是设计一个情况，软件程序在这种情况下，必须能够正常运行并且达到程序所设计的执行结果。如果不能正常运行，并且这种问题会重复发生，那么就表明已经测出了软件的缺陷，这时就必须将这个问题标示出来，并且输入到问题跟踪系统内，通知开发人员。开发人员接收到这个问题后，进行修复，然后测试人员取得新的测试版本，必须利用同一个用例来测试这个问题，确保该问题已经修改。

<br>

转载请注明：[锡佳的博客](http://www.luxijia.top) » [点击阅读原文](http://www.luxijia.top/2018/05/SoftwareTestingIntroduction/)
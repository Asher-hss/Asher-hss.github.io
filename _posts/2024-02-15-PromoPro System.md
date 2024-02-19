---
layout:     post
title:      "PromoPro System"
subtitle:   "对于PromoPro System项目的简易说明"
data:       2024-02-15
author:     Asher
header-img: "img/240215/bg.jpg"
header-style: text
catalog:    true
tags:       
    - React
    - SpringBoot
    - DDD
---
<br>In today's competitive market, engaging customers and fostering loyalty are paramount to driving sales and growth.

<br>My latest project is designed to address these challenges head-on, offering a comprehensive marketing solution that spans various activities such as lotteries and points redemption programs.

<br>The current system provides a simple lottery interface, allowing users to conduct lottery operations and receive feedback on the results.

![lottery](/img/240215/lottery.jpg)

![result](/img/240215/result.jpg)

<br>Designed the domain model functionalities for lottery, abstracted into three stages of the lottery process: pre-lottery, during-lottery, and post-lottery. Expanded actions at each stage, such as audience segmentation before lottery, inventory deduction during lottery, and providing fallback rewards after lottery.

<br>Designed a lottery database schema and abstracted the lottery process into four tables: Lottery Strategy Table, Strategy Detail Table, Rule Configuration Table, and Rule Tree Action Table, enhancing the project's scalability.

![award](/img/240215/award.jpg)

![rule](/img/240215/rule.jpg)


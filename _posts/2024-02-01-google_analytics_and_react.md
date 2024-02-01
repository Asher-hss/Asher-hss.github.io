---
layout:     post
title:      "use Google Analytics in react project"
subtitle:   "如何在react项目中进行网站数据统计"
data:       2024-02-01
author:     Asher
header-img: "img/post-bg-os-metro.jpg"
catalog:    true
tags:       
    - react
    - Google Analytics
---
<div>
<br>最近做react项目的时候，新增了一个需求。
<br>需要使用进行网站数据的统计，这里选择了google analytics，baidu analytics同理。
<br>省去前面的步骤，google analytics会提示我们直接加入下面代码在 `<head>` 后面。

    <!-- Google tag (gtag.js) -->
        <script async src="https://www.googletagmanager.com/gtag/js?id=G-xxxxxx"></script>
        <script>
            window.dataLayer = window.dataLayer || [];
            function gtag(){dataLayer.push(arguments);}
            gtag('js', new Date());
            gtag('config', 'G-xxxxxx');
        </script>
<br>
<br>但是呢，直接加入是没有效果，这是因为在JSX中直接写入脚本标签会被处理为文本内容，因此需要做以下修改：

        <Head>
        <script async src="https://www.googletagmanager.com/gtag/js?id=G-xxxxxx"></script>
        <script
            dangerouslySetInnerHTML={{
            __html: `
            window.dataLayer = window.dataLayer || [];
            function gtag(){dataLayer.push(arguments);}
            gtag('js', new Date());
            gtag('config', 'G-FFPXB3TZP8');
                `,
            }}
        />
        </Head>

<br>这样就可以了,此时可以在google analytics里使用test进行测试。
</div>
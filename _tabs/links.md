---
layout: page 
icon: fas fa-link
order: 4
---

<div style="text-align: center; margin-bottom: 20px;">
  <h1 style="text-align: center; font-size: 1.5rem;"> 欢迎成为我的网上邻居 (>_<) </h1>
</div>

<hr style="border-top: 2px solid #f0f0f0; margin: 20px 0;">

<style>
    /* 用于整体友链区域的样式，设置一些基本的布局样式，修改此处让其整体偏左 */
   .friend-links-container {
        width: fit-content;
        margin: 0 auto;
    }

    /* 图片样式，保持之前设置的尺寸等属性 */
   .my-img-size {
        width: 80px;
        height: 80px;
        border-radius: 50%;
    }

    /* 每个友链链接的样式，设置为块级元素，使其上下排列 */
   .friend-link {
        display: block;
        margin-bottom: 30px;
    }

    /* 调整图片和描述文字之间的距离 */
   .friend-link img + span {
        margin-left: 30px;
    }
</style>

<div class="friend-links-container">
    <!-- 这个 div 用于放置所有的友链元素，后续通过 JavaScript 动态添加 -->
</div>

<script>
    const friendLinks = [
        {
            href: "https://ohoou.cn",
            imgSrc: "https://avatars.githubusercontent.com/u/110218151?v=4",
            name: "OHO"
        },
        {
            href: "https://notes.youngkbt.cn",
            imgSrc: "https://cdn.jsdelivr.net/gh/Kele-Bingtang/static/user/avatar2.png",
            name: "Young Kbt Blog"
        }
    ];

    const friendLinksContainer = document.querySelector('.friend-links-container');
    friendLinks.forEach(link => {
        const aTag = document.createElement('a');
        aTag.href = link.href;
        aTag.target = "_blank";
        aTag.className = "friend-link";
        aTag.style.textDecoration = "none";

        const imgTag = document.createElement('img');
        imgTag.src = link.imgSrc;
        imgTag.className = "my-img-size";
        imgTag.alt = link.name;

        const spanTag = document.createElement('span');
        spanTag.textContent = link.name;

        aTag.appendChild(imgTag);
        aTag.appendChild(spanTag);
        friendLinksContainer.appendChild(aTag);
    });
</script>

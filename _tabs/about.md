---
layout: page
icon: fas fa-info-circle
order: 5
---

<style>
 .social-links {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 10px;
    }
 .social-icon {
        font-size: 1.5rem; /* 增大图标字体大小 */
        margin-right: 5px;
    }
 .social-link {
        font-size: 1.2rem; /* 增大链接文字的字体大小 */
        color: #007bff; /* 链接颜色，可自行调整 */
        text-decoration: none;
        transition: color 0.3s ease; /* 鼠标悬停过渡效果 */
    }
 .social-link:hover {
        color: #0056b3; /* 鼠标悬停时的颜色变化 */
    }
</style>

<div id="app">
    <h1 style="text-align: center; font-size: 1.5rem;">欢迎来到Destiny-LB的个人网站！</h1>
    <hr>
    <h2 style="text-align: center; font-size: 1.2rem;">有关我的更多信息，请访问以下网站:</h2>
    <div class="social-links" id="social-links-container"></div>
    <hr>
    <p style="text-align: center; font-size: 1.1rem;">谢谢您的浏览！</p>
</div>

<script>
    const socialPlatforms = [
        { iconClass: "fab fa-weibo", href: "https://weibo.com/n/Destiny-LB", url: "https://weibo.com/destiny-lb" },
        { iconClass: "fab fa-tiktok", href: "https://v.douyin.com/AvmNk7J", url: "https://www.douyin.com/destiny-lb" },
        { iconClass: "fab fa-redhat", href: "https://www.xiaohongshu.com/user/profile/6306d9d900000000120010e0", url: "https://www.xiaohongshu.com/destiny-lb" },
        { iconClass: "fab fa-github", href: "https://github.com/Destiny-LB", url: "https://github.com/destiny-lb" }
    ];

    const socialLinksContainer = document.getElementById('social-links-container');

    socialPlatforms.forEach((platform) => {
        const linkElement = document.createElement('a');
        linkElement.href = platform.href;
        linkElement.target = "_blank";
        linkElement.rel = "noopener";
        linkElement.className = "social-link";
        linkElement.textContent = platform.url;

        const iconElement = document.createElement('i');
        iconElement.className = `fab ${platform.iconClass} social-icon`;

        const listItem = document.createElement('div');
        listItem.appendChild(iconElement);
        listItem.appendChild(linkElement);

        socialLinksContainer.appendChild(listItem);
    });

    function addNewSocialLink(iconClass, href, url) {
        const newLinkElement = document.createElement('a');
        newLinkElement.href = href;
        newLinkElement.target = "_blank";
        newLinkElement.rel = "noopener";
        newLinkElement.className = "social-link";
        newLinkElement.textContent = url;

        const newIconElement = document.createElement('i');
        newIconElement.className = `fab ${iconClass} social-icon`;

        const newListItem = document.createElement('div');
        newListItem.appendChild(newIconElement);
        newListItem.appendChild(newLinkElement);

        socialLinksContainer.appendChild(newListItem);
    }
</script>

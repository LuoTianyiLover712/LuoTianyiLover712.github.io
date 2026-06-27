<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的个人博客</title>
    <style>
        /* ---------- 全局重置 ---------- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            background: #f8f9fa;
            color: #1e1e2a;
            line-height: 1.7;
            padding: 0 20px;
        }

        .wrapper {
            max-width: 960px;
            margin: 0 auto;
            padding: 30px 0 50px;
        }

        /* ---------- 顶栏 / 导航 ---------- */
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 0 20px;
            border-bottom: 1px solid #eaeef2;
            flex-wrap: wrap;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 800;
            letter-spacing: -0.5px;
            color: #0b0b1a;
            text-decoration: none;
        }

        .logo span {
            color: #4a6cf7;
        }

        .nav-links {
            display: flex;
            gap: 28px;
            font-size: 0.95rem;
            font-weight: 500;
        }

        .nav-links a {
            text-decoration: none;
            color: #3d3d4e;
            transition: color 0.2s;
        }

        .nav-links a:hover {
            color: #4a6cf7;
        }

        /* ---------- 博客头部简介 ---------- */
        .hero {
            margin: 40px 0 45px;
            padding-bottom: 25px;
            border-bottom: 1px solid #eaeef2;
        }

        .hero h1 {
            font-size: 2.8rem;
            font-weight: 700;
            letter-spacing: -1px;
            line-height: 1.2;
            margin-bottom: 8px;
        }

        .hero p {
            font-size: 1.15rem;
            color: #5e5e72;
            max-width: 600px;
        }

        /* ---------- 文章列表 ---------- */
        .post-list {
            display: flex;
            flex-direction: column;
            gap: 30px;
            margin-top: 10px;
        }

        .post-card {
            background: #ffffff;
            padding: 28px 32px;
            border-radius: 20px;
            box-shadow: 0 2px 12px rgba(0, 0, 0, 0.04);
            transition: box-shadow 0.25s, transform 0.2s;
            border: 1px solid #ffffff;
        }

        .post-card:hover {
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.07);
            transform: translateY(-2px);
            border-color: #eef2f6;
        }

        .post-meta {
            display: flex;
            gap: 18px;
            font-size: 0.85rem;
            color: #8a8a9e;
            margin-bottom: 6px;
            flex-wrap: wrap;
        }

        .post-meta .tag {
            background: #f0f2f5;
            padding: 0 12px;
            border-radius: 40px;
            color: #3d3d4e;
            font-weight: 500;
            font-size: 0.75rem;
            line-height: 22px;
        }

        .post-card h2 {
            font-size: 1.6rem;
            font-weight: 700;
            margin: 6px 0 10px;
            line-height: 1.3;
        }

        .post-card h2 a {
            text-decoration: none;
            color: #0b0b1a;
            transition: color 0.2s;
        }

        .post-card h2 a:hover {
            color: #4a6cf7;
        }

        .post-card .excerpt {
            color: #3d3d4e;
            margin-bottom: 14px;
            font-size: 0.98rem;
        }

        .post-card .read-more {
            font-weight: 600;
            font-size: 0.9rem;
            color: #4a6cf7;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 4px;
        }

        .post-card .read-more:hover {
            text-decoration: underline;
        }

        /* ---------- 分页（示例） ---------- */
        .pagination {
            margin-top: 45px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-top: 1px solid #eaeef2;
            padding-top: 30px;
        }

        .pagination a {
            text-decoration: none;
            color: #4a6cf7;
            font-weight: 600;
            font-size: 0.95rem;
        }

        .pagination a:hover {
            text-decoration: underline;
        }

        .pagination .disabled {
            color: #b0b0c0;
            pointer-events: none;
        }

        /* ---------- 页脚 ---------- */
        .footer {
            margin-top: 50px;
            text-align: center;
            font-size: 0.85rem;
            color: #8a8a9e;
            border-top: 1px solid #eaeef2;
            padding-top: 30px;
        }

        .footer a {
            color: #4a6cf7;
            text-decoration: none;
        }

        /* ---------- 移动端 ---------- */
        @media (max-width: 640px) {
            .wrapper {
                padding: 15px 0 30px;
            }
            .navbar {
                flex-direction: column;
                align-items: flex-start;
                gap: 12px;
            }
            .hero h1 {
                font-size: 2.1rem;
            }
            .post-card {
                padding: 20px 18px;
            }
            .post-card h2 {
                font-size: 1.3rem;
            }
            .post-meta {
                font-size: 0.8rem;
                gap: 10px;
            }
        }
    </style>
</head>
<body>

    <div class="wrapper">

        <!-- ======== 导航栏 ======== -->
        <nav class="navbar">
            <a href="#" class="logo">My<span>Blog</span></a>
            <div class="nav-links">
                <a href="#">首页</a>
                <a href="#">归档</a>
                <a href="#">关于</a>
                <a href="#">友链</a>
            </div>
        </nav>

        <!-- ======== 个人简介 ======== -->
        <header class="hero">
            <h1>👋 你好，我是 <span style="color:#4a6cf7;">你的名字</span></h1>
            <p>这里是我记录技术思考、生活随笔和读书笔记的地方。持续更新，保持好奇。</p>
        </header>

        <!-- ======== 文章列表 ======== -->
        <main class="post-list">

            <!-- 文章卡片 1 -->
            <article class="post-card">
                <div class="post-meta">
                    <time datetime="2026-06-27">2026年6月27日</time>
                    <span class="tag">技术</span>
                    <span class="tag">GitHub</span>
                </div>
                <h2><a href="#">如何用 GitHub Pages 搭建个人博客</a></h2>
                <p class="excerpt">
                    从零开始，手把手教你注册仓库、配置域名、选择主题，十分钟内上线你的第一个博客网站...
                </p>
                <a href="#" class="read-more">阅读全文 →</a>
            </article>

            <!-- 文章卡片 2 -->
            <article class="post-card">
                <div class="post-meta">
                    <time datetime="2026-06-20">2026年6月20日</time>
                    <span class="tag">生活</span>
                    <span class="tag">阅读</span>
                </div>
                <h2><a href="#">2026上半年读书清单分享</a></h2>
                <p class="excerpt">
                    今年读完了 12 本书，从科幻小说到认知心理学，挑出 5 本最值得推荐的分享给你...
                </p>
                <a href="#" class="read-more">阅读全文 →</a>
            </article>

            <!-- 文章卡片 3 -->
            <article class="post-card">
                <div class="post-meta">
                    <time datetime="2026-06-10">2026年6月10日</time>
                    <span class="tag">工具</span>
                    <span class="tag">效率</span>
                </div>
                <h2><a href="#">5 个提升编码效率的 VS Code 插件</a></h2>
                <p class="excerpt">
                    精选我日常离不开的插件，涵盖代码格式化、Git 可视化、AI 辅助编程和主题美化...
                </p>
                <a href="#" class="read-more">阅读全文 →</a>
            </article>

            <!-- 文章卡片 4（可继续添加） -->
            <article class="post-card">
                <div class="post-meta">
                    <time datetime="2026-06-01">2026年6月1日</time>
                    <span class="tag">随想</span>
                </div>
                <h2><a href="#">儿童节快乐：保持编程的初心</a></h2>
                <p class="excerpt">
                    写代码就像搭积木，永远保持好奇心和创造力，是我们对抗职业倦怠最好的方式...
                </p>
                <a href="#" class="read-more">阅读全文 →</a>
            </article>

        </main>

        <!-- ======== 分页导航 ======== -->
        <div class="pagination">
            <span class="disabled">← 上一页</span>
            <span style="color:#3d3d4e; font-size:0.9rem;">第 1 页 / 共 3 页</span>
            <a href="#">下一页 →</a>
        </div>

        <!-- ======== 页脚 ======== -->
        <footer class="footer">
            © 2026 你的名字 · 用 ❤️ 和 GitHub Pages 搭建 ·
            <a href="https://github.com/你的用户名" target="_blank">GitHub</a>
        </footer>

    </div>

</body>
</html>

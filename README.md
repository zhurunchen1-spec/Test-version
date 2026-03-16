diff --git a/README.md b/README.md
index 6d342d80fb64341236ac63a4b543d179ec3457c9..e4c6c94714659ffd129a69346eed76d8afd2e2d0 100644
--- a/README.md
+++ b/README.md
@@ -1,2 +1,44 @@
 # Test-version
-在真正使用codex之前的测试工作
+在真正使用 codex 之前的测试工作。
+
+## 贪吃蛇小游戏
+已新增一个纯前端的贪吃蛇小游戏：
+
+- 文件：`index.html`
+- 本地运行：在仓库目录启动任意静态服务器后打开页面
+- 线上运行：支持 GitHub Pages 自动部署，部署后可通过固定网址访问
+
+## 本地体验
+```bash
+python3 -m http.server 8000
+```
+
+然后访问：
+- `http://localhost:8000/index.html`
+
+## 操作说明
+- 点击“开始 / 重新开始”开始游戏
+- 使用方向键或 `W/A/S/D` 控制蛇的移动
+- 点击“暂停”可暂停/继续
+- 撞墙或撞到自己会结束游戏
+
+## 难度与排行榜
+- 难度分为三级：
+  - 低级：速度最慢
+  - 中等：速度中等
+  - 高级：速度最快
+- 每个难度有独立排行榜（前 5 名），互不影响
+- 每局结束后会把当前分数写入当前难度排行榜
+- 排行榜数据会保存在浏览器本地存储中
+
+## 生成可分享网址（GitHub Pages）
+仓库已包含自动部署工作流：`.github/workflows/deploy-pages.yml`。
+
+1. 把当前分支推送到 GitHub 仓库。
+2. 在仓库 `Settings -> Pages` 中确认 Source 为 `GitHub Actions`。
+3. 等待 `Deploy static content to Pages` 工作流执行完成。
+4. 访问：
+   - `https://<你的GitHub用户名>.github.io/<仓库名>/`
+
+例如仓库名是 `Test-version`，用户名是 `alice`，则网址是：
+- `https://alice.github.io/Test-version/`

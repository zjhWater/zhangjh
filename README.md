# zhangjh · 作品集

一个静态单页作品集，只用 HTML + CSS，没有框架、没有构建步骤。
唯一的内容是作品 **dsh-stand-reminder**（DeepSeek Harness 的像素风久坐与饮水提醒插件）。

## 本地预览

直接双击 `index.html`，或：

```powershell
cd D:\Python\zhangjh-site
python -m http.server 8080
# 浏览器打开 http://localhost:8080
```

## 部署到 GitHub Pages

1. 在 GitHub 新建仓库 **`zhangjh`**（public，不要勾选初始化 README）。
2. 在本目录执行：

   ```powershell
   git init
   git add .
   git commit -m "feat: portfolio page"
   git branch -M main
   git remote add origin https://github.com/zjhWater/zhangjh.git
   git push -u origin main
   ```

3. 打开仓库 **Settings → Pages**：
   - Source 选 `Deploy from a branch`
   - Branch 选 `main`，目录选 `/ (root)`
   - 点 Save
4. 等 1–2 分钟，访问 **https://zjhwater.github.io/zhangjh/**

之后每次改完内容，`git add -A && git commit -m "..." && git push` 就会自动更新（Pages 重新构建大约 1 分钟）。

## 结构

```
index.html        页面本体（样式内联在 <style> 里）
assets/widget.png 完整挂件截图（像素图放大，非模糊缩放）
assets/mini.png   迷你模式截图
.nojekyll         关掉 Jekyll，静态文件原样发布
```

## 改内容时看这里

- 名字：搜 `张继辉`，共 3 处（`<h1>`、页脚、`<title>`）。
- 作品数据：搜 `126`（断言数）、`85 kB`（打包体积）这几个数字。
- 配色：改 `:root` 里的 CSS 变量即可，深色模式在 `prefers-color-scheme: dark` 那一段。

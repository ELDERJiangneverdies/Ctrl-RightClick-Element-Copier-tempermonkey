# Ctrl-RightClick-Element-Copier-tempermonkey
A lightweight userscript (for Tampermonkey/Greasemonkey)/一个轻量的用户脚本（适用于 Tampermonkey/Greasemonkey）
# Ctrl+RightClick Element Copier / Ctrl+右键元素复制器

中文简介
一个轻量的 Tampermonkey/Greasemonkey 用户脚本：按住 Ctrl 并右键点击页面上的任意元素即可复制该元素的 outerHTML。操作时会短暂高亮目标元素并显示提示（toast），优先使用现代 Clipboard API，失败时自动回退到 execCommand。适合快速抓取 DOM 片段或调试页面结构。

English summary
A lightweight userscript for Tampermonkey/Greasemonkey: hold Ctrl and right‑click any page element to copy its outerHTML. The element is briefly highlighted and a toast confirms the copy. Uses the Clipboard API when available and falls back to execCommand. Handy for quickly extracting DOM snippets or debugging page markup.

## Features / 功能
- Ctrl + 右键复制元素 outerHTML / Ctrl + Right‑Click copies element outerHTML  
- 高亮目标元素并显示短暂提示 / Brief highlight + toast confirmation  
- 支持现代 Clipboard API，自动回退到 execCommand / Uses Clipboard API with execCommand fallback  
- 全站匹配（可按需修改 @match）/ Matches all sites by default (adjust @match as needed)

## Installation / 安装
1. 安装 Tampermonkey 或 Greasemonkey 浏览器扩展。  
2. 新建一个用户脚本（Create new script），将脚本内容粘贴进编辑器并保存。或者将脚本文件放入扩展支持的导入方式中。  
3. 根据需要修改 @match 或脚本中的样式/快捷键。

1. Install the Tampermonkey or Greasemonkey extension.  
2. Create a new userscript, paste the script content and save. Or import the .user.js file if supported.  
3. Optionally adjust @match, styles, or key settings in the script.

## Usage / 使用方法
- 在任意网页按住 Ctrl，使用鼠标右键点击想要复制的元素。  
- 成功时会短暂高亮元素并在页面顶部显示“元素已复制！”的提示。  
- 若复制失败，会显示错误提示。

- Hold Ctrl and right‑click any element on a webpage to copy it.  
- On success the element is briefly highlighted and a toast appears saying the element was copied.  
- An error toast appears if copying fails.

## Customization / 可定制项
- 修改快捷键：编辑脚本中对 event.ctrlKey 的判断（例如改为 event.shiftKey）。  
- 修改高亮样式或持续时间：编辑脚本中对应的 CSS 或 setTimeout 时长。  
- 更改提示文案或位置：编辑 showToast 函数或样式。

- Change the trigger key: edit event.ctrlKey to another condition (e.g., event.shiftKey).  
- Tweak highlight style or duration via the CSS or setTimeout.  
- Adjust toast text or position in showToast and CSS.

## Security & Permissions / 安全与权限
- 脚本仅在本地注入并读取 DOM，使用剪贴板 API 时需在安全上下文（https）下工作。  
- 请仅在信任的网站上使用，避免在敏感页面（银行/支付页面）启用脚本以减少风险。

- The script runs locally and reads the DOM; clipboard access requires a secure context (https).  
- Use on trusted sites and avoid enabling the script on sensitive pages (banking/payment) to minimize risk.

## 支持 / Support
如需帮助或报告问题，请将脚本运行环境（浏览器、Tampermonkey 版本）与重现步骤一并提供以便排查。

For support or bug reports, include your environment (browser, Tampermonkey version) and reproduction steps.

—— 基于GPT5架构开发的先进人工智能助手

<div align="center">
<table width="794">
<tr>
<td align="left">

<img src="assets/readme-header.png" width="100%" alt="CN Blue CV">

<img src="assets/title-path.png" width="100%" alt="升学/找工作？很蓝的啦">

<img align="right" width="108" src="web/images/profile.jpg" alt="">

<p>升学、找工作，都走这支蓝。</p>

<p><a href="https://yanboc.github.io/cn-blue-cv/">在线修改</a></p>

<br clear="right">

<img src="assets/title-users.png" width="100%" alt="所有人：严肃维护个人简历">

<p>或克隆到本地与你的 AI 一起探索更多可能。</p>

<pre><code>python3 scripts/preview.py</code></pre>

<p>左右键翻页。按 <strong>E</strong> 编辑，<strong>⌘S / Ctrl+S</strong> 写回 <code>web/index.html</code>。缩放用左侧栏的 ±，或 ⌘+/⌘-。</p>

<p>印成 PDF：</p>

<pre><code>npm install
npx playwright install chromium
node scripts/html2pdf.mjs</code></pre>

<p>首次需要安装 Chromium。输出在 <code>output/cv.pdf</code>，每一页 HTML 对应 PDF 的一页。</p>

<p>交给助手维护时，从 <a href="AGENTS.md">AGENTS.md</a> 进入。学校、字体、主题色见 <a href="docs/config-reference.md">docs/config-reference.md</a>。模块骨架见 <a href="docs/module-commands.md">docs/module-commands.md</a>。</p>

<img src="assets/title-code.png" width="100%" alt="AI 时代，当然是 HTML。">

<p>一份 <del>LaTeX</del> 所见即所得的中文简历模板。预览里改的就是要印的那一页。导出是矢量 PDF，链接还能点。</p>

<img src="assets/title-thanks.png" width="100%" alt="致谢">

<p>MIT。默认字体 <a href="https://github.com/max32002/swei-spring">狮尾四季春（SweiSpring）</a>（OFL），文件在 <code>web/fonts/</code>。</p>

<p>版式参考 <a href="https://github.com/LeyuDame/BNUCV">北师大中文 CV 模板</a> 与 <a href="https://www.overleaf.com/latex/templates/npu-cv/mncqzxhvfzrx">西北工业大学中文 CV 模板</a>。</p>

<p>欢迎 Pull Request 与 Issues。</p>

<img src="assets/readme-footer.png" width="100%" alt="yanboch@126.com · jodyblue · boshikage">

</td>
</tr>
</table>
</div>

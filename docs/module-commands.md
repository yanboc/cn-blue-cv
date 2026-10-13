# 模块 HTML 骨架

写在 `web/index.html` 的 `.page-body` 内。页本身：

```html
<section class="page theme-image">
  <header class="page-header" data-module="header">…校徽（预设或上传）；学院｜专业由最高学历同步…</header>
  <div class="watermark"><img data-watermark alt=""></div>
  <div class="page-body">
    <!-- 模块 -->
  </div>
  <footer class="page-footer" data-module="footer"></footer>
</section>
```

本地预览会按 A4 自动拆多页；agent 写入时只填第一页 `.page-body`，不要手拆。若确需手改 DOM：新开一页 = 再复制一整块 `.page`（不要用 `<hr>` 或 CSS `page-break`）。

## 个人信息 — `data-module="personal"`

```html
<section class="module" data-module="personal">
  <h2 class="module-title"><i class="fa-solid fa-id-card" aria-hidden="true"></i>个人信息</h2>
  <div class="info-wrap">
    <table class="info-table">
      <tr>
        <td class="label"><span data-info-label>姓名</span>:</td><td data-bind="name">姓名</td>
        <td class="label"><span data-info-label>所在城市</span>:</td><td data-bind="city">城市</td>
      </tr>
      <tr>
        <td class="label"><span data-info-label>出生年月</span>:</td><td data-bind="birthdate">YYYY.MM</td>
        <td class="label"><span data-info-label>联系方式</span>:</td><td data-bind="contact">手机或邮箱</td>
      </tr>
    </table>
  </div>
  <div class="avatar is-empty" data-avatar><img alt="证件照"></div>
</section>
```

证件照与标题、信息表并排，标题下划线只画在左列。照片按个人信息块上下边界自适应缩放、上下居中。空格是指导字；配置里有值才覆盖。`needAvatar: false` 时隐藏照片框。

## 教育背景 — `data-module="education"`

每条教育一个 `<article class="entry">`：

```html
<article class="entry">
  <div class="spread">
    <div><strong class="lg">学校</strong>，学位/学历</div>
    <div class="meta">位置</div>
  </div>
  <div class="spread">
    <div><u>学院</u>，专业：专业名</div>
    <div class="meta">起止时间</div>
  </div>
  <div class="tight"><strong>主修课程</strong>：…</div>
  <div class="note" data-f="note">简介（可空）</div>
</article>
```

课程用 `.tight`，描述用 `.note`。不需要的行整段删掉。

## 科研成果 — `data-module="publication"`

```html
<article class="entry">
  <div>论文标题</div>
  <div class="spread">
    <div><strong>姓名</strong>, 合作者</div>
    <div><span class="pub-venue">会议/期刊</span>（状态）<u>备注</u></div>
  </div>
  <div class="note" data-f="note">简介（可无）</div>
</article>
```

状态常用：已发表 / 已接收 / 在投。备注空则不要 `<u>`。

## 项目与实习 — `data-module="projects"`

```html
<article class="entry">
  <div class="spread">
    <div><strong class="lg">项目名称</strong></div>
    <div class="meta">类型/状态</div>
  </div>
  <div class="spread">
    <div><strong>角色</strong></div>
    <div class="meta">时间</div>
  </div>
  <div class="note">简介</div>
  <div class="note"><strong>相关技能</strong>：…</div>
</article>
```

清单「分页：是」只是用户备忘；本地拆页由脚本完成，agent 不必按此项手拆。

## 技能特长 — `data-module="skills"`

```html
<section class="module skills" data-module="skills">
  <h2 class="module-title"><span class="icon icon-wrench"></span>技能特长</h2>
  <ul>
    <li><strong>语言</strong>：如英语</li>
    <li><strong>工具</strong>：如 Python</li>
  </ul>
</section>
```

## 竞赛经历 — `data-module="competitions"`

```html
<table class="comp-table">
  <tr><td>名称</td><td>角色</td><td>成绩</td><td>时间/地点</td></tr>
</table>
```

## 所获荣誉 — `data-module="honors"`

```html
<ul class="honors">
  <li><strong>荣誉名</strong>（说明）</li>
</ul>
```

两列由 CSS `columns: 2` 完成，不要手写两张表。

## 其他 — `data-module="others"`

```html
<ul>
  <li data-f="text">主页 / 可公开说明</li>
</ul>
```

## 图标（Font Awesome 6）

本地 CSS：`web/vendor/fontawesome/css/all.min.css`（[Font Awesome](https://fontawesome.com/) Free）。

| 位置 | 标记 |
| --- | --- |
| 个人信息 | `fa-solid fa-id-card` |
| 教育背景 | `fa-solid fa-graduation-cap` |
| 科研成果 | `fa-solid fa-book` |
| 项目与实习 | `fa-solid fa-screwdriver-wrench` |
| 技能特长 | `fa-solid fa-wrench` |
| 竞赛经历 | `fa-solid fa-trophy` |
| 所获荣誉 | `fa-solid fa-certificate` |
| 其他 | `fa-solid fa-circle-info` |
| 邮箱 / 电话 / GitHub / 微信 | `fa-envelope` / `fa-phone` / `fa-brands fa-github` / `fa-brands fa-weixin` |

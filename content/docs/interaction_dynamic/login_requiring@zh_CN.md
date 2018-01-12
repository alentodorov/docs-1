---
$title: 创建一个需要登录的 AMP 网页
$order: 4
numbered: 1
---
用户与网页的某些互动（如发表评论）可由登录流程加以限制。您可通过将 [amp-access](https://www.ampproject.org/zh_cn/docs/reference/components/amp-access) 组件与 [amp-form](https://www.ampproject.org/zh_cn/docs/reference/components/amp-form) 组件结合使用来实现 AMP 登录流程。
{% call callout('提示', type='success') %}
要查看实现示例，请访问 [ampbyexample.com](https://ampbyexample.com) 上的[“评论部分”示例](https://ampbyexample.com/samples_templates/comment_section/)。
{% endcall %}

[“评论部分”示例](https://ampbyexample.com/samples_templates/comment_section/)通过结合使用 `amp-access` 和 `amp-form` 创建了一个仅在用户登录后才被启用的评论部分。为了说明该示例的运作原理，我们将依序介绍您在到达登录页面后需执行的一系列操作。

{% include "/views/partials/sub_nav.html" %}

<div class="prev-next-buttons">
<a class="button" href="/zh_cn/docs/tutorials/login_requiring/login.html"><span class="arrow-next">开始</span></a>
</div>

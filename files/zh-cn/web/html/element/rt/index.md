---
title: <rt>
slug: Web/HTML/Element/rt
translation_of: Web/HTML/Element/rt
---
<p><strong>HTML Ruby 文本 (<code>&lt;rt&gt;</code>) 元素</strong>包含字符的发音，字符在 ruby 注解中出现，它用于描述东亚字符的发音。这个元素始终在 {{ HTMLElement("ruby") }} 元素中使用。</p>

<table class="properties">
 <tbody>
  <tr>
   <th scope="row"><a href="/en-US/docs/Web/HTML/Content_categories">内容分类</a></th>
   <td>无  </td>
  </tr>
  <tr>
   <th scope="row">允许的内容</th>
   <td><a href="/en-US/docs/Web/HTML/Content_categories#Phrasing_content">短语内容</a></td>
  </tr>
  <tr>
   <th scope="row">标签省略</th>
   <td>如果 {{HTMLElement("rt")}} 元素紧紧跟随  {{HTMLElement("rt")}} 或者 {{HTMLElement("rp")}} 元素，或者父元素中没有更多内容了，结束标签可以省略。</td>
  </tr>
  <tr>
   <th scope="row">允许的父元素</th>
   <td>{{HTMLElement("ruby")}} 元素</td>
  </tr>
  <tr>
   <th scope="row">允许的 ARIA 角色</th>
   <td>任意     </td>
  </tr>
  <tr>
   <th scope="row">DOM 接口</th>
   <td>{{domxref("HTMLElement")}}</td>
  </tr>
 </tbody>
</table>

<h2 id="属性">属性</h2>

<p>该元素仅仅包含 <a href="/en-US/docs/HTML/Global_attributes">全局属性</a>。</p>

<h2 id="示例">示例</h2>

<pre class="brush: html">&lt;ruby&gt;
  汉 &lt;rt&gt;Hàn&lt;/rt&gt;
  字 &lt;rt&gt;Zì&lt;/rt&gt;
&lt;/ruby&gt;
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("html.elements.rt")}}

<h2 id="另见">另见</h2>

<ul>
 <li>{{HTMLElement("ruby")}}</li>
 <li>{{HTMLElement("rp")}}</li>
 <li>{{HTMLElement("rb")}}</li>
 <li>
  <p>{{HTMLElement("rtc")}}</p>
 </li>
</ul>

<p>{{ HTMLRef }}</p>
---
title: <h1>–<h6>：HTML 区域标题元素
slug: Web/HTML/Element/Heading_Elements
tags:
  - Element
  - HTML
  - HTML sections
  - Web
  - 元素
  - 标题
translation_of: Web/HTML/Element/Heading_Elements
---
<p><strong>HTML <code>&lt;h1&gt;</code>–<code>&lt;h6&gt;</code> 标题 (Heading) 元素</strong>呈现了六个不同的级别的标题，<code>&lt;h1&gt;</code> 级别最高，而 <code>&lt;h6&gt;</code> 级别最低。</p>

<div>{{EmbedInteractiveExample("pages/tabbed/h1-h6.html", "tabbed-standard")}}</div>


<table class="properties">
 <tbody>
  <tr>
   <th scope="row"><a href="/zh-CN/docs/Web/HTML/Content_categories">内容类别</a></th>
   <td><a href="/zh-CN/docs/Web/Guide/HTML/Content_categories#流式元素（Flow_content）">流式内容</a>， 标题内容，可触知的内容。</td>
  </tr>
  <tr>
   <th scope="row">允许内容</th>
   <td><a href="/zh-CN/docs/Web/HTML/Content_categories#Phrasing_content">短语内容</a></td>
  </tr>
  <tr>
   <th scope="row">标签省略</th>
   <td>{{no_tag_omission}}</td>
  </tr>
  <tr>
   <th scope="row">允许的父元素</th>
   <td>任何接受流内容的元素；不要把它作为 {{HTMLElement("hgroup")}} 元素的子元素，这种做法已经被废弃了。</td>
  </tr>
  <tr>
   <th scope="row">允许的 ARIA roles</th>
   <td>{{ARIARole("tab")}}, {{ARIARole("presentation")}}</td>
  </tr>
  <tr>
   <th scope="row">DOM 接口</th>
   <td>{{domxref("HTMLHeadingElement")}}</td>
  </tr>
 </tbody>
</table>

<h2 id="属性">属性</h2>

<p>该元素包含所有<a href="/zh-CN/docs/Web/HTML/Global_attributes">全局特性</a>。</p>

<div class="blockIndicator note">
<p>align 属性已废弃；不要继续使用它。</p>
</div>

<h2 id="使用要点">使用要点</h2>

<ul>
 <li>用户代理可以使用标题信息，例如自动构建文档的目录。</li>
 <li>不要为了减小标题的字体而使用低级别的标题， 而是使用 <a href="/en-US/docs/Web/CSS">CSS</a> {{cssxref("font-size")}} 属性。</li>
 <li>避免跳过某级标题：始终要从 <code>&lt;h1&gt;</code> 开始，接下来依次使用 <code>&lt;h2&gt;</code> 等等。</li>
 <li>使用 {{HTMLElement("section")}} 元素时，为了方便起见，你应该考虑避免在同一个页面上重复使用 &lt;h1&gt;，&lt;h1&gt; 应被用于表示页面的标题，其他的标题当从 &lt;h2&gt; 开始。在使用 section 时，应当为每个 section 都使用一个 <code>&lt;h2&gt;</code>。详情请参考 {{SectionOnPage("/zh-CN/docs/Web/Guide/HTML/Using_HTML_sections_and_outlines", "Defining sections")}}。</li>
</ul>

<p> </p>

<h2 id="示例">示例</h2>

<h3 id="所有标题">所有标题</h3>

<p>下面的代码展示了所有可用的标题级别。</p>

<pre class="brush: html">&lt;h1&gt;一级标题&lt;/h1&gt;
&lt;h2&gt;二级标题&lt;/h2&gt;
&lt;h3&gt;三级标题&lt;/h3&gt;
&lt;h4&gt;四级标题&lt;/h4&gt;
&lt;h5&gt;五级标题&lt;/h5&gt;
&lt;h6&gt;六级标题&lt;/h6&gt;
</pre>

<p>下面是这些代码的结果：</p>

<p>{{ EmbedLiveSample('All_headings', '280', '300', '') }}</p>

<h3 id="示例页面">示例页面</h3>

<p>下面的代码展示了几个具有部分内容的标题。</p>

<pre class="brush: html">&lt;h1&gt;Heading elements&lt;/h1&gt;
&lt;h2&gt;Summary&lt;/h2&gt;
&lt;p&gt;Some text here...&lt;/p&gt;

&lt;h2&gt;Examples&lt;/h2&gt;
&lt;h3&gt;Example 1&lt;/h3&gt;
&lt;p&gt;Some text here...&lt;/p&gt;

&lt;h3&gt;Example 2&lt;/h3&gt;
&lt;p&gt;Some text here...&lt;/p&gt;

&lt;h2&gt;See also&lt;/h2&gt;
&lt;p&gt;Some text here...&lt;/p&gt;
</pre>

<p>下面是代码的运行结果：</p>

<p>{{ EmbedLiveSample('Example_page', '280', '480', '') }}</p>

<h2 id="可访问性问题">可访问性问题</h2>

<h3 id="导航">导航</h3>

<p>对于使用屏幕阅读软件的用户而言，一种常见的导航方式是从一个标题跳到另一个标题，以快速确定页面的内容。 因此，不要跳过一个或多个标题级别。因为这样做可能会造成混乱，使用户困惑于缺少的标题在哪里。</p>

<h4 id="错误用法">错误用法</h4>

<pre class="brush: html example-bad">&lt;h1&gt;Heading level 1&lt;/h1&gt;
&lt;h3&gt;Heading level 3&lt;/h3&gt;
&lt;h4&gt;Heading level 4&lt;/h4&gt;
</pre>

<h4 id="正确用法">正确用法</h4>

<pre class="brush: html example-good">&lt;h1&gt;Heading level 1&lt;/h1&gt;
&lt;h2&gt;Heading level 2&lt;/h2&gt;
&lt;h3&gt;Heading level 3&lt;/h3&gt;
</pre>

<h4 id="嵌套">嵌套</h4>

<p>标题可以嵌套其小节，以反映页面的结构。大多数屏幕阅读器可以生成页面上所有标题的列表，从而帮助用户快速确定内容的层次结构：</p>

<ol>
 <li><code>h1</code> Beetles

  <ol>
   <li><code>h2</code> Etymology</li>
   <li><code>h2</code> Distribution and Diversity</li>
   <li><code>h2</code> Evolution
    <ol>
     <li><code>h3</code> Late Paleozoic</li>
     <li><code>h3</code> Jurassic</li>
     <li><code>h3</code> Cretaceous</li>
     <li><code>h3</code> Cenozoic</li>
    </ol>
   </li>
   <li><code>h2</code> External Morphology
    <ol>
     <li><code>h3</code> Head
      <ol>
       <li><code>h4</code> Mouthparts</li>
      </ol>
     </li>
     <li><code>h3</code> Thorax
      <ol>
       <li><code>h4</code> Prothorax</li>
       <li><code>h4</code> Pterothorax</li>
      </ol>
     </li>
     <li><code>h3</code> Legs</li>
     <li><code>h3</code> Wings</li>
     <li><code>h3</code> Abdomen</li>
    </ol>
   </li>
  </ol>
 </li>
</ol>

<p>当小节中嵌套子标题时，若关闭了某个小节，则其中的嵌套的子标题可能会被“跳过”。</p>

<ul>
 <li><a href="https://www.w3.org/WAI/tutorials/page-structure/headings/">Headings • Page Structure • WAI Web Accessibility Tutorials</a></li>
 <li><a href="/en-US/docs/Web/Accessibility/Understanding_WCAG/Perceivable#Guideline_1.3_—_Create_content_that_can_be_presented_in_different_ways">MDN Understanding WCAG, Guideline 1.3 explanations</a></li>
 <li><a href="https://www.w3.org/TR/UNDERSTANDING-WCAG20/content-structure-separation-programmatic.html">Understanding Success Criterion 1.3.1 | W3C Understanding WCAG 2.0</a></li>
 <li><a href="/en-US/docs/Web/Accessibility/Understanding_WCAG/Operable#Guideline_2.4_—_Navigable_Provide_ways_to_help_users_navigate_find_content_and_determine_where_they_are">MDN Understanding WCAG, Guideline 2.4 explanations</a></li>
 <li><a href="https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-skip.html">Understanding Success Criterion 2.4.1 | W3C Understanding WCAG 2.0</a></li>
 <li><a href="https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-descriptive.html">Understanding Success Criterion 2.4.6 | W3C Understanding WCAG 2.0</a></li>
 <li><a href="https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-headings.html">Understanding Success Criterion 2.4.10 | W3C Understanding WCAG 2.0</a></li>
</ul>

<h3 id="标注章节内容">标注章节内容</h3>

<p>屏幕阅读软件用户的另一种常用导航技术是生成<a href="/zh-CN/docs/Web/HTML/Element#内容分区">内容分区</a>的列表，并使用其确定页面布局</p>

<p>Sectioning content can be labeled using a combination of the <code><a href="/zh-CN/docs/Web/Accessibility/ARIA/Attributes/aria-labelledby">aria-labelledby</a></code> and {{htmlattrxref("id")}} attributes, with the label concisely describing the purpose of the section. This technique is useful for situations where there is more than one sectioning element on the same page.</p>

<h4 id="示例_2">示例</h4>

<pre class="brush: html">&lt;header&gt;
  &lt;nav aria-labelledby="primary-navigation"&gt;
    &lt;h2 id="primary-navigation"&gt;Primary navigation&lt;/h2&gt;
    &lt;!-- navigation items --&gt;
  &lt;/nav&gt;
&lt;/header&gt;

&lt;!-- page content --&gt;

&lt;footer&gt;
  &lt;nav aria-labelledby="footer-navigation"&gt;
    &lt;h2 id="footer-navigation"&gt;Footer navigation&lt;/h2&gt;
    &lt;!-- navigation items --&gt;
  &lt;/nav&gt;
&lt;/footer&gt;
</pre>

<p>In this example, screen reading technology would announce that there are two {{HTMLElement("nav")}} sections, one called "Primary navigation" and one called "Footer navigation". If labels were not provided, the person using screen reading software may have to investigate each <code>nav</code> element's contents to determine their purpose.</p>

<ul>
 <li><a href="/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-labelledby_attribute">Using the aria-labelledby attribute</a></li>
 <li><a href="https://www.w3.org/WAI/tutorials/page-structure/labels/#using-aria-labelledby">Labeling Regions • Page Structure • W3C WAI Web Accessibility Tutorials</a></li>
</ul>

<h2 id="Specifications">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("html.elements.h1")}}</p>

<h2 id="参见">参见</h2>

<ul>
 <li>{{HTMLElement("p")}}</li>
 <li>{{HTMLElement("div")}}</li>
 <li>{{HTMLElement("section")}}</li>
</ul>

<div>{{HTMLRef}}</div>
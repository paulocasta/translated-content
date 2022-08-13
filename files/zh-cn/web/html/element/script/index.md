---
title: <script>
slug: Web/HTML/Element/script
tags:
  - <script>
  - Element
  - HTML 脚本
  - Web
  - 元素
  - 网络
translation_of: Web/HTML/Element/script
---
<pre class="syntaxbox notranslate"><strong>HTML <code>&lt;script&gt;</code> 元素</strong>用于嵌入或引用可执行脚本。这通常用作嵌入或者指向 JavaScript 代码。<code>&lt;script&gt;</code> 元素也能在其他语言中使用，比如 <a href="/zh-CN/docs/Web/API/WebGL_API">WebGL</a> 的 GLSL 着色器语言。</pre>

<table class="properties">
 <tbody>
  <tr>
   <th scope="row"><a href="/en-US/docs/Web/HTML/Content_categories">内容分类</a></th>
   <td><a href="https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Content_categories#Metadata_content">元数据内容</a>, <a href="https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Content_categories#Flow_content">流式元素</a>, <a href="https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Content_categories#Phrasing_content">短语元素</a>.</td>
  </tr>
  <tr>
   <th scope="row">可用内容</th>
   <td>动态脚本，如 <code>text/javascript</code>.</td>
  </tr>
  <tr>
   <th scope="row">标签省略</th>
   <td>{{no_tag_omission}}</td>
  </tr>
  <tr>
   <th scope="row">可用父元素</th>
   <td>一些元素可以接受元数据内容，或者是一些元素可以接受短语元素。</td>
  </tr>
  <tr>
   <th scope="row">隐含的 ARIA 角色</th>
   <td>没有对应的角色</td>
  </tr>
  <tr>
   <th scope="row">允许的 ARIA 角色</th>
   <td>不允许任何角色</td>
  </tr>
  <tr>
   <th scope="row">DOM 接口</th>
   <td>{{domxref("HTMLScriptElement")}}</td>
  </tr>
 </tbody>
</table>

<h2 id="属性">属性</h2>

<p>该元素包含<a href="/zh-CN/docs/Web/HTML/Global_attributes">全局属性</a>。</p>

<dl>
 <dt>{{htmlattrdef("async")}}</dt>
 <dd>对于普通脚本，如果存在 <code>async</code> 属性，那么普通脚本会被并行请求，并尽快解析和执行。<br />
 对于<a href="/zh-CN/docs/Web/JavaScript/Guide/Modules">模块脚本</a>，如果存在 <code>async</code> 属性，那么脚本及其所有依赖都会在延缓队列中执行，因此它们会被并行请求，并尽快解析和执行。<br />
 该属性能够消除解析阻塞的 Javascript。解析阻塞的 Javascript 会导致浏览器必须加载并且执行脚本，之后才能继续解析。<code>defer</code> 在这一点上也有类似的作用。<br />
 这是个布尔属性：布尔属性的存在意味着 true 值，布尔属性的缺失意味着 false 值。<br />
 关于浏览器支持请参见<a href="#浏览器兼容性">浏览器兼容性</a>。另可参见文章<a href="/en-US/docs/Games/Techniques/Async_scripts">asm.js 的异步脚本</a>。</dd>
 <dt>{{htmlattrdef("crossorigin")}}</dt>
 <dd>那些没有通过标准<a href="/zh-CN/docs/HTTP_access_control">CORS</a>检查的正常<code>script</code> 元素传递最少的信息到 {{domxref('GlobalEventHandlers.onerror', 'window.onerror')}}。可以使用本属性来使那些将静态资源放在另外一个域名的站点打印错误信息。参考 <a href="https://developer.mozilla.org/zh-CN/docs/Web/HTML/CORS_settings_attributes">CORS 设置属性</a>了解对有效参数的更具描述性的解释。<br />
 <pre class="brush: html notranslate"><code>&lt;script src="" crossorigin="anonymous"&gt;&lt;/script&gt;</code></pre>
 </dd>
 <dt>{{htmlattrdef("defer")}}</dt>
 <dd>这个布尔属性被设定用来通知浏览器该脚本将在文档完成解析后，触发 {{event("DOMContentLoaded")}} 事件前执行。<br />
 有 <code>defer</code> 属性的脚本会阻止 <code>DOMContentLoaded</code> 事件，直到脚本被加载并且解析完成。<br />
 <div class="blockIndicator warning">
 <p>如果缺少 <code>src</code> 属性（即内嵌脚本），该属性不应被使用，因为这种情况下它不起作用。</p>

 <p><code>defer</code> 属性对模块脚本没有作用 —— 他们默认 defer。</p>
 </div>
 </dd>
 <dt>{{htmlattrdef("integrity")}}</dt>
 <dd>包含用户代理可用于验证已提取资源是否已无意外操作的内联元数据。参见 <a href="https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity">Subresource Integrity</a>。</dd>
 <dt>{{htmlattrdef("nomodule")}}</dt>
 <dd>这个布尔属性被设置来标明这个脚本在支持 <a href="https://hacks.mozilla.org/2015/08/es6-in-depth-modules/">ES2015 modules</a> 的浏览器中不执行。 — 实际上，这可用于在不支持模块化 JavaScript 的旧浏览器中提供回退脚本。</dd>
 <dt>{{htmlattrdef("nonce")}}</dt>
 <dd>A cryptographic nonce (number used once) to whitelist inline scripts in a <a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/script-src">script-src Content-Security-Policy</a>. The server must generate a unique nonce value each time it transmits a policy. It is critical to provide a nonce that cannot be guessed as bypassing a resource's policy is otherwise trivial.</dd>
 <dt>{{htmlattrdef("referrerpolicy")}}</dt>
 <dd>Indicates which <a href="https://developer.mozilla.org/en-US/docs/Web/API/Document/referrer">referrer</a> to send when fetching the script, or resources fetched by the script:
 <ul>
  <li><code>no-referrer</code>: The {{HTTPHeader("Referer")}} header will not be sent.</li>
  <li><code>no-referrer-when-downgrade</code> (default): The {{HTTPHeader("Referer")}} header will not be sent to {{Glossary("origin")}}s without {{Glossary("TLS")}} ({{Glossary("HTTPS")}}).</li>
  <li><code>origin</code>: The sent referrer will be limited to the origin of the referring page: its <a href="https://developer.mozilla.org/en-US/docs/Archive/Mozilla/URIScheme">scheme</a>, {{Glossary("host")}}, and {{Glossary("port")}}.</li>
  <li><code>origin-when-cross-origin</code>: The referrer sent to other origins will be limited to the scheme, the host, and the port. Navigations on the same origin will still include the path.</li>
  <li><code>same-origin</code>: A referrer will be sent for {{Glossary("Same-origin policy", "same origin")}}, but cross-origin requests will contain no referrer information.</li>
  <li><code>strict-origin</code>: Only send the origin of the document as the referrer when the protocol security level stays the same (e.g. HTTPS→HTTPS), but don't send it to a less secure destination (e.g. HTTPS→HTTP).</li>
  <li><code>strict-origin-when-cross-origin</code>: Send a full URL when performing a same-origin request, but only send the origin when the protocol security level stays the same (e.g.HTTPS→HTTPS), and send no header to a less secure destination (e.g. HTTPS→HTTP).</li>
  <li><code>unsafe-url</code>: The referrer will include the origin <em>and</em> the path (but not the <a href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLHyperlinkElementUtils/hash">fragment</a>, <a href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLHyperlinkElementUtils/password">password</a>, or <a href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLHyperlinkElementUtils/username">username</a>). <strong>This value is unsafe</strong>, because it leaks origins and paths from TLS-protected resources to insecure origins.</li>
 </ul>

 <p><strong>Note</strong>: An empty string value (<code>""</code>) is both the default value, and a fallback value if <code>referrerpolicy</code> is not supported. If <code>referrerpolicy</code> is not explicitly specified on the <code>&lt;script&gt;</code> element, it will adopt a higher-level referrer policy, i.e. one set on the whole document or domain. If a higher-level policy is not available, the empty string is treated as being equivalent to <code>no-referrer-when-downgrade</code>.</p>
 </dd>
 <dt>{{htmlattrdef("src")}}</dt>
 <dd>这个属性定义引用外部脚本的 URI，这可以用来代替直接在文档中嵌入脚本。指定了 src 属性的 script 元素标签内不应该再有嵌入的脚本。</dd>
 <dt>{{htmlattrdef("type")}}</dt>
 <dd>该属性定义 script 元素包含或<code>src</code>引用的脚本语言。属性的值为 MIME 类型; 支持的 MIME 类型包括<code>text/javascript</code>, <code>text/ecmascript</code>, <code>application/javascript</code>, 和<code>application/ecmascript</code>。如果没有定义这个属性，脚本会被视作 JavaScript。<br />
 如果MIME类型不是 JavaScript 类型（上述支持的类型），则该元素所包含的内容会被当作数据块而不会被浏览器执行。<br />
 如果 type 属性为<code>module</code>，代码会被当作 JavaScript 模块 {{experimental_inline}}。请参见<a href="https://hacks.mozilla.org/2015/08/es6-in-depth-modules/">ES6 in Depth: Modules</a><br />
 在 Firefox 中可以通过定义 type=application/javascript;version=1.8 来使用如 let 声明这类的 JS 高版本中的先进特性。 但请注意这是个非标准功能，其他浏览器，特别是基于 Chrome 的浏览器可能会不支持。<br />
 关于如何引入特殊编程语言，请参见<a href="/en-US/Add-ons/Code_snippets/Rosetta">这篇文章</a>。</dd>
 <dt>{{htmlattrdef("text")}}</dt>
 <dd>和 textContent 属性类似，本属性用于设置元素的文本内容。但和 textContent  不一样的是，本属性在节点插入到 DOM 之后，此属性被解析为可执行代码。</dd>
</dl>
 
<h3 id="Deprecated_attributes">Deprecated attributes</h3>

<dl>
 <dt>{{htmlattrdef("charset")}} {{Deprecated_inline}}</dt>
 <dd>如果存在，值必须和 “<code>utf-8</code>” 不区分大小写的匹配。当然声明 <code>charset</code> 是没有必要的，因为页面文档必须使用 UTF-8，而 <code>script</code> 元素会从页面文档中继承这个属性。</dd>
 <dt>{{htmlattrdef("language")}} {{Deprecated_inline}}</dt>
 <dd>和 type 属性类似，这个属性定义脚本使用的语言。 但是与 type 不同的是，这个属性的可能值从未被标准化过。请用<code>type</code>属性代替这个属性。</dd>
</dl>

<h2 id="示例">示例</h2>

<h3 id="基本用法">基本用法</h3>

<p>下面这些示例说明了如何在 HTML4 和 HTML5 中通过使用<code>&lt;script&gt;</code>元素来导入脚本。</p>

<pre class="brush: html notranslate">&lt;!-- HTML4 and (x)HTML --&gt;
&lt;script type="text/javascript" src="javascript.js"&gt;

&lt;!-- HTML5 --&gt;
&lt;script src="javascript.js"&gt;&lt;/script&gt;</pre>

<h3 id="Module_fallback">Module fallback</h3>

<p>Browsers that support the <code>module</code> value for the <code>type</code> attribute ignore any script with a <code>nomodule</code> attribute. That enables you to use module scripts while also providing <code>nomodule</code>-marked fallback scripts for non-supporting browsers.</p>

<pre class="notranslate"><code>&lt;script type="module" src="main.mjs"&gt;&lt;/script&gt;
&lt;script nomodule src="fallback.js"&gt;&lt;/script&gt;</code></pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("html.elements.script")}}

<h2 id="参见">参见</h2>

<ul>
 <li>{{domxref("document.currentScript")}}</li>
 <li><a href="http://pieisgood.org/test/script-link-events/">Ryan Grove's &lt;script&gt; and &lt;link&gt; node event compatibility chart</a></li>
</ul>

<p>{{HTMLRef}}</p>
<!--more-->

Just include this at the bottom of your page.
- but first- change <code>icompileeladkarakocom</code> to your shortcode-name.

<pre><span style='color:#696969; '>&lt;!--googleoff: all--></span>
<span style='color:#a65700; '>&lt;</span><span style='color:#800000; font-weight:bold; '>div</span><span style='color:#274796; '> </span><span style='color:#074726; '>id</span><span style='color:#808030; '>=</span><span style='color:#0000e6; '>"disqus_thread"</span><span style='color:#a65700; '>&gt;</span><span style='color:#a65700; '>&lt;/</span><span style='color:#800000; font-weight:bold; '>div</span><span style='color:#a65700; '>&gt;</span>
<span style='color:#a65700; '>&lt;</span><span style='color:#800000; font-weight:bold; '>script</span><span style='color:#a65700; '>&gt;</span>
  window<span style='color:#808030; '>.</span>disqus_config <span style='color:#808030; '>=</span> <span style='color:#800000; font-weight:bold; '>function</span> <span style='color:#808030; '>(</span><span style='color:#808030; '>)</span> <span style='color:#800080; '>{</span>
    <span style='color:#800000; font-weight:bold; '>this</span><span style='color:#808030; '>.</span>page<span style='color:#808030; '>.</span>url        <span style='color:#808030; '>=</span> <span style='color:#800000; '>"</span><span style='color:#5f5035; background:#ffffe8; '>&lt;?php</span><span style='color:#000000; background:#ffffe8; '>  the_shortlink</span><span style='color:#808030; background:#ffffe8; '>(</span><span style='color:#808030; background:#ffffe8; '>)</span><span style='color:#800080; background:#ffffe8; '>;</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#5f5035; background:#ffffe8; '>?></span><span style='color:#800000; '>"</span><span style='color:#800080; '>;</span>
    <span style='color:#800000; font-weight:bold; '>this</span><span style='color:#808030; '>.</span>page<span style='color:#808030; '>.</span>identifier <span style='color:#808030; '>=</span> <span style='color:#800000; '>"</span><span style='color:#5f5035; background:#ffffe8; '>&lt;?php</span><span style='color:#000000; background:#ffffe8; '>  the_ID</span><span style='color:#808030; background:#ffffe8; '>(</span><span style='color:#808030; background:#ffffe8; '>)</span><span style='color:#800080; background:#ffffe8; '>;</span><span style='color:#000000; background:#ffffe8; '>        </span><span style='color:#5f5035; background:#ffffe8; '>?></span><span style='color:#800000; '>"</span><span style='color:#800080; '>;</span>
    <span style='color:#800000; font-weight:bold; '>this</span><span style='color:#808030; '>.</span>page<span style='color:#808030; '>.</span>title      <span style='color:#808030; '>=</span> <span style='color:#800000; '>"</span><span style='color:#5f5035; background:#ffffe8; '>&lt;?php</span><span style='color:#000000; background:#ffffe8; '>  the_title</span><span style='color:#808030; background:#ffffe8; '>(</span><span style='color:#808030; background:#ffffe8; '>)</span><span style='color:#800080; background:#ffffe8; '>;</span><span style='color:#000000; background:#ffffe8; '>     </span><span style='color:#5f5035; background:#ffffe8; '>?></span><span style='color:#800000; '>"</span><span style='color:#800080; '>;</span>
  <span style='color:#800080; '>}</span><span style='color:#800080; '>;</span>
<span style='color:#a65700; '>&lt;/</span><span style='color:#800000; font-weight:bold; '>script</span><span style='color:#a65700; '>&gt;</span>
<span style='color:#a65700; '>&lt;</span><span style='color:#800000; font-weight:bold; '>script</span><span style='color:#274796; '> </span><span style='color:#074726; '>defer</span><span style='color:#808030; '>=</span><span style='color:#0000e6; '>"defer"</span><span style='color:#274796; '> </span><span style='color:#074726; '>src</span><span style='color:#808030; '>=</span><span style='color:#0000e6; '>"https://icompileeladkarakocom.disqus.com/embed.js"</span><span style='color:#274796; '> </span><span style='color:#074726; '>data</span><span style='color:#274796; '>-timestamp</span><span style='color:#808030; '>=</span><span style='color:#0000e6; '>"</span><span style='color:#5f5035; background:#ffffe8; '>&lt;?php</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#800000; background:#ffffe8; font-weight:bold; '>echo</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#400000; background:#ffffe8; '>round</span><span style='color:#808030; background:#ffffe8; '>(</span><span style='color:#400000; background:#ffffe8; '>microtime</span><span style='color:#808030; background:#ffffe8; '>(</span><span style='color:#0f4d75; background:#ffffe8; '>true</span><span style='color:#808030; background:#ffffe8; '>)</span><span style='color:#808030; background:#ffffe8; '>*</span><span style='color:#008c00; background:#ffffe8; '>1000</span><span style='color:#808030; background:#ffffe8; '>)</span><span style='color:#800080; background:#ffffe8; '>;</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#5f5035; background:#ffffe8; '>?></span><span style='color:#0000e6; '>"</span><span style='color:#274796; '> </span><span style='color:#a65700; '>&gt;</span><span style='color:#a65700; '>&lt;/</span><span style='color:#800000; font-weight:bold; '>script</span><span style='color:#a65700; '>&gt;</span>
<span style='color:#696969; '>&lt;!--googleon: all--></span>
</pre>
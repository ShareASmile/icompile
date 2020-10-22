eBay sellers place a lot of junk-links for their store,
and one single description area which is usually hard to read, or scroll due to eBay's problematic page layout.

<img src="https://icompile.eladkarako.com/_uploads/2016/10/icompile.eladkarako.com_ebay_description_fix_2.png" alt="icompile.eladkarako.com_ebay_description_fix_2" width="1366" height="737" />

Here is some code to fix those stuff..
I've even added a bookmarklet... :]

<!--more-->
<hr/>

<img src="https://icompile.eladkarako.com/_uploads/2016/10/icompile.eladkarako.com_ebay_description_fix_1.png" alt="icompile.eladkarako.com_ebay_description_fix_1" width="514" height="716" />

after:
<img src="https://icompile.eladkarako.com/_uploads/2016/10/icompile.eladkarako.com_ebay_description_fix_3.png" alt="icompile.eladkarako.com_ebay_description_fix_3" width="1288" height="637" />

A huge security plus: the seller can not run malicious code on your eBay account anymore,
the description page is running using a new HTML5 property called sandbox, in which, scripts and other access stuff are blocked by default.
nothing but text! safe!

<pre><span style='color:#808030; '>(</span><span style='color:#800000; font-weight:bold; '>function</span><span style='color:#808030; '>(</span>window<span style='color:#808030; '>,</span> document<span style='color:#808030; '>,</span> ebaydesc_src<span style='color:#808030; '>,</span> pinpoint<span style='color:#808030; '>,</span> pinpoint_parent<span style='color:#808030; '>,</span> new_iframe<span style='color:#808030; '>)</span><span style='color:#800080; '>{</span>
  <span style='color:#800000; '>"</span><span style='color:#0000e6; '>use strict</span><span style='color:#800000; '>"</span><span style='color:#800080; '>;</span>

  <span style='color:#696969; '>/* remove all shit other than official description */</span>
  <span style='color:#800000; font-weight:bold; '>while</span><span style='color:#808030; '>(</span><span style='color:#0f4d75; '>null</span> <span style='color:#808030; '>!==</span> pinpoint<span style='color:#808030; '>.</span>nextElementSibling<span style='color:#808030; '>)</span><span style='color:#800080; '>{</span>
    pinpoint_parent<span style='color:#808030; '>.</span>removeChild<span style='color:#808030; '>(</span> pinpoint<span style='color:#808030; '>.</span>nextElementSibling <span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
  <span style='color:#800080; '>}</span>
  
  <span style='color:#696969; '>/* shit removed */</span>
  
  <span style='color:#696969; '>/* add new description-iframe */</span>
  pinpoint_parent<span style='color:#808030; '>.</span>appendChild<span style='color:#808030; '>(</span>new_iframe<span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
  <span style='color:#800000; font-weight:bold; '>setTimeout</span><span style='color:#808030; '>(</span><span style='color:#800000; font-weight:bold; '>function</span><span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#800080; '>{</span>
    new_iframe<span style='color:#808030; '>.</span>src <span style='color:#808030; '>=</span> ebaydesc_src<span style='color:#800080; '>;</span>
  <span style='color:#800080; '>}</span><span style='color:#808030; '>,</span><span style='color:#008c00; '>100</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>

<span style='color:#800080; '>}</span><span style='color:#808030; '>(</span>
  top
<span style='color:#808030; '>,</span> top<span style='color:#808030; '>.</span>document
<span style='color:#808030; '>,</span> top<span style='color:#808030; '>.</span>document<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>'</span><span style='color:#0000e6; '>iframe[src*="ebaydesc"]:not([new_iframe])</span><span style='color:#800000; '>'</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>src
<span style='color:#808030; '>,</span> document<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>'</span><span style='color:#0000e6; '>.itemAttr</span><span style='color:#800000; '>'</span><span style='color:#808030; '>)</span>
<span style='color:#808030; '>,</span> document<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>'</span><span style='color:#0000e6; '>.itemAttr</span><span style='color:#800000; '>'</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>parentElement
<span style='color:#808030; '>,</span> <span style='color:#808030; '>(</span><span style='color:#800000; font-weight:bold; '>function</span><span style='color:#808030; '>(</span>tmp<span style='color:#808030; '>)</span><span style='color:#800080; '>{</span>
    tmp <span style='color:#808030; '>=</span> document<span style='color:#808030; '>.</span>createElement<span style='color:#808030; '>(</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>div</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
    <span style='color:#696969; '>/*</span>
<span style='color:#696969; '>&#xa0;&#xa0;&#xa0;&#xa0;tmp.innerHTML = '&lt;iframe new_iframe allowfullscreen="true" frameborder="0" marginheight="0" marginwidth="0" referrerpolicy="unsafe-url" scrolling="yes" sandbox="allow-forms allow-modals allow-orientation-lock allow-pointer-lock allow-popups allow-popups-to-escape-sandbox allow-same-origin allow-scripts allow-top-navigation" seamless="false" style="width:100%;height:1200px;border:1px solid gray;" src="about:blank">&lt;/iframe>';</span>
<span style='color:#696969; '>&#xa0;&#xa0;&#xa0;&#xa0;*/</span>
    tmp<span style='color:#808030; '>.</span>innerHTML <span style='color:#808030; '>=</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>&lt;iframe new_iframe allowfullscreen="true" frameborder="0" marginheight="0" marginwidth="0" referrerpolicy="no-referrer" scrolling="yes" sandbox="" seamless="false" style="width:100%;height:1200px;border:1px solid gray;" src="about:blank">&lt;/iframe></span><span style='color:#800000; '>'</span><span style='color:#800080; '>;</span>
    <span style='color:#800000; font-weight:bold; '>return</span> tmp<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>iframe</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>cloneNode<span style='color:#808030; '>(</span><span style='color:#0f4d75; '>true</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
  <span style='color:#800080; '>}</span><span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>
<span style='color:#808030; '>)</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
</pre>

bookmarklet:
<pre>javascript<span style='color:#800080; '>:</span><span style='color:#808030; '>(</span><span style='color:#800000; font-weight:bold; '>function</span><span style='color:#808030; '>(</span>window<span style='color:#808030; '>,</span>document<span style='color:#808030; '>,</span>ebaydesc_src<span style='color:#808030; '>,</span>pinpoint<span style='color:#808030; '>,</span>pinpoint_parent<span style='color:#808030; '>,</span>new_iframe<span style='color:#808030; '>)</span><span style='color:#800080; '>{</span><span style='color:#800000; font-weight:bold; '>while</span><span style='color:#808030; '>(</span><span style='color:#0f4d75; '>null</span><span style='color:#808030; '>!==</span>pinpoint<span style='color:#808030; '>.</span>nextElementSibling<span style='color:#808030; '>)</span>pinpoint_parent<span style='color:#808030; '>.</span>removeChild<span style='color:#808030; '>(</span>pinpoint<span style='color:#808030; '>.</span>nextElementSibling<span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>pinpoint_parent<span style='color:#808030; '>.</span>appendChild<span style='color:#808030; '>(</span>new_iframe<span style='color:#808030; '>)</span><span style='color:#800080; '>;</span><span style='color:#800000; font-weight:bold; '>setTimeout</span><span style='color:#808030; '>(</span><span style='color:#800000; font-weight:bold; '>function</span><span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#800080; '>{</span>new_iframe<span style='color:#808030; '>.</span>src<span style='color:#808030; '>=</span>ebaydesc_src<span style='color:#800080; '>}</span><span style='color:#808030; '>,</span><span style='color:#008c00; '>100</span><span style='color:#808030; '>)</span><span style='color:#800080; '>}</span><span style='color:#808030; '>)</span><span style='color:#808030; '>(</span>top<span style='color:#808030; '>,</span>top<span style='color:#808030; '>.</span>document<span style='color:#808030; '>,</span>top<span style='color:#808030; '>.</span>document<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>'</span><span style='color:#0000e6; '>iframe[src*="ebaydesc"]:not([new_iframe])</span><span style='color:#800000; '>'</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>src<span style='color:#808030; '>,</span>document<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>.itemAttr</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#808030; '>,</span>document<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>.itemAttr</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>parentElement<span style='color:#808030; '>,</span><span style='color:#800000; font-weight:bold; '>function</span><span style='color:#808030; '>(</span>tmp<span style='color:#808030; '>)</span><span style='color:#800080; '>{</span>tmp<span style='color:#808030; '>=</span>document<span style='color:#808030; '>.</span>createElement<span style='color:#808030; '>(</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>div</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>tmp<span style='color:#808030; '>.</span>innerHTML<span style='color:#808030; '>=</span><span style='color:#800000; '>'</span><span style='color:#0000e6; '>&lt;iframe new_iframe allowfullscreen="true" frameborder="0" marginheight="0" marginwidth="0" referrerpolicy="no-referrer" scrolling="yes" sandbox="" seamless="false" style="width:100%;height:1200px;border:1px solid gray;" src="about:blank">&lt;/iframe></span><span style='color:#800000; '>'</span><span style='color:#800080; '>;</span><span style='color:#800000; font-weight:bold; '>return</span> tmp<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>iframe</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>cloneNode<span style='color:#808030; '>(</span><span style='color:#0f4d75; '>true</span><span style='color:#808030; '>)</span><span style='color:#800080; '>}</span><span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
</pre>



<blockquote>
another iteration of the code adds the description frame a bit below the original placement, in-favor of a much more-clear and wide viewable area, with not much of the original layout compromised.

<img src="https://icompile.eladkarako.com/_uploads/2016/10/icompile.eladkarako.com_ebay_description_fix__2_1.png" alt="icompile.eladkarako.com_ebay_description_fix__2_1" width="525" height="638"/>


<img src="https://icompile.eladkarako.com/_uploads/2016/10/icompile.eladkarako.com_ebay_description_fix__2_2.png" alt="icompile.eladkarako.com_ebay_description_fix__2_2" width="1358" height="682"/>

<pre><span style='color:#808030; '>(</span><span style='color:#800000; font-weight:bold; '>function</span><span style='color:#808030; '>(</span>window<span style='color:#808030; '>,</span> document<span style='color:#808030; '>,</span> ebaydesc_src<span style='color:#808030; '>,</span> pinpoint<span style='color:#808030; '>,</span> pinpoint_parent<span style='color:#808030; '>,</span> new_iframe<span style='color:#808030; '>,</span> footer<span style='color:#808030; '>)</span><span style='color:#800080; '>{</span>
  <span style='color:#800000; '>"</span><span style='color:#0000e6; '>use strict</span><span style='color:#800000; '>"</span><span style='color:#800080; '>;</span>

  <span style='color:#696969; '>/* remove all shit other than official description */</span>
  <span style='color:#800000; font-weight:bold; '>while</span><span style='color:#808030; '>(</span><span style='color:#0f4d75; '>null</span> <span style='color:#808030; '>!==</span> pinpoint<span style='color:#808030; '>.</span>nextElementSibling<span style='color:#808030; '>)</span><span style='color:#800080; '>{</span>
    pinpoint_parent<span style='color:#808030; '>.</span>removeChild<span style='color:#808030; '>(</span> pinpoint<span style='color:#808030; '>.</span>nextElementSibling <span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
  <span style='color:#800080; '>}</span>
  
  <span style='color:#696969; '>/* shit removed */</span>
  
  <span style='color:#696969; '>/* add new description-iframe */</span>

  <span style='color:#696969; '>/*</span>
<span style='color:#696969; '>&#xa0;&#xa0;option #1 - just add it in same (sort of) placement.</span>
<span style='color:#696969; '>&#xa0;&#xa0;pinpoint_parent.appendChild(new_iframe);</span>
<span style='color:#696969; '>&#xa0;&#xa0;*/</span>
  <span style='color:#696969; '>/*</span>
<span style='color:#696969; '>&#xa0;&#xa0;option #2 - a little bit below the layout enables a much larger width.</span>
<span style='color:#696969; '>&#xa0;&#xa0;*/</span>
  footer<span style='color:#808030; '>.</span>insertBefore<span style='color:#808030; '>(</span>new_iframe<span style='color:#808030; '>,</span> footer<span style='color:#808030; '>.</span>firstChild<span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
  new_iframe<span style='color:#808030; '>.</span>style<span style='color:#808030; '>.</span>display <span style='color:#808030; '>=</span> <span style='color:#800000; '>"</span><span style='color:#0000e6; '>none</span><span style='color:#800000; '>"</span><span style='color:#800080; '>;</span>
  new_iframe<span style='color:#808030; '>.</span>onload <span style='color:#808030; '>=</span> <span style='color:#800000; font-weight:bold; '>function</span><span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#800080; '>{</span> 
    <span style='color:#800000; font-weight:bold; '>setTimeout</span><span style='color:#808030; '>(</span><span style='color:#800000; font-weight:bold; '>function</span><span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#800080; '>{</span> 
      new_iframe<span style='color:#808030; '>.</span>style<span style='color:#808030; '>.</span>display <span style='color:#808030; '>=</span> <span style='color:#800000; '>"</span><span style='color:#0000e6; '>block</span><span style='color:#800000; '>"</span><span style='color:#800080; '>;</span>
    <span style='color:#800080; '>}</span><span style='color:#808030; '>,</span> <span style='color:#008c00; '>100</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
  <span style='color:#800080; '>}</span><span style='color:#800080; '>;</span>

  new_iframe<span style='color:#808030; '>.</span>src <span style='color:#808030; '>=</span> ebaydesc_src<span style='color:#800080; '>;</span>

<span style='color:#800080; '>}</span><span style='color:#808030; '>(</span>
  top
<span style='color:#808030; '>,</span> top<span style='color:#808030; '>.</span>document
<span style='color:#808030; '>,</span> top<span style='color:#808030; '>.</span>document<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>'</span><span style='color:#0000e6; '>iframe[src*="ebaydesc"]:not([new_iframe])</span><span style='color:#800000; '>'</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>src
<span style='color:#808030; '>,</span> document<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>'</span><span style='color:#0000e6; '>.itemAttr</span><span style='color:#800000; '>'</span><span style='color:#808030; '>)</span>
<span style='color:#808030; '>,</span> document<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>'</span><span style='color:#0000e6; '>.itemAttr</span><span style='color:#800000; '>'</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>parentElement
<span style='color:#808030; '>,</span> <span style='color:#808030; '>(</span><span style='color:#800000; font-weight:bold; '>function</span><span style='color:#808030; '>(</span>tmp<span style='color:#808030; '>)</span><span style='color:#800080; '>{</span>
    tmp <span style='color:#808030; '>=</span> document<span style='color:#808030; '>.</span>createElement<span style='color:#808030; '>(</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>div</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
    <span style='color:#696969; '>/*</span>
<span style='color:#696969; '>&#xa0;&#xa0;&#xa0;&#xa0;tmp.innerHTML = '&lt;iframe new_iframe allowfullscreen="true" frameborder="0" marginheight="0" marginwidth="0" referrerpolicy="unsafe-url" scrolling="yes" sandbox="allow-forms allow-modals allow-orientation-lock allow-pointer-lock allow-popups allow-popups-to-escape-sandbox allow-same-origin allow-scripts allow-top-navigation" seamless="false" style="width:100%;height:1200px;border:1px solid gray;" src="about:blank">&lt;/iframe>';</span>
<span style='color:#696969; '>&#xa0;&#xa0;&#xa0;&#xa0;*/</span>
    tmp<span style='color:#808030; '>.</span>innerHTML <span style='color:#808030; '>=</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>&lt;iframe new_iframe allowfullscreen="true" frameborder="0" marginheight="0" marginwidth="0" referrerpolicy="no-referrer" scrolling="yes" sandbox="" seamless="false" style="width:100%;height:1200px;border:1px solid gray;" src="about:blank">&lt;/iframe></span><span style='color:#800000; '>'</span><span style='color:#800080; '>;</span>
    <span style='color:#800000; font-weight:bold; '>return</span> tmp<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>iframe</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>cloneNode<span style='color:#808030; '>(</span><span style='color:#0f4d75; '>true</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
  <span style='color:#800080; '>}</span><span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>
<span style='color:#808030; '>,</span> document<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>'</span><span style='color:#0000e6; '>footer</span><span style='color:#800000; '>'</span><span style='color:#808030; '>)</span>
<span style='color:#808030; '>)</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
</pre>

bookmarklet:
<pre>javascript<span style='color:#800080; '>:</span><span style='color:#808030; '>(</span><span style='color:#800000; font-weight:bold; '>function</span><span style='color:#808030; '>(</span>window<span style='color:#808030; '>,</span>document<span style='color:#808030; '>,</span>ebaydesc_src<span style='color:#808030; '>,</span>pinpoint<span style='color:#808030; '>,</span>pinpoint_parent<span style='color:#808030; '>,</span>new_iframe<span style='color:#808030; '>,</span>footer<span style='color:#808030; '>)</span><span style='color:#800080; '>{</span><span style='color:#800000; font-weight:bold; '>while</span><span style='color:#808030; '>(</span><span style='color:#0f4d75; '>null</span><span style='color:#808030; '>!==</span>pinpoint<span style='color:#808030; '>.</span>nextElementSibling<span style='color:#808030; '>)</span>pinpoint_parent<span style='color:#808030; '>.</span>removeChild<span style='color:#808030; '>(</span>pinpoint<span style='color:#808030; '>.</span>nextElementSibling<span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>footer<span style='color:#808030; '>.</span>insertBefore<span style='color:#808030; '>(</span>new_iframe<span style='color:#808030; '>,</span>footer<span style='color:#808030; '>.</span>firstChild<span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>new_iframe<span style='color:#808030; '>.</span>style<span style='color:#808030; '>.</span>display<span style='color:#808030; '>=</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>none</span><span style='color:#800000; '>"</span><span style='color:#800080; '>;</span>new_iframe<span style='color:#808030; '>.</span>onload<span style='color:#808030; '>=</span><span style='color:#800000; font-weight:bold; '>function</span><span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#800080; '>{</span><span style='color:#800000; font-weight:bold; '>setTimeout</span><span style='color:#808030; '>(</span><span style='color:#800000; font-weight:bold; '>function</span><span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#800080; '>{</span>new_iframe<span style='color:#808030; '>.</span>style<span style='color:#808030; '>.</span>display<span style='color:#808030; '>=</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>block</span><span style='color:#800000; '>"</span><span style='color:#800080; '>}</span><span style='color:#808030; '>,</span><span style='color:#008c00; '>100</span><span style='color:#808030; '>)</span><span style='color:#800080; '>}</span><span style='color:#800080; '>;</span>new_iframe<span style='color:#808030; '>.</span>src<span style='color:#808030; '>=</span>ebaydesc_src<span style='color:#800080; '>}</span><span style='color:#808030; '>)</span><span style='color:#808030; '>(</span>top<span style='color:#808030; '>,</span>top<span style='color:#808030; '>.</span>document<span style='color:#808030; '>,</span>top<span style='color:#808030; '>.</span>document<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>'</span><span style='color:#0000e6; '>iframe[src*="ebaydesc"]:not([new_iframe])</span><span style='color:#800000; '>'</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>src<span style='color:#808030; '>,</span>document<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>.itemAttr</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#808030; '>,</span>document<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>.itemAttr</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>parentElement<span style='color:#808030; '>,</span><span style='color:#800000; font-weight:bold; '>function</span><span style='color:#808030; '>(</span>tmp<span style='color:#808030; '>)</span><span style='color:#800080; '>{</span>tmp<span style='color:#808030; '>=</span>document<span style='color:#808030; '>.</span>createElement<span style='color:#808030; '>(</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>div</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>tmp<span style='color:#808030; '>.</span>innerHTML<span style='color:#808030; '>=</span><span style='color:#800000; '>'</span><span style='color:#0000e6; '>&lt;iframe new_iframe allowfullscreen="true" frameborder="0" marginheight="0" marginwidth="0" referrerpolicy="no-referrer" scrolling="yes" sandbox="" seamless="false" style="width:100%;height:1200px;border:1px solid gray;" src="about:blank">&lt;/iframe></span><span style='color:#800000; '>'</span><span style='color:#800080; '>;</span><span style='color:#800000; font-weight:bold; '>return</span> tmp<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>iframe</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>cloneNode<span style='color:#808030; '>(</span><span style='color:#0f4d75; '>true</span><span style='color:#808030; '>)</span><span style='color:#800080; '>}</span><span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#808030; '>,</span>document<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>footer</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
</pre>
</blockquote>

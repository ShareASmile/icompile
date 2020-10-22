<pre><span style='color:#808030; '>(</span><span style='color:#800000; font-weight:bold; '>function</span><span style='color:#808030; '>(</span>w<span style='color:#808030; '>)</span><span style='color:#800080; '>{</span>
<span style='color:#800000; font-weight:bold; '>return</span> <span style='color:#800080; '>{</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>width</span><span style='color:#800000; '>'</span><span style='color:#800080; '>:</span><span style='color:#800080; '>{</span> 
           <span style='color:#800000; '>'</span><span style='color:#0000e6; '>value</span><span style='color:#800000; '>'</span><span style='color:#800080; '>:</span>  <span style='color:#797997; '>Number</span><span style='color:#808030; '>(</span>w<span style='color:#808030; '>.</span>width<span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>toLowerCase</span><span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>replace</span><span style='color:#808030; '>(</span><span style='color:#800000; '>/</span><span style='color:#808030; '>[</span><span style='color:#808030; '>^</span><span style='color:#797997; '>\\d</span><span style='color:#0f69ff; '>\\.</span><span style='color:#808030; '>]</span><span style='color:#800000; '>/</span><span style='color:#800000; font-weight:bold; '>g</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>
         <span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>unit</span><span style='color:#800000; '>'</span><span style='color:#800080; '>:</span>   w<span style='color:#808030; '>.</span>width<span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>replace</span><span style='color:#808030; '>(</span><span style='color:#800000; '>/</span><span style='color:#808030; '>[</span><span style='color:#797997; '>\\d</span><span style='color:#0f69ff; '>\\.</span><span style='color:#808030; '>]</span><span style='color:#800000; '>/</span><span style='color:#800000; font-weight:bold; '>g</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span>
         <span style='color:#800080; '>}</span>
        <span style='color:#808030; '>,</span><span style='color:#800000; '>'</span><span style='color:#0000e6; '>height</span><span style='color:#800000; '>'</span><span style='color:#800080; '>:</span><span style='color:#800080; '>{</span> 
           <span style='color:#800000; '>'</span><span style='color:#0000e6; '>value</span><span style='color:#800000; '>'</span><span style='color:#800080; '>:</span>  <span style='color:#797997; '>Number</span><span style='color:#808030; '>(</span>w<span style='color:#808030; '>.</span>height<span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>toLowerCase</span><span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>replace</span><span style='color:#808030; '>(</span><span style='color:#800000; '>/</span><span style='color:#808030; '>[</span><span style='color:#808030; '>^</span><span style='color:#797997; '>\\d</span><span style='color:#0f69ff; '>\\.</span><span style='color:#808030; '>]</span><span style='color:#800000; '>/</span><span style='color:#800000; font-weight:bold; '>g</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>
         <span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>unit</span><span style='color:#800000; '>'</span><span style='color:#800080; '>:</span>   w<span style='color:#808030; '>.</span>height<span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>replace</span><span style='color:#808030; '>(</span><span style='color:#800000; '>/</span><span style='color:#808030; '>[</span><span style='color:#797997; '>\\d</span><span style='color:#0f69ff; '>\\.</span><span style='color:#808030; '>]</span><span style='color:#800000; '>/</span><span style='color:#800000; font-weight:bold; '>g</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span>
         <span style='color:#800080; '>}</span>
        <span style='color:#800080; '>}</span>
<span style='color:#800080; '>}</span><span style='color:#808030; '>(</span>
window<span style='color:#808030; '>.</span>getComputedStyle<span style='color:#808030; '>(</span>document<span style='color:#808030; '>.</span>querySelector<span style='color:#808030; '>(</span><span style='color:#800000; '>'</span><span style='color:#0000e6; '>html</span><span style='color:#800000; '>'</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>
<span style='color:#808030; '>)</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
</pre>

get something like this:

<pre><span style='color:#800080; '>{</span>
  width<span style='color:#800080; '>:</span> <span style='color:#800080; '>{</span>
    value<span style='color:#800080; '>:</span> <span style='color:#008000; '>1092.8</span>
    <span style='color:#808030; '>,</span> unit<span style='color:#800080; '>:</span> <span style='color:#800000; '>"</span><span style='color:#0000e6; '>px</span><span style='color:#800000; '>"</span>
  <span style='color:#800080; '>}</span>
  <span style='color:#808030; '>,</span> height<span style='color:#800080; '>:</span> <span style='color:#800080; '>{</span>
    value<span style='color:#800080; '>:</span> <span style='color:#008000; '>215.2</span>
    <span style='color:#808030; '>,</span> unit<span style='color:#800080; '>:</span> <span style='color:#800000; '>"</span><span style='color:#0000e6; '>px</span><span style='color:#800000; '>"</span>
  <span style='color:#800080; '>}</span>
<span style='color:#800080; '>}</span>
</pre>
<img src="https://icompile.eladkarako.com/_uploads/2015/03/icompile.eladkarako.com_keep_calm_and_sanitize.png" alt="keep calm and sanitize" rem-width="208" rem-height="243" class="alignright size-full wp-image-2724" />Sometimes it is better to use a clear and simple solution that has better readability over a 'template thinking'. over-thinking is a good thing, it keeps your mind sharp.

considering the fact that using <code>FILTER_SANITIZE_SPECIAL_CHARS</code> with <code>FILTER_FLAG_STRIP_HIGH</code> will probably send you co-friend/team-mate programmer to dig through http://php.net, which is not nice..

...sometimes RegEx is just the better choice, especially when you are working on a custom solution,

<strong>Here is a clean <code>filter_input</code> to SANITIZE YouTube Video-ID-like value,</strong>

<pre>
<span style='color:#5f5035'>&lt;?php</span><span style='color:#000000'></span>
<span style='color:#797997'>$video_id</span><span style='color:#000000'> </span><span style='color:#808030'>=</span><span style='color:#000000'> filter_input</span><span style='color:#808030'>(</span><span style='color:#000000'>INPUT_GET</span><span style='color:#808030'>,</span><span style='color:#000000'> </span><span style='color:#0000e6'>'video_id'</span><span style='color:#808030'>,</span><span style='color:#000000'> FILTER_CALLBACK</span><span style='color:#808030'>,</span><span style='color:#000000'> </span><span style='color:#808030'>[</span><span style='color:#0000e6'>'options'</span><span style='color:#000000'> </span><span style='color:#808030'>=</span><span style='color:#808030'>></span><span style='color:#000000'> </span><span style='color:#800000font-weight:bold; '>function</span><span style='color:#000000'> </span><span style='color:#808030'>(</span><span style='color:#797997'>$value</span><span style='color:#808030'>)</span><span style='color:#000000'> </span><span style='color:#800080'>{</span><span style='color:#000000'></span>
<span style='color:#000000'>&#xa0;&#xa0;</span><span style='color:#800000font-weight:bold; '>return</span><span style='color:#000000'> </span><span style='color:#400000'>preg_replace</span><span style='color:#808030'>(</span><span style='color:#0000e6'>"</span><span style='color:#800000'>#</span><span style='color:#808030'>[</span><span style='color:#808030'>^</span><span style='color:#0000e6'>_0</span><span style='color:#808030'>-</span><span style='color:#0000e6'>9a</span><span style='color:#808030'>-</span><span style='color:#0000e6'>z</span><span style='color:#0f69ff'>\\-</span><span style='color:#808030'>]</span><span style='color:#800000'>#</span><span style='color:#800000font-weight:bold; '>im</span><span style='color:#0000e6'>"</span><span style='color:#808030'>,</span><span style='color:#000000'> </span><span style='color:#0000e6'>""</span><span style='color:#808030'>,</span><span style='color:#000000'> </span><span style='color:#797997'>$value</span><span style='color:#808030'>)</span><span style='color:#800080'>;</span><span style='color:#000000'></span>
<span style='color:#800080'>}</span><span style='color:#808030'>]</span><span style='color:#808030'>)</span><span style='color:#800080'>;</span><span style='color:#000000'></span>
<span style='color:#5f5035'>?></span>
</pre>
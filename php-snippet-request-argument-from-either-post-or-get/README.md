In-case you would like to enable a request details from either POST or GET (and you do not really care from where it got from)- this is the proper way to do this.

*consider filtering the input, which should be handled depending on the content you expect to receive.

<pre><span style='color:#5f5035;'>&lt;?php</span><span style='color:#000000;'></span>
<span style='color:#800000;font-weight:bold; '>function</span><span style='color:#000000;'> arg_value</span><span style='color:#808030;'>(</span><span style='color:#797997;'>$name</span><span style='color:#808030;'>)</span><span style='color:#800080;'>{</span><span style='color:#000000;'> </span><span style='color:#696969;'>/*returns a valid value or empty string. valid argument from either POST or GET */</span><span style='color:#000000;'></span>
<span style='color:#000000;'>&#xa0;&#xa0;</span><span style='color:#797997;'>$items</span><span style='color:#000000;'> </span><span style='color:#808030;'>=</span><span style='color:#000000;'> </span><span style='color:#808030;'>[</span><span style='color:#000000;'></span>
<span style='color:#000000;'>&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;filter_input</span><span style='color:#808030;'>(</span><span style='color:#000000;'>INPUT_POST</span><span style='color:#808030;'>,</span><span style='color:#000000;'> </span><span style='color:#797997;'>$name</span><span style='color:#808030;'>,</span><span style='color:#000000;'> FILTER_UNSAFE_RAW</span><span style='color:#808030;'>)</span><span style='color:#000000;'></span>
<span style='color:#000000;'>&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;</span><span style='color:#808030;'>,</span><span style='color:#000000;'>filter_input</span><span style='color:#808030;'>(</span><span style='color:#000000;'>INPUT_GET</span><span style='color:#808030;'>,</span><span style='color:#000000;'>  </span><span style='color:#797997;'>$name</span><span style='color:#808030;'>,</span><span style='color:#000000;'> FILTER_UNSAFE_RAW</span><span style='color:#808030;'>)</span><span style='color:#000000;'></span>
<span style='color:#000000;'>&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;</span><span style='color:#808030;'>]</span><span style='color:#800080;'>;</span><span style='color:#000000;'></span>
<span style='color:#000000;'></span>
<span style='color:#000000;'>&#xa0;&#xa0;</span><span style='color:#797997;'>$items</span><span style='color:#000000;'> </span><span style='color:#808030;'>=</span><span style='color:#000000;'> </span><span style='color:#400000;'>array_filter</span><span style='color:#808030;'>(</span><span style='color:#797997;'>$items</span><span style='color:#808030;'>,</span><span style='color:#000000;'> </span><span style='color:#800000;font-weight:bold; '>function</span><span style='color:#808030;'>(</span><span style='color:#797997;'>$item</span><span style='color:#808030;'>)</span><span style='color:#800080;'>{</span><span style='color:#000000;'></span>
<span style='color:#000000;'>&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;</span><span style='color:#797997;'>$item</span><span style='color:#000000;'> </span><span style='color:#808030;'>=</span><span style='color:#000000;'> </span><span style='color:#808030;'>(</span><span style='color:#800000;font-weight:bold; '>null</span><span style='color:#000000;'> </span><span style='color:#808030;'>!</span><span style='color:#808030;'>=</span><span style='color:#808030;'>=</span><span style='color:#000000;'> </span><span style='color:#797997;'>$item</span><span style='color:#808030;'>)</span><span style='color:#000000;'> </span><span style='color:#808030;'>&amp;</span><span style='color:#808030;'>&amp;</span><span style='color:#000000;'> </span><span style='color:#808030;'>(</span><span style='color:#0f4d75;'>false</span><span style='color:#000000;'> </span><span style='color:#808030;'>!</span><span style='color:#808030;'>=</span><span style='color:#808030;'>=</span><span style='color:#000000;'> </span><span style='color:#797997;'>$item</span><span style='color:#808030;'>)</span><span style='color:#800080;'>;</span><span style='color:#000000;'></span>
<span style='color:#000000;'>&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;</span><span style='color:#800000;font-weight:bold; '>return</span><span style='color:#000000;'> </span><span style='color:#797997;'>$item</span><span style='color:#800080;'>;</span><span style='color:#000000;'></span>
<span style='color:#000000;'>&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;</span><span style='color:#800080;'>}</span><span style='color:#808030;'>)</span><span style='color:#800080;'>;</span><span style='color:#000000;'></span>
<span style='color:#000000;'>&#xa0;&#xa0;</span><span style='color:#400000;'>array_push</span><span style='color:#808030;'>(</span><span style='color:#797997;'>$items</span><span style='color:#808030;'>,</span><span style='color:#000000;'> </span><span style='color:#800000;font-weight:bold; '>null</span><span style='color:#808030;'>)</span><span style='color:#800080;'>;</span><span style='color:#000000;'> </span><span style='color:#696969;'>/* null value */</span><span style='color:#000000;'></span>
<span style='color:#000000;'>&#xa0;&#xa0;</span><span style='color:#797997;'>$items</span><span style='color:#000000;'> </span><span style='color:#808030;'>=</span><span style='color:#000000;'> </span><span style='color:#400000;'>array_shift</span><span style='color:#808030;'>(</span><span style='color:#797997;'>$items</span><span style='color:#808030;'>)</span><span style='color:#800080;'>;</span><span style='color:#000000;'></span>
<span style='color:#000000;'>&#xa0;&#xa0;</span><span style='color:#800000;font-weight:bold; '>return</span><span style='color:#000000;'> </span><span style='color:#797997;'>$items</span><span style='color:#800080;'>;</span><span style='color:#000000;'></span>
<span style='color:#800080;'>}</span><span style='color:#000000;'></span>
<span style='color:#5f5035;'>?&gt;</span>
</pre>
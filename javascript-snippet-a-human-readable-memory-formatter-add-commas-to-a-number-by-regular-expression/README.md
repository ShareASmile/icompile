<img src="https://icompile.eladkarako.com/_uploads/2017/03/icompile.eladkarako.com_human_readable_javascript_file_size.jpg" alt="" width="143" height="80"/>

<pre><span style='color:#800000; font-weight:bold; '>function</span> human_readable_bytes_size<span style='color:#808030; '>(</span>bytes<span style='color:#808030; '>,</span> decimals<span style='color:#808030; '>,</span> sap<span style='color:#808030; '>)</span> <span style='color:#800080; '>{</span>
  decimals <span style='color:#808030; '>=</span> <span style='color:#800000; '>"</span><span style='color:#0000e6; '>number</span><span style='color:#800000; '>"</span> <span style='color:#808030; '>===</span> <span style='color:#800000; font-weight:bold; '>typeof</span> decimals <span style='color:#800080; '>?</span> decimals <span style='color:#800080; '>:</span> <span style='color:#008c00; '>2</span><span style='color:#800080; '>;</span>
  sap <span style='color:#808030; '>=</span> <span style='color:#800000; '>"</span><span style='color:#0000e6; '>string</span><span style='color:#800000; '>"</span> <span style='color:#808030; '>===</span> <span style='color:#800000; font-weight:bold; '>typeof</span> sap <span style='color:#800080; '>?</span> sap <span style='color:#800080; '>:</span> <span style='color:#800000; '>"</span><span style='color:#800000; '>"</span><span style='color:#800080; '>;</span>

  <span style='color:#800000; font-weight:bold; '>var</span> 
    size <span style='color:#808030; '>=</span> <span style='color:#808030; '>[</span><span style='color:#800000; '>'</span><span style='color:#0000e6; '>B</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>kB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>MB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>GB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>TB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>PB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>EB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>ZB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>YB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>]</span>
  <span style='color:#808030; '>,</span> factor <span style='color:#808030; '>=</span> <span style='color:#797997; '>Math</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>floor</span><span style='color:#808030; '>(</span>  <span style='color:#808030; '>(</span><span style='color:#797997; '>String</span><span style='color:#808030; '>(</span>bytes<span style='color:#808030; '>)</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>length</span> <span style='color:#808030; '>-</span> <span style='color:#008c00; '>1</span><span style='color:#808030; '>)</span> <span style='color:#808030; '>/</span> <span style='color:#008c00; '>3</span>  <span style='color:#808030; '>)</span>
  <span style='color:#800080; '>;</span>
  
  bytes <span style='color:#808030; '>=</span> bytes <span style='color:#808030; '>/</span> <span style='color:#797997; '>Math</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>pow</span><span style='color:#808030; '>(</span><span style='color:#008c00; '>1024</span><span style='color:#808030; '>,</span> factor<span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>  <span style='color:#696969; '>//calc</span>
  bytes <span style='color:#808030; '>=</span> <span style='color:#797997; '>Math</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>floor</span><span style='color:#808030; '>(</span>bytes <span style='color:#808030; '>*</span> <span style='color:#797997; '>Math</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>pow</span><span style='color:#808030; '>(</span><span style='color:#008c00; '>10</span><span style='color:#808030; '>,</span> decimals<span style='color:#808030; '>)</span><span style='color:#808030; '>)</span> <span style='color:#808030; '>/</span> <span style='color:#797997; '>Math</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>pow</span><span style='color:#808030; '>(</span><span style='color:#008c00; '>10</span><span style='color:#808030; '>,</span> decimals<span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>  <span style='color:#696969; '>//round digits</span>
  
   
  <span style='color:#800000; font-weight:bold; '>return</span> <span style='color:#797997; '>String</span><span style='color:#808030; '>(</span>bytes<span style='color:#808030; '>)</span> <span style='color:#808030; '>+</span> sap <span style='color:#808030; '>+</span> size<span style='color:#808030; '>[</span>factor<span style='color:#808030; '>]</span><span style='color:#800080; '>;</span>
<span style='color:#800080; '>}</span>



human_readable_bytes_size<span style='color:#808030; '>(</span><span style='color:#008c00; '>29</span><span style='color:#808030; '>)</span>
<span style='color:#696969; '>//"29B"</span>
human_readable_bytes_size<span style='color:#808030; '>(</span><span style='color:#008c00; '>29000000000000000</span><span style='color:#808030; '>)</span>
<span style='color:#696969; '>//"25.75PB"</span>
human_readable_bytes_size<span style='color:#808030; '>(</span><span style='color:#008c00; '>2900000000000</span><span style='color:#808030; '>)</span>
<span style='color:#696969; '>//"2.63TB"</span>
human_readable_bytes_size<span style='color:#808030; '>(</span><span style='color:#008c00; '>290000000000</span><span style='color:#808030; '>)</span>
<span style='color:#696969; '>//"270.08GB"</span>
human_readable_bytes_size<span style='color:#808030; '>(</span><span style='color:#008c00; '>290000000000</span><span style='color:#808030; '>,</span><span style='color:#008c00; '>5</span><span style='color:#808030; '>)</span>
<span style='color:#696969; '>//"270.08354GB"</span>
human_readable_bytes_size<span style='color:#808030; '>(</span><span style='color:#008c00; '>290000000000</span><span style='color:#808030; '>,</span><span style='color:#008c00; '>5</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>---</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span>
<span style='color:#696969; '>//"270.08354---GB"</span>
</pre>

also available on GitHub: <a href="https://github.com/eladkarako/javascript_human_readable_bytes_size" target="_blank">https://github.com/eladkarako/javascript_human_readable_bytes_size</a>

Would you like the PHP version? - <a href="https://icompile.eladkarako.com/php-snippet-a-human-readable-memory-formatter-add-commas-to-a-number-by-regular-expression/" target="_blank">https://icompile.eladkarako.com/php-snippet-a-human-readable-memory-formatter-add-commas-to-a-number-by-regular-expression/</a>

<hr/>

This is a variation with comma-separation (only for the integer part since the fraction part looks weird w/ commas..)

<pre>
<span style='color:#800000; font-weight:bold; '>function</span> human_readable_bytes_size<span style='color:#808030; '>(</span>bytes<span style='color:#808030; '>,</span> digits<span style='color:#808030; '>,</span> sap<span style='color:#808030; '>,</span> is_comma_sap<span style='color:#808030; '>)</span> <span style='color:#800080; '>{</span>  <span style='color:#800000; '>"</span><span style='color:#0000e6; '>use strict</span><span style='color:#800000; '>"</span><span style='color:#800080; '>;</span>
  digits       <span style='color:#808030; '>=</span> <span style='color:#800000; '>"</span><span style='color:#0000e6; '>number</span><span style='color:#800000; '>"</span>  <span style='color:#808030; '>===</span> <span style='color:#800000; font-weight:bold; '>typeof</span> digits        <span style='color:#800080; '>?</span> digits         <span style='color:#800080; '>:</span>  <span style='color:#008c00; '>2</span><span style='color:#800080; '>;</span>
  sap          <span style='color:#808030; '>=</span> <span style='color:#800000; '>"</span><span style='color:#0000e6; '>string</span><span style='color:#800000; '>"</span>  <span style='color:#808030; '>===</span> <span style='color:#800000; font-weight:bold; '>typeof</span> sap           <span style='color:#800080; '>?</span> sap            <span style='color:#800080; '>:</span> <span style='color:#800000; '>"</span><span style='color:#800000; '>"</span><span style='color:#800080; '>;</span>
  is_comma_sap <span style='color:#808030; '>=</span> <span style='color:#800000; '>"</span><span style='color:#0000e6; '>boolean</span><span style='color:#800000; '>"</span> <span style='color:#808030; '>===</span> <span style='color:#800000; font-weight:bold; '>typeof</span> is_comma_sap  <span style='color:#800080; '>?</span> is_comma_sap   <span style='color:#800080; '>:</span> <span style='color:#0f4d75; '>false</span><span style='color:#800080; '>;</span>

  <span style='color:#800000; font-weight:bold; '>var</span>  size <span style='color:#808030; '>=</span> <span style='color:#808030; '>[</span><span style='color:#800000; '>'</span><span style='color:#0000e6; '>B</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>kB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>MB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>GB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>TB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>PB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>EB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>ZB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>'</span><span style='color:#0000e6; '>YB</span><span style='color:#800000; '>'</span><span style='color:#808030; '>]</span>
     <span style='color:#808030; '>,</span> factor <span style='color:#808030; '>=</span> <span style='color:#797997; '>Math</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>floor</span><span style='color:#808030; '>(</span>  <span style='color:#808030; '>(</span><span style='color:#797997; '>String</span><span style='color:#808030; '>(</span>bytes<span style='color:#808030; '>)</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>length</span> <span style='color:#808030; '>-</span> <span style='color:#008c00; '>1</span><span style='color:#808030; '>)</span> <span style='color:#808030; '>/</span> <span style='color:#008c00; '>3</span>  <span style='color:#808030; '>)</span>
     <span style='color:#800080; '>;</span>

  bytes <span style='color:#808030; '>=</span> bytes <span style='color:#808030; '>/</span> <span style='color:#797997; '>Math</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>pow</span><span style='color:#808030; '>(</span><span style='color:#008c00; '>1024</span><span style='color:#808030; '>,</span> factor<span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>  <span style='color:#696969; '>//calc</span>
  bytes <span style='color:#808030; '>=</span> <span style='color:#797997; '>Math</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>floor</span><span style='color:#808030; '>(</span>bytes <span style='color:#808030; '>*</span> <span style='color:#797997; '>Math</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>pow</span><span style='color:#808030; '>(</span><span style='color:#008c00; '>10</span><span style='color:#808030; '>,</span> digits<span style='color:#808030; '>)</span><span style='color:#808030; '>)</span> <span style='color:#808030; '>/</span> <span style='color:#797997; '>Math</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>pow</span><span style='color:#808030; '>(</span><span style='color:#008c00; '>10</span><span style='color:#808030; '>,</span> digits<span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>  <span style='color:#696969; '>//round digits</span>
  
  <span style='color:#800000; font-weight:bold; '>if</span><span style='color:#808030; '>(</span><span style='color:#0f4d75; '>true</span> <span style='color:#808030; '>===</span> is_comma_sap<span style='color:#808030; '>)</span><span style='color:#800080; '>{</span>
    bytes <span style='color:#808030; '>=</span> <span style='color:#797997; '>String</span><span style='color:#808030; '>(</span>bytes<span style='color:#808030; '>)</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>split</span><span style='color:#808030; '>(</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>.</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
    bytes<span style='color:#808030; '>[</span><span style='color:#008c00; '>0</span><span style='color:#808030; '>]</span> <span style='color:#808030; '>=</span> bytes<span style='color:#808030; '>[</span><span style='color:#008c00; '>0</span><span style='color:#808030; '>]</span><span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>replace</span><span style='color:#808030; '>(</span><span style='color:#800000; '>/</span><span style='color:#808030; '>(</span><span style='color:#797997; '>\\d</span><span style='color:#808030; '>)</span><span style='color:#808030; '>(</span><span style='color:#800000; font-weight:bold; '>?=</span><span style='color:#808030; '>(</span><span style='color:#797997; '>\\d</span><span style='color:#808030; '>{</span><span style='color:#008c00; '>3</span><span style='color:#808030; '>}</span><span style='color:#808030; '>)</span><span style='color:#808030; '>+</span><span style='color:#808030; '>$</span><span style='color:#808030; '>)</span><span style='color:#800000; '>/</span><span style='color:#800000; font-weight:bold; '>g</span><span style='color:#808030; '>,</span> <span style='color:#800000; '>"</span><span style='color:#0000e6; '>$1,</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
    bytes <span style='color:#808030; '>=</span> bytes<span style='color:#808030; '>.</span><span style='color:#800000; font-weight:bold; '>join</span><span style='color:#808030; '>(</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>.</span><span style='color:#800000; '>"</span><span style='color:#808030; '>)</span><span style='color:#800080; '>;</span>
  <span style='color:#800080; '>}</span>

  <span style='color:#800000; font-weight:bold; '>return</span> <span style='color:#797997; '>String</span><span style='color:#808030; '>(</span>bytes<span style='color:#808030; '>)</span> <span style='color:#808030; '>+</span> sap <span style='color:#808030; '>+</span> size<span style='color:#808030; '>[</span>factor<span style='color:#808030; '>]</span><span style='color:#800080; '>;</span>
<span style='color:#800080; '>}</span>
</pre>

<hr/>

since it is very rare (actually improbable) to use the comma-feature when measuring to the largest scale available,
- In my project <a href="https://github.com/eladkarako/any2base64" target="_blank">https://github.com/eladkarako/any2base64</a> I'm using a slightly different variation that actually 'reduce a scale by one' meaning, instead of using 1GB it will use 1024MB <sub>(or 1000-MiB.. 
<sub>* <a href="https://en.wikipedia.org/wiki/Mebibyte" target="_blank">[1]</a> <a href="http://physics.nist.gov/cuu/Units/binary.html" target="_blank">[2]</a></sub>)</sub>
It works nicely, and sometimes helps to comprehend byte sizes more clearly... Ahhh.. human perspective! ;] ;]

', 'JavaScript Snippet - A Human-Readable Memory-Formatter
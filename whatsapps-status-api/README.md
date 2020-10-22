<blockquote>Over HTTPS, and with no requiring of log-in, auth or any token, you are free to ping it if you'll ever require a fast response (<a href="https://www.lighttpd.net/" target="_blank">lighttpd</a><a href="https://en.wikipedia.org/wiki/Lighttpd" target="_blank"><sup>[wiki]</sup></a>) from a valid HTTPS (SSL) server, that will have almost 100% up-time. Which is kind'a useful :)</blockquote>

<ul>
<li>
For
  <ul>
  <li><a href="https://www.whatsapp.com/status.php?" target="_blank">https://www.whatsapp.com/status.php?</a></li>
  <li><a href="https://www.whatsapp.com/status.php?v=0" target="_blank">https://www.whatsapp.com/status.php?v=0</a></li>
  <li><a href="https://www.whatsapp.com/status.php?v=1" target="_blank">https://www.whatsapp.com/status.php?v=1</a></li>
  <li>or for any <code>?v=</code> parameter with a value of <code><em>3</em></code> (or larger than <code>3</code>..)</li>
  </ul>
You will get <code>text/xml</code>:
<pre><span style='color:#004a43; '>&lt;?</span><span style='color:#800000; font-weight:bold; '>xml</span><span style='color:#004a43; '> </span><span style='color:#074726; '>version</span><span style='color:#808030; '>=</span><span style='color:#800000; '>"</span><span style='color:#7d0045; '>1.0</span><span style='color:#800000; '>"</span><span style='color:#004a43; '> </span><span style='color:#074726; '>encoding</span><span style='color:#808030; '>=</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>UTF-8</span><span style='color:#800000; '>"</span><span style='color:#004a43; '>?&gt;</span>
<span style='color:#a65700; '>&lt;</span><span style='color:#5f5035; '>status</span><span style='color:#a65700; '>&gt;</span>
<span style='color:#a65700; '>&lt;</span><span style='color:#5f5035; '>function</span> <span style='color:#274796; '>name</span><span style='color:#808030; '>=</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>registration</span><span style='color:#800000; '>"</span> <span style='color:#274796; '>available</span><span style='color:#808030; '>=</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>true</span><span style='color:#800000; '>"</span> <span style='color:#274796; '>since</span><span style='color:#808030; '>=</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>1311836400</span><span style='color:#800000; '>"</span> <span style='color:#a65700; '>/&gt;</span>
<span style='color:#a65700; '>&lt;</span><span style='color:#5f5035; '>function</span> <span style='color:#274796; '>name</span><span style='color:#808030; '>=</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>chat</span><span style='color:#800000; '>"</span> <span style='color:#274796; '>available</span><span style='color:#808030; '>=</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>true</span><span style='color:#800000; '>"</span> <span style='color:#274796; '>since</span><span style='color:#808030; '>=</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>1314015300</span><span style='color:#800000; '>"</span> <span style='color:#a65700; '>/&gt;</span>
<span style='color:#a65700; '>&lt;/</span><span style='color:#5f5035; '>status</span><span style='color:#a65700; '>&gt;</span>
</pre>
</li>
<li>
For <a href="https://www.whatsapp.com/status.php?v=2" target="_blank">https://www.whatsapp.com/status.php?v=2</a> 

You will get <code>application/json</code>:
<pre><span style='color:#800080; '>{</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>email</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#800080; '>{</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>available</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#0f4d75; '>true</span><span style='color:#800080; '>}</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>last</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#800080; '>{</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>available</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#0f4d75; '>true</span><span style='color:#800080; '>}</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>sync</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#800080; '>{</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>available</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#0f4d75; '>true</span><span style='color:#800080; '>}</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>chat</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#800080; '>{</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>available</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#0f4d75; '>true</span><span style='color:#800080; '>}</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>group</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#800080; '>{</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>available</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#0f4d75; '>true</span><span style='color:#800080; '>}</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>multimedia</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#800080; '>{</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>available</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#0f4d75; '>true</span><span style='color:#800080; '>}</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>online</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#800080; '>{</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>available</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#0f4d75; '>true</span><span style='color:#800080; '>}</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>profile</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#800080; '>{</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>available</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#0f4d75; '>true</span><span style='color:#800080; '>}</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>push</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#800080; '>{</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>available</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#0f4d75; '>true</span><span style='color:#800080; '>}</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>registration</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#800080; '>{</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>available</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#0f4d75; '>true</span><span style='color:#800080; '>}</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>status</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#800080; '>{</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>available</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#0f4d75; '>true</span><span style='color:#800080; '>}</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>broadcast</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#800080; '>{</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>available</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#0f4d75; '>true</span><span style='color:#800080; '>}</span><span style='color:#808030; '>,</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>version</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#800080; '>{</span><span style='color:#800000; '>"</span><span style='color:#0000e6; '>available</span><span style='color:#800000; '>"</span><span style='color:#800080; '>:</span><span style='color:#0f4d75; '>true</span><span style='color:#800080; '>}</span><span style='color:#800080; '>}</span>
</pre>
</li>
</ul>
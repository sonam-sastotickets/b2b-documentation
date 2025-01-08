<article class="md-content__inner md-typeset">
                
                  



  <h1>Download eTicket</h1>

<h2 id="download-eticket">Download eTicket</h2>
<div class="highlight"><pre><span></span><code tabindex="0">Endpoint: ~/download-ticket
Method: Post
Header Params: Content-Type  : application/json
Authorization : Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC9nZHMtYWRtaW4udGVzdFwvYXBpXC9pbnRsXC9hbmRyb2lkXC9pbml0aWFsaXplIiwiaWF0IjoxNjEzMzg1ODY3LCJleHAiOjE2MTMzODk0NjcsIm5iZiI6MTYxMzM4NTg2NywianRpIjoiY3o2eFZLdEVkd05jTTRVcCIsInN1YiI6MTMsInBydiI6IjQyZWRlMzMzNGEwNGNkNjVjYjJiZTNmNWFkZmViMmMxZWRkMzA3NzQifQ.UzEWszpOW92jOqSkdciWoGV4456CdS1nuPx7Tql-_Xk
</code></pre></div>
<p><code>Request Body</code></p>
<div class="highlight"><pre><span></span><code><span class="p">{</span>
<span class="w">  </span><span class="nt">"ticketReferenceID"</span><span class="p">:</span><span class="w"> </span><span class="s2">"29f27b24-3f33-4190-9835-9859c790fc47"</span>
<span class="p">}</span>
</code></pre></div>
<p><code>Sample Response</code></p>
<div class="highlight"><pre><span></span><code tabindex="0"><span class="p">{</span>
<span class="w">  </span><span class="nt">"success"</span><span class="p">:</span><span class="w"> </span><span class="kc">true</span><span class="p">,</span>
<span class="w">  </span><span class="nt">"data"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">    </span><span class="nt">"eticketLink"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights-private.s3.ap-southeast-1.amazonaws.com/tickets/PQMJ8E-1676354461.pdf?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&amp;X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIA4CEOEY6AUXGMCTXF%2F20230214%2Fap-southeast-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20230214T060104Z&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Expires=900&amp;X-Amz-Signature=a834632054848ad610561f9a7588a1ff789ae2a35c7991f091d97a043ed7d043"</span>
<span class="w">  </span><span class="p">}</span>
<span class="p">}</span>
</code></pre></div>
<p><br></p>
<p><code>Sample Error Response</code></p>
<div class="highlight"><pre><span></span><code><span class="err">Case</span><span class="p">:</span><span class="w"> </span><span class="err">Valida</span><span class="kc">t</span><span class="err">io</span><span class="kc">n</span><span class="w"> </span><span class="err">Error</span>
<span class="p">{</span>
<span class="w">    </span><span class="nt">"success"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"data"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">        </span><span class="nt">"error"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Invalid Ticket Parameters."</span>
<span class="w">    </span><span class="p">}</span>
<span class="p">}</span>


<span class="err">Case</span><span class="p">:</span><span class="w"> </span><span class="err">Ticke</span><span class="kc">t</span><span class="w"> </span><span class="kc">transa</span><span class="err">c</span><span class="kc">t</span><span class="err">io</span><span class="kc">n</span><span class="w"> </span><span class="kc">n</span><span class="err">o</span><span class="kc">t</span><span class="w"> </span><span class="kc">f</span><span class="err">ou</span><span class="kc">n</span><span class="err">d</span>
<span class="p">{</span>
<span class="w">    </span><span class="nt">"success"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"data"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">        </span><span class="nt">"error"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Ticket Records Not Found."</span>
<span class="w">    </span><span class="p">}</span>
<span class="p">}</span>


<span class="err">Case</span><span class="p">:</span><span class="w"> </span><span class="err">Ticke</span><span class="kc">t</span><span class="w"> </span><span class="err">PDF</span><span class="w"> </span><span class="err">ge</span><span class="kc">nerat</span><span class="err">io</span><span class="kc">n</span><span class="w"> </span><span class="err">Failed</span>
<span class="p">{</span>
<span class="w">    </span><span class="nt">"success"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"data"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">        </span><span class="nt">"error"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Invalid Ticket Parameters. Ticket could not be generated."</span>
<span class="w">    </span><span class="p">}</span>
<span class="p">}</span>
</code></pre></div>





                
              </article>
---
layout: default
title: RFCs
section_id: rfc
---

<div class="full parallax" style="background-image: url(images/banner/banner.jpg); color: #000000;">
  <div class="row">
    <div class="large-12 columns">
      {% include section-header.html title="RFC" tagline="" color="#000000" class="big" %}
    </div>
  </div>
  <div class="four spacing"></div>
</div>

<div class="row" style="margin-top: 20px;">
  Over the years, members of the IRL have contributed to a number of IETF Request for Comments (RFCs).
  We list all known RFC contributions here.

  <hr />
</div>
<div class="row">

{% assign current_year = site.time | date: "%Y" %}
{% assign months = "January,February,March,April,May,June,July,August,September,October,November,December" | split: "," %}
{% for year in (2006..current_year) reversed %}
  {% assign is_publication_for_year = false %}
  {% for pub in site.data.publications %}
    {% if pub.type == "rfc" %}
      {% if pub.year == year %}
        {% assign is_publication_for_year = true %}
      {% endif %}
    {% endif %}
  {% endfor %}

  {% if is_publication_for_year %}
    <h3>{{ year }}</h3>
    <ul>
    {% for month in months reversed %}
      {% for pub in site.data.publications %}
        {% assign pub_month_downcase = pub.month | downcase %}
        {% assign month_downcase = month | downcase %}
        {% if pub.year == year and pub_month_downcase == month_downcase %}
          {% if pub.type == "rfc" %}
            <li>
              {{ pub.authors }}<br />
              <strong>"{{ pub.title }}"</strong><br />
              <em>RFC {{ pub.number }}</em>, {{ month }} {{ year }}.<br />
              {% if pub.note %}
                <em>{{ pub.note }}</em><br />
              {% endif %}
              <a href="https://www.rfc-editor.org/rfc/rfc{{ pub.number }}.html" target="_blank"><img src="images/extensions/html.png" alt="HTML" /></a>
            </li>
          {% endif %}
        {% endif %}
      {% endfor %}
    {% endfor %}
    </ul>
  {% endif %}
{% endfor %}

<h3>2001</h3>
<ul>


<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=45" title="R. Braden and L. Zhang, &lt;strong&gt;&amp;quot;RSVP Cryptographic Authentication&lt;/strong&gt;,&amp;quot; &lt;em&gt;RFC 3097&lt;/em&gt;, April  2001. "><img src="/images/extensions/bib.png" /></a>

     R. Braden and L. Zhang, <br/><strong>&quot;RSVP Cryptographic Authentication</strong>,&quot; <br/><em>RFC 3097</em>, April  2001.

        <a target="_blank" href="ftp://ftp.isi.edu/in-notes/rfc3097.txt"><img src="/images/extensions/txt.png"></a>

    </li>

</ul><h3>2000</h3>
<ul>


<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=46" title="Y. Bernet, P. Ford, R. Yavatkar, F. Baker, L. Zhang, M. Speer, R. Braden, B. Davie, J. Wroclawski, and E. Felstaine, &lt;strong&gt;&amp;quot;A Framework for Integrated Services Operation over Diffserv Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;RFC 2998&lt;/em&gt;, November  2000. "><img src="/images/extensions/bib.png" /></a>

     Y. Bernet, P. Ford, R. Yavatkar, F. Baker, L. Zhang, M. Speer, R. Braden, B. Davie, J. Wroclawski, and E. Felstaine, <br/><strong>&quot;A Framework for Integrated Services Operation over Diffserv Networks</strong>,&quot; <br/><em>RFC 2998</em>, November  2000.

        <a target="_blank" href="ftp://ftp.isi.edu/in-notes/rfc2998.txt"><img src="/images/extensions/txt.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=47" title="R. Stewart, Q. Xie, K. Morneault, C. Sharp, H. Schwarzbauer, T. Taylor, I. Rytina, M. Kalla, L. Zhang, and V. Paxson, &lt;strong&gt;&amp;quot;Stream Control Transmission Protocol&lt;/strong&gt;,&amp;quot; &lt;em&gt;RFC 2960&lt;/em&gt;, October  2000. "><img src="/images/extensions/bib.png" /></a>

     R. Stewart, Q. Xie, K. Morneault, C. Sharp, H. Schwarzbauer, T. Taylor, I. Rytina, M. Kalla, L. Zhang, and V. Paxson, <br/><strong>&quot;Stream Control Transmission Protocol</strong>,&quot; <br/><em>RFC 2960</em>, October  2000.

        <a target="_blank" href="ftp://ftp.isi.edu/in-notes/rfc2960.txt"><img src="/images/extensions/txt.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=48" title="A. Terzis, J. Krawczyk, J. Wroclawski, and L. Zhang, &lt;strong&gt;&amp;quot;RSVP Operation over IP Tunnels&lt;/strong&gt;,&amp;quot; &lt;em&gt;RFC 2746&lt;/em&gt;, January  2000. "><img src="/images/extensions/bib.png" /></a>

     A. Terzis, J. Krawczyk, J. Wroclawski, and L. Zhang, <br/><strong>&quot;RSVP Operation over IP Tunnels</strong>,&quot; <br/><em>RFC 2746</em>, January  2000.

        <a target="_blank" href="/papers/rfc2746.txt"><img src="/images/extensions/txt.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=49" title="A. Terzis, L. Zhang, S. Vincent, and B. Braden, &lt;strong&gt;&amp;quot;RSVP Diagnostic Messages&lt;/strong&gt;,&amp;quot; &lt;em&gt;RFC 2745&lt;/em&gt;, January  2000. "><img src="/images/extensions/bib.png" /></a>

     A. Terzis, L. Zhang, S. Vincent, and B. Braden, <br/><strong>&quot;RSVP Diagnostic Messages</strong>,&quot; <br/><em>RFC 2745</em>, January  2000.

        <a target="_blank" href="/papers/rfc2745.txt"><img src="/images/extensions/txt.png"></a>

    </li>

</ul><h3>1999</h3>
<ul>


<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=50" title="K. Nichols, V. Jacobson, and L. Zhang, &lt;strong&gt;&amp;quot;A Two-bit Differentiated Services Architecture for the Internet&lt;/strong&gt;,&amp;quot; &lt;em&gt;RFC 2638&lt;/em&gt;, July  1999. "><img src="/images/extensions/bib.png" /></a>

     K. Nichols, V. Jacobson, and L. Zhang, <br/><strong>&quot;A Two-bit Differentiated Services Architecture for the Internet</strong>,&quot; <br/><em>RFC 2638</em>, July  1999.

        <a target="_blank" href="ftp://ftp.isi.edu/in-notes/rfc2638.txt"><img src="/images/extensions/txt.png"></a>

    </li>

</ul><h3>1998</h3>
<ul>


<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=51" title="B. Braden, D. Clark, J. Crowcroft, B. Davie, S. Deering, D. Estrin, S. Floyd, V. Jacobson, G. Minshall, C. Partridge, L. Peterson, K. Ramakrishnan, S. Shenker, J. Wroclawski, and L. Zhang, &lt;strong&gt;&amp;quot;Recommendations on Queue Management and Congestion Avoidance in the Internet&lt;/strong&gt;,&amp;quot; &lt;em&gt;RFC 2309&lt;/em&gt;, April  1998. "><img src="/images/extensions/bib.png" /></a>

     B. Braden, D. Clark, J. Crowcroft, B. Davie, S. Deering, D. Estrin, S. Floyd, V. Jacobson, G. Minshall, C. Partridge, L. Peterson, K. Ramakrishnan, S. Shenker, J. Wroclawski, and L. Zhang, <br/><strong>&quot;Recommendations on Queue Management and Congestion Avoidance in the Internet</strong>,&quot; <br/><em>RFC 2309</em>, April  1998.

        <a target="_blank" href="ftp://ftp.isi.edu/in-notes/rfc2309.txt"><img src="/images/extensions/txt.png"></a>

    </li>

</ul><h3>1997</h3>
<ul>


<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=44" title="R. Braden, Ed., L. Zhang, S. Berson, S. Herzog, and S. Jamin, &lt;strong&gt;&amp;quot;Resource ReSerVation Protocol (RSVP) -- Version 1 Functional Specification&lt;/strong&gt;,&amp;quot; &lt;em&gt;RFC 2205&lt;/em&gt;, September  1997. "><img src="/images/extensions/bib.png" /></a>

     R. Braden, Ed., L. Zhang, S. Berson, S. Herzog, and S. Jamin, <br/><strong>&quot;Resource ReSerVation Protocol (RSVP) -- Version 1 Functional Specification</strong>,&quot; <br/><em>RFC 2205</em>, September  1997.

        <a target="_blank" href="ftp://ftp.isi.edu/in-notes/rfc2205.txt"><img src="/images/extensions/txt.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=52" title="R. Braden and L. Zhang, &lt;strong&gt;&amp;quot;Resource ReSerVation Protocol (RSVP) -- Version 1 Message Processing Rules&lt;/strong&gt;,&amp;quot; &lt;em&gt;RFC 2209&lt;/em&gt;, September  1997. "><img src="/images/extensions/bib.png" /></a>

     R. Braden and L. Zhang, <br/><strong>&quot;Resource ReSerVation Protocol (RSVP) -- Version 1 Message Processing Rules</strong>,&quot; <br/><em>RFC 2209</em>, September  1997.

        <a target="_blank" href="ftp://ftp.isi.edu/in-notes/rfc2209.txt"><img src="/images/extensions/txt.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=53" title="A. Mankin, Ed., F. Baker, B. Braden, S. Bradner, M. O`Dell, A. Romanow, A. Weinrib, and L. Zhang, &lt;strong&gt;&amp;quot;Resource ReSerVation Protocol (RSVP) -- Version 1 Applicability Statement Some Guidelines on Deployment&lt;/strong&gt;,&amp;quot; &lt;em&gt;RFC 2208&lt;/em&gt;, September  1997. "><img src="/images/extensions/bib.png" /></a>

     A. Mankin, Ed., F. Baker, B. Braden, S. Bradner, M. O`Dell, A. Romanow, A. Weinrib, and L. Zhang, <br/><strong>&quot;Resource ReSerVation Protocol (RSVP) -- Version 1 Applicability Statement Some Guidelines on Deployment</strong>,&quot; <br/><em>RFC 2208</em>, September  1997.

        <a target="_blank" href="ftp://ftp.isi.edu/in-notes/rfc2208.txt"><img src="/images/extensions/txt.png"></a>

    </li>
</ul>
</div>
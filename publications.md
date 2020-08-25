---
layout: default
title: Publications
section_id: publications
---

<div class="full parallax" style="background-image: url(images/banner/banner.jpg); color: #fff;">
  <div class="row">
    <div class="large-12 columns">
      {% include section-header.html title="Publications" tagline="" color="#000000" class="big" %}
    </div>
  </div>
  <div class="four spacing"></div>
</div>

<div class="row" style="margin-top: 20px;">
    <h2>COPYRIGHT NOTICE</h2>

    <p>
      The documents here are provided as a means to ensure timely dissemination of technical work on a noncommercial basis. Copyright and all rights therein are maintained by the authors or by other copyright holders. It is understood that anyone copying the papers from this page will adhere to the terms and constraints invoked by the copyright.
    </p>
</div>

<div class="row">

{% assign current_year = site.time | date: "%Y" %}
{% assign months = "January,February,March,April,May,June,July,August,September,October,November,December" | split: "," %}
{% for year in (2001..current_year) reversed %}
  {% assign is_publication_for_year = false %}
  {% for pub in site.data.publications %}
    {% if pub.type == "conference" or pub.type == "journal" or pub.type == "preprint" %}
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
          {% if pub.type == "conference" or pub.type == "journal" or pub.type == "preprint" or pub.type == "chapter" %}
            <li>
            {% if pub.type == "conference" %}
              {{ pub.authors }}<br />
              <strong>"{{ pub.title }}"</strong><br />
              <em>{{ pub.conference }}</em>, {{ month }} {{ year }}.<br />
            {% elsif pub.type == "journal" %}
              {{ pub.authors }}<br />
              <strong>"{{ pub.title }}"</strong><br />
              <em>{{ pub.journal }}</em>, vol. {{ pub.volume }}, {% if pub.issue %}no. {{ pub.issue }}, {% endif %}pp. {{ pub.pages }}, {{ month }} {{ year }}.<br />
            {% elsif pub.type == "preprint" %}
              {{ pub.authors }}<br />
              <strong>"{{ pub.title }}"</strong><br />
              <em>{{ pub.archive }}</em> preprint {{ pub.number }}, {{ month }} {{ year }}.<br />
            {% elsif pub.type == "chapter" %}
              {{ pub.authors }}<br />
              <strong>"{{ pub.title }}"</strong><br />
              {% if pub.chapter %}
                Chapter {{ pub.chapter }},
              {% else %}
                Book chapter,
              {% endif %}
              <em>{{ pub.book }}</em>, {% if pub.isbn %} ISBN {{ pub.isbn }}, {% endif %} {{ pub.publisher }}, {{ month }} {{ year }}.<br />
            {% endif %}
            {% if pub.note %}
            <em>{{ pub.note }}</em><br />
            {% endif %}
            {% if pub.pdf %}
              <a href="data/files/papers/{{ pub.pdf }}" target="_blank"><img src="images/extensions/pdf.png" alt="PDF" /></a>
            {% elsif pub.pdfext %}
              <a href="{{ pub.pdfext }}" target="_blank"><img src="images/extensions/pdf.png" alt="PDF" /></a>
            {% endif %}
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
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=145" title="J. Kong, P. Zerfos, H. Luo, S. Lu, and L. Zhang, &lt;strong&gt;&amp;quot;Providing robust and ubiquitous security support for MANET&lt;/strong&gt;,&amp;quot; in &lt;em&gt;Proceedings of IEEE International Conference on Network Protocols (ICNP)&lt;/em&gt;, November  2001. "><img src="/images/extensions/bib.png" /></a>

     J. Kong, P. Zerfos, H. Luo, S. Lu, and L. Zhang, <br/><strong>&quot;Providing robust and ubiquitous security support for MANET</strong>,&quot; <br/>in <em>Proceedings of IEEE International Conference on Network Protocols (ICNP)</em>, November  2001.

        <a target="_blank" href="/papers/ICNP01-haiyun.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=146" title="Joe Albowicz, Alvin Chen, and Lixia Zhang, &lt;strong&gt;&amp;quot;Recursive Position Estimation in Sensor Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE Internation Conference on Network Protocols (ICNP)&lt;/em&gt;, November  2001. "><img src="/images/extensions/bib.png" /></a>

     Joe Albowicz, Alvin Chen, and Lixia Zhang, <br/><strong>&quot;Recursive Position Estimation in Sensor Networks</strong>,&quot; <br/><em>IEEE Internation Conference on Network Protocols (ICNP)</em>, November  2001.

        <a target="_blank" href="/papers/grab-icnp01.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=147" title="Allison Mankin, Dan Massey, Chie Lung Wu, Felix S. Wu, and Lixia Zhang, &lt;strong&gt;&amp;quot;On Design and Evaluation of &#039;Intention-Driven&#039; ICMP Traceback&lt;/strong&gt;,&amp;quot; &lt;em&gt;10th International Conference on Computer Communications and Networks (IC3N)&lt;/em&gt;, October  2001. "><img src="/images/extensions/bib.png" /></a>

     Allison Mankin, Dan Massey, Chie Lung Wu, Felix S. Wu, and Lixia Zhang, <br/><strong>&quot;On Design and Evaluation of 'Intention-Driven' ICMP Traceback</strong>,&quot; <br/><em>10th International Conference on Computer Communications and Networks (IC3N)</em>, October  2001.

        <a target="_blank" href="/papers/Intention-iTrace.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=148" title="Fan Ye, Alvin Chen, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;A Scalable Solution to Minimum Cost Forwarding in Large Scale Sensor Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;International Conference on Computer Communications and Networks (IC3N)&lt;/em&gt;, October  2001. "><img src="/images/extensions/bib.png" /></a>

     Fan Ye, Alvin Chen, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;A Scalable Solution to Minimum Cost Forwarding in Large Scale Sensor Networks</strong>,&quot; <br/><em>International Conference on Computer Communications and Networks (IC3N)</em>, October  2001.

        <a target="_blank" href="/papers/grab-icccn01.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=149" title="P. Francis, S. Jamin, C. Jin, Y. Jin, D. Raz, Y. Shavitt, , and L. Zhang, &lt;strong&gt;&amp;quot;IDMAPS: A Global Internet Host Distance Estimate Service&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE/ACM Transactions on Networking, Vol. 9, No 5, PP525-540&lt;/em&gt;, October  2001. "><img src="/images/extensions/bib.png" /></a>

     P. Francis, S. Jamin, C. Jin, Y. Jin, D. Raz, Y. Shavitt, , and L. Zhang, <br/><strong>&quot;IDMAPS: A Global Internet Host Distance Estimate Service</strong>,&quot;quot; <br/><em>IEEE/ACM Transactions on Networking, Vol. 9, No 5, PP525-540</em>, October  2001.

        <a target="_blank" href="/papers/ton01-idmaps.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=150" title="Xiaoliang Zhao, Dan Pei, Lan Wang, Dan Massey, Allison Mankin, Felix S. Wu, and Lixia Zhang, &lt;strong&gt;&amp;quot;An Analysis of BGP Multiple Origin AS(MOAS) Conflicts&lt;/strong&gt;,&amp;quot; &lt;em&gt;SIGCOMM Internet Measurement Workshop&lt;/em&gt;, August  2001. "><img src="/images/extensions/bib.png" /></a>

     Xiaoliang Zhao, Dan Pei, Lan Wang, Dan Massey, Allison Mankin, Felix S. Wu, and Lixia Zhang, <br/><strong>&quot;An Analysis of BGP Multiple Origin AS(MOAS) Conflicts</strong>,&quot; <br/><em>SIGCOMM Internet Measurement Workshop</em>, August  2001.

        <a target="_blank" href="/papers/fniisc-sigcomm-workshop01.ps"><img src="/images/extensions/ps.png"></a>

    </li>

</ul><h3>2000</h3>
<ul>


<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=151" title="Andreas Terzis, Konstantinos Nikoloudakis, Lan Wang, and Lixia Zhang, &lt;strong&gt;&amp;quot;IRLSim: A general purpose packet level network simulator&lt;/strong&gt;,&amp;quot; &lt;em&gt;33rd Annual Simulation Symposium, Washington D.C.&lt;/em&gt; April  2000. "><img src="/images/extensions/bib.png" /></a>

     Andreas Terzis, Konstantinos Nikoloudakis, Lan Wang, and Lixia Zhang, <br/><strong>&quot;IRLSim: A general purpose packet level network simulator</strong>,&quot; <br/><em>33rd Annual Simulation Symposium, Washington D.C.</em> April  2000.

        <a target="_blank" href="/papers/irlsim.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=152" title="Michel, B. S., Nikoloudakis, K., Reiher, P., , Zhang, and L. &lt;strong&gt;&amp;quot;URL Forwarding and Compression in Adaptive Web Caching&lt;/strong&gt;,&amp;quot; &lt;em&gt;INFOCOM&lt;/em&gt;, March  2000. "><img src="/images/extensions/bib.png" /></a>

     Michel, B. S., Nikoloudakis, K., Reiher, P., , Zhang, and L. <br/><strong>&quot;URL Forwarding and Compression in Adaptive Web Caching</strong>,&quot; <br/><em>INFOCOM</em>, March  2000.

        <a target="_blank" href="http://flapps.cs.ucla.edu/papers/AWC-INFOCOM2K.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=153" title="S. Jamin, C. Jin, Y. Jin, D. Raz, Y. Shavitt, and L. Zhang, &lt;strong&gt;&amp;quot;On the Placement of Internet Instrumentation&lt;/strong&gt;,&amp;quot; &lt;em&gt;INFOCOM&lt;/em&gt;, March  2000. "><img src="/images/extensions/bib.png" /></a>

     S. Jamin, C. Jin, Y. Jin, D. Raz, Y. Shavitt, and L. Zhang, <br/><strong>&quot;On the Placement of Internet Instrumentation</strong>,&quot; <br/><em>INFOCOM</em>, March  2000.

        <a target="_blank" href="http://idmaps.eecs.umich.edu/papers/infocom00.ps"><img src="/images/extensions/ps.png"></a>

    </li>

</ul><h3>1999</h3>
<ul>


<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=154" title="Andreas Terzis, Lan Wang, Jun Ogawa, and Lixia Zhang, &lt;strong&gt;&amp;quot;A Two-Tier Resource Management Model for the Internet&lt;/strong&gt;,&amp;quot; in &lt;em&gt;Proceedings of Global Internet 99&lt;/em&gt;, December  1999. "><img src="/images/extensions/bib.png" /></a>

     Andreas Terzis, Lan Wang, Jun Ogawa, and Lixia Zhang, <br/><strong>&quot;A Two-Tier Resource Management Model for the Internet</strong>,&quot; <br/>in <em>Proceedings of Global Internet 99</em>, December  1999.

        <a target="_blank" href="/papers/paper-final-gi99.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=155" title="C. G. Liu, D. Estrin, S. Shenker, and L. Zhang, &lt;strong&gt;&amp;quot;Recovery Timer Adaptation in SRM&lt;/strong&gt;,&amp;quot; in &lt;em&gt;Proceedings of ICCC&lt;/em&gt;, October  1999. "><img src="/images/extensions/bib.png" /></a>

     C. G. Liu, D. Estrin, S. Shenker, and L. Zhang, <br/><strong>&quot;Recovery Timer Adaptation in SRM</strong>,&quot; <br/>in <em>Proceedings of ICCC</em>, October  1999.

        <a target="_blank" href="/papers/ICCC99.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=156" title="Lan Wang, Andreas Terzis, and Lixia Zhang, &lt;strong&gt;&amp;quot;A New Proposal for RSVP Refreshes&lt;/strong&gt;,&amp;quot; in &lt;em&gt;Proceedings of the 7th International Conference on Network Protocols (ICNP)&lt;/em&gt;, October  1999. "><img src="/images/extensions/bib.png" /></a>

     Lan Wang, Andreas Terzis, and Lixia Zhang, <br/><strong>&quot;A New Proposal for RSVP Refreshes</strong>,&quot; <br/>in <em>Proceedings of the 7th International Conference on Network Protocols (ICNP)</em>, October  1999.

        <a target="_blank" href="/papers/ICNP99.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=157" title="N. Sturtevant, N. Tang, and L. Zhang, &lt;strong&gt;&amp;quot;The Information Discovery Graph: Towards a Scalable Multimedia Resource Directory&lt;/strong&gt;,&amp;quot; in &lt;em&gt;Proceedings of IEEE Workshop on Internet Applications&lt;/em&gt;, July  1999. "><img src="/images/extensions/bib.png" /></a>

     N. Sturtevant, N. Tang, and L. Zhang, <br/><strong>&quot;The Information Discovery Graph: Towards a Scalable Multimedia Resource Directory</strong>,&quot; <br/>in <em>Proceedings of IEEE Workshop on Internet Applications</em>, July  1999.

        <a target="_blank" href="/papers/IDG_WIAPP_paper.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=158" title="Mario Gerla, Rajive Bagrodia, Lixia Zhang, Ken Tang, and Lan Wang, &lt;strong&gt;&amp;quot;TCP over Wireless Multihop Protocols: Simulation and Experiments&lt;/strong&gt;,&amp;quot; in &lt;em&gt;Proceedings of International Conference on Communications (ICC)&lt;/em&gt;, June  1999. "><img src="/images/extensions/bib.png" /></a>

     Mario Gerla, Rajive Bagrodia, Lixia Zhang, Ken Tang, and Lan Wang, <br/><strong>&quot;TCP over Wireless Multihop Protocols: Simulation and Experiments</strong>,&quot; <br/>in <em>Proceedings of International Conference on Communications (ICC)</em>, June  1999.

        <a target="_blank" href="/papers/icc99.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=159" title="Andreas Terzis, Jun Ogawa, Sonia Tsui, Lan Wang, and Lixia Zhang, &lt;strong&gt;&amp;quot;A Prototype Implementation of the Two-Tier Architecture for Differentiated Services&lt;/strong&gt;,&amp;quot; in &lt;em&gt;Proceedings of RTAS99&lt;/em&gt;, June  1999. "><img src="/images/extensions/bib.png" /></a>

     Andreas Terzis, Jun Ogawa, Sonia Tsui, Lan Wang, and Lixia Zhang, <br/><strong>&quot;A Prototype Implementation of the Two-Tier Architecture for Differentiated Services</strong>,&quot; <br/>in <em>Proceedings of RTAS99</em>, June  1999.

        <a target="_blank" href="/papers/rtas99-final.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=160" title="A. Terzis, M. Srivastava, and L. Zhang, &lt;strong&gt;&amp;quot;A Simple QoS Signaling Protocol for Mobile Hosts in the Integrated Services Internet&lt;/strong&gt;,&amp;quot; in &lt;em&gt;Proceedings of IEEE INFOCOM&lt;/em&gt;, March  1999. "><img src="/images/extensions/bib.png" /></a>

     A. Terzis, M. Srivastava, and L. Zhang, <br/><strong>&quot;A Simple QoS Signaling Protocol for Mobile Hosts in the Integrated Services Internet</strong>,&quot; <br/>in <em>Proceedings of IEEE INFOCOM</em>, March  1999.

        <a target="_blank" href="/papers/infocom99.ps.gz"><img src="/images/extensions/gz.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=161" title="P. Francis, S. Jamin, V. Paxson, L. Zhang, D. Gryniewicz, and Y. Jin, &lt;strong&gt;&amp;quot;An Architecture for a Global Internet Host Distance Estimation Service&lt;/strong&gt;,&amp;quot; in &lt;em&gt;Proceedings of IEEE INFOCOM&lt;/em&gt;, March  1999. "><img src="/images/extensions/bib.png" /></a>

     P. Francis, S. Jamin, V. Paxson, L. Zhang, D. Gryniewicz, and Y. Jin, <br/><strong>&quot;An Architecture for a Global Internet Host Distance Estimation Service</strong>,&quot; <br/>in <em>Proceedings of IEEE INFOCOM</em>, March  1999.

        <a target="_blank" href="http://idmaps.eecs.umich.edu/papers/infocom99.ps.gz"><img src="/images/extensions/gz.png"></a>

    </li>

</ul><h3>1998</h3>
<ul>


<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=162" title="C. Liu, D. Estrin, S. Shenker, and L. Zhang, &lt;strong&gt;&amp;quot;Local Error Recovery in SRM: Comparison of Two Approaches&lt;/strong&gt;,&amp;quot; &lt;em&gt;EEE/ACM Transactions on Networking&lt;/em&gt;, vol. 6, no. 6, pp. 686&amp;ndash;699, December  1998. "><img src="/images/extensions/bib.png" /></a>

     C. Liu, D. Estrin, S. Shenker, and L. Zhang, <br/><strong>&quot;Local Error Recovery in SRM: Comparison of Two Approaches</strong>,&quot; <br/><em>EEE/ACM Transactions on Networking</em>, vol. 6, no. 6, pp. 686&ndash;699, December  1998.

        <a target="_blank" href="/papers/TON_97_1.PS.gz"><img src="/images/extensions/gz.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=163" title="A. Fei, G. Pei, R. Liu, and L. Zhang, &lt;strong&gt;&amp;quot;Measurements on Delay and Hop-Count of the Internet&lt;/strong&gt;,&amp;quot; in &lt;em&gt;Proceedings of GLOBECOM&lt;/em&gt;, November  1998. "><img src="/images/extensions/bib.png" /></a>

     A. Fei, G. Pei, R. Liu, and L. Zhang, <br/><strong>&quot;Measurements on Delay and Hop-Count of the Internet</strong>,&quot; <br/>in <em>Proceedings of GLOBECOM</em>, November  1998.

        <a target="_blank" href="/papers/internet-measurement.ps.gz"><img src="/images/extensions/gz.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=164" title="A. Terzis, L. Wang, and L. Zhang, &lt;strong&gt;&amp;quot;A Scalable Resource Management Framework for Differentiated Services Internet&lt;/strong&gt;,&amp;quot; in &lt;em&gt;Proceedings of the 3rd NASA/NREN Workshop on QoS for the Next Generation Internet&lt;/em&gt;, August  1998. "><img src="/images/extensions/bib.png" /></a>

     A. Terzis, L. Wang, and L. Zhang, <br/><strong>&quot;A Scalable Resource Management Framework for Differentiated Services Internet</strong>,&quot; <br/>in <em>Proceedings of the 3rd NASA/NREN Workshop on QoS for the Next Generation Internet</em>, August  1998.

        <a target="_blank" href="/papers/NREN-final.txt"><img src="/images/extensions/txt.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=165" title="A. Terzis, L. Zhang, and E. Hahne, &lt;strong&gt;&amp;quot;Making Reservations for Aggregate Flows: Experiences from an RSVP Tunnels Implementation&lt;/strong&gt;,&amp;quot; in &lt;em&gt;Proceedings of IWQoS&lt;/em&gt;, Napa Valley, CA, May  1998. "><img src="/images/extensions/bib.png" /></a>

     A. Terzis, L. Zhang, and E. Hahne, <br/><strong>&quot;Making Reservations for Aggregate Flows: Experiences from an RSVP Tunnels Implementation</strong>,&quot; <br/>in <em>Proceedings of IWQoS</em>, Napa Valley, CA, May  1998.

        <a target="_blank" href="/papers/rsvp-tunnels-camera.ps.gz"><img src="/images/extensions/gz.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=166" title="R. Bruyeron, B. Hemon, and L. Zhang, &lt;strong&gt;&amp;quot;Exprerimentatons with TCP Selective Acknowledgement&lt;/strong&gt;,&amp;quot; &lt;em&gt;CCR&lt;/em&gt;, vol. 28, no. 2, April  1998. "><img src="/images/extensions/bib.png" /></a>

     R. Bruyeron, B. Hemon, and L. Zhang, <br/><strong>&quot;Exprerimentatons with TCP Selective Acknowledgement</strong>,&quot; <br/><em>CCR</em>, vol. 28, no. 2, April  1998.

        <a target="_blank" href="/papers/sack_exp.ps.gz"><img src="/images/extensions/gz.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=167" title="S. Dao, B. Perry, E. Shek, A. Vellaikal, R. Muntz, L. Zhang, M. Potkonjak, , and O. Wolfson, &lt;strong&gt;&amp;quot;Semantic Multicast: Intelligently Sharing Collaborative Sessions&lt;/strong&gt;,&amp;quot; &lt;em&gt;ACM Computing Survey&lt;/em&gt;, January  1998. "><img src="/images/extensions/bib.png" /></a>

     S. Dao, B. Perry, E. Shek, A. Vellaikal, R. Muntz, L. Zhang, M. Potkonjak, , and O. Wolfson, <br/><strong>&quot;Semantic Multicast: Intelligently Sharing Collaborative Sessions</strong>,&quot; <br/><em>ACM Computing Survey</em>, January  1998.

        <a target="_blank" href="http://www.wins.hrl.com/projects/semcast/semcast_whitepaper.ps"><img src="/images/extensions/ps.png"></a>

    </li>

</ul><h3>1997</h3>
<ul>


<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=168" title="A. Rosenstein, J. Li, and S. Y. Tong, &lt;strong&gt;&amp;quot;MASH: The Multicasting Archie Server Hierearchy&lt;/strong&gt;,&amp;quot; &lt;em&gt;CCR&lt;/em&gt;, vol. 27, no. 3, July  1997. "><img src="/images/extensions/bib.png" /></a>

     A. Rosenstein, J. Li, and S. Y. Tong, <br/><strong>&quot;MASH: The Multicasting Archie Server Hierearchy</strong>,&quot; <br/><em>CCR</em>, vol. 27, no. 3, July  1997.

        <a target="_blank" href="http://www.cs.ucla.edu/%7Eadam/report.ps.gz"><img src="/images/extensions/gz.png"></a>

    </li>

    </ul>
</div>
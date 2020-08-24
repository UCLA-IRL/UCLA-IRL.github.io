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
{% for year in (2006..current_year) reversed %}
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
          {% if pub.type == "conference" or pub.type == "journal" or pub.type == "preprint" %}
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

<h3>2005</h3>
<ul>


<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=88" title="Ricardo V. Oliveira, Rafit Izhak-Ratzin, Beichuan Zhang, and Lixia Zhang, &lt;strong&gt;&amp;quot;Measurement of Highly Active Prefixes in BGP&lt;/strong&gt;,&amp;quot; &lt;em&gt;In GLOBECOM&lt;/em&gt;, November  2005. "><img src="/images/extensions/bib.png" /></a>

     Ricardo V. Oliveira, Rafit Izhak-Ratzin, Beichuan Zhang, and Lixia Zhang, <br/><strong>&quot;Measurement of Highly Active Prefixes in BGP</strong>,&quot; <br/><em>In GLOBECOM</em>, November  2005.

        <a target="_blank" href="/papers/activity.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=89" title="Hyo-Joeng Shin, Dan Pei, Mohit Lad, Yanghee Choi, , and Lixia Zhang, &lt;strong&gt;&amp;quot;The Impact of Multi-homing on Network Reliability and Stability: A Case Study&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE ICCCN&lt;/em&gt;, October  2005. "><img src="/images/extensions/bib.png" /></a>

     Hyo-Joeng Shin, Dan Pei, Mohit Lad, Yanghee Choi, , and Lixia Zhang, <br/><strong>&quot;The Impact of Multi-homing on Network Reliability and Stability: A Case Study</strong>,&quot; <br/><em>IEEE ICCCN</em>, October  2005.

        <a target="_blank" href="/papers/imh.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=90" title="Beichuan Zhang, Vamsi Kambhampati, Mohit Lad, Daniel Massey, and Lixia Zhang, &lt;strong&gt;&amp;quot;Identifying  BGP Routing Table Transfers&lt;/strong&gt;,&amp;quot; &lt;em&gt;SIGCOMM Mining the Network Data (MineNet) Workshop&lt;/em&gt;, August  2005. "><img src="/images/extensions/bib.png" /></a>

     Beichuan Zhang, Vamsi Kambhampati, Mohit Lad, Daniel Massey, and Lixia Zhang, <br/><strong>&quot;Identifying  BGP Routing Table Transfers</strong>,&quot; <br/><em>SIGCOMM Mining the Network Data (MineNet) Workshop</em>, August  2005.

        <a target="_blank" href="/papers/05-minenet-mct.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=91" title="D. Clark, C. Partridge, R. Braden, B. Davie, S. Floyd, V. Jacobson, D. Katabi, G. Minshall, K. K. Ramakrishnan, T. Roscoe, I. Stoica, J. Wroclawski, , and L. Zhang, &lt;strong&gt;&amp;quot;Making the World (of Communications) a Different Place&lt;/strong&gt;,&amp;quot; &lt;em&gt;ACMComputer Communication Review,Vol. 35, No. 3, pp. 91-96&lt;/em&gt;, July  2005. "><img src="/images/extensions/bib.png" /></a>

     D. Clark, C. Partridge, R. Braden, B. Davie, S. Floyd, V. Jacobson, D. Katabi, G. Minshall, K. K. Ramakrishnan, T. Roscoe, I. Stoica, J. Wroclawski, , and L. Zhang, <br/><strong>&quot;Making the World (of Communications) a Different Place</strong>,&quot; <br/><em>ACMComputer Communication Review,Vol. 35, No. 3, pp. 91-96</em>, July  2005.

        <a target="_blank" href="/papers/e2e-vision.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=92" title="Beichuan Zhang, Dan Pei, Daniel Massey, and Lixia Zhang, &lt;strong&gt;&amp;quot;Timer Interaction in Route Flap Damping&lt;/strong&gt;,&amp;quot; &lt;em&gt;The 25th International Conference on Distributed Computing Systems (ICDCS)&lt;/em&gt;, June  2005. "><img src="/images/extensions/bib.png" /></a>

     Beichuan Zhang, Dan Pei, Daniel Massey, and Lixia Zhang, <br/><strong>&quot;Timer Interaction in Route Flap Damping</strong>,&quot; <br/><em>The 25th International Conference on Distributed Computing Systems (ICDCS)</em>, June  2005.

        <a target="_blank" href="http://www.cs.ucla.edu/~bzhang/paper/dtimer.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=93" title="Dan Pei, Matt Azuma, Daniel Massey, , and Lixia Zhang, &lt;strong&gt;&amp;quot;BGP-RCN: Improving BGP Convergence Through Root Cause Notification&lt;/strong&gt;,&amp;quot; &lt;em&gt;Computer Networks, Volume 48, Issue 2, Pages 175-194&lt;/em&gt;, June  2005. "><img src="/images/extensions/bib.png" /></a>

     Dan Pei, Matt Azuma, Daniel Massey, , and Lixia Zhang, <br/><strong>&quot;BGP-RCN: Improving BGP Convergence Through Root Cause Notification</strong>,&quot; <br/><em>Computer Networks, Volume 48, Issue 2, Pages 175-194</em>, June  2005.

        <a target="_blank" href="/papers/massey_comnet05.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=94" title="Fan Ye, Haiyun Luo, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;Statistical En-Route Filtering in Wireless Sensor Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE Jounal on Selected Areas in Communications, Special Issue on Self-organizing Distributed Collaborative Sensor Networks, Vol. 23, No. 4, pp. 839-850&lt;/em&gt;, April  2005. "><img src="/images/extensions/bib.png" /></a>

     Fan Ye, Haiyun Luo, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;Statistical En-Route Filtering in Wireless Sensor Networks</strong>,&quot; <br/><em>IEEE Jounal on Selected Areas in Communications, Special Issue on Self-organizing Distributed Collaborative Sensor Networks, Vol. 23, No. 4, pp. 839-850</em>, April  2005.

        <a target="_blank" href="/papers/sef-jsac.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=95" title="Xiaoliang Zhao, Beichuan Zhang, Andreas Terzis, Daniel Massey, and Lixia Zhang, &lt;strong&gt;&amp;quot;The Impact of Link Failure Location on Routing Dynamics: A Formal Analysis&lt;/strong&gt;,&amp;quot; &lt;em&gt;ACM SIGCOMM Asia Workshop&lt;/em&gt;, April  2005. "><img src="/images/extensions/bib.png" /></a>

     Xiaoliang Zhao, Beichuan Zhang, Andreas Terzis, Daniel Massey, and Lixia Zhang, <br/><strong>&quot;The Impact of Link Failure Location on Routing Dynamics: A Formal Analysis</strong>,&quot; <br/><em>ACM SIGCOMM Asia Workshop</em>, April  2005.

        <a target="_blank" href="/papers/05-asia-location.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=96" title="Zhenghua Fu, Haiyun Luo, Petros Zerfos, Songwu Lu, Lixia Zhang, and Mario Gerla, &lt;strong&gt;&amp;quot;The Impact of Multihop Wireless Channel on TCP Performance&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE Transactions on Mobile Computing, Vol. 4, No. 2, pp. 209-221&lt;/em&gt;, March  2005. "><img src="/images/extensions/bib.png" /></a>

     Zhenghua Fu, Haiyun Luo, Petros Zerfos, Songwu Lu, Lixia Zhang, and Mario Gerla, <br/><strong>&quot;The Impact of Multihop Wireless Channel on TCP Performance</strong>,&quot; <br/><em>IEEE Transactions on Mobile Computing, Vol. 4, No. 2, pp. 209-221</em>, March  2005.

        <a target="_blank" href="http://www.cs.ucla.edu/wing/publication/papers/Fu.TMC04.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=97" title="Fan Ye, Gary Zhong, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;GRAdient Broadcast: A robust Data Delivery Protocol for Large Scale Sensor Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;ACM Wireless Networks (WINET) Journal, Vol. 11, No.2&lt;/em&gt;, March  2005. "><img src="/images/extensions/bib.png" /></a>

     Fan Ye, Gary Zhong, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;GRAdient Broadcast: A robust Data Delivery Protocol for Large Scale Sensor Networks</strong>,&quot; <br/><em>ACM Wireless Networks (WINET) Journal, Vol. 11, No.2</em>, March  2005.

        <a target="_blank" href="/papers/grab-winet.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=98" title="Haiyun Luo, Fan Ye, Jerry Cheng, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;TTDD: Two-Tier Data Dissemination in Large-scale Wireless Sensor Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;ACM Wireless Networks, Vol. 11, Issue 1-2, pp. 161-175,&lt;/em&gt; January  2005. "><img src="/images/extensions/bib.png" /></a>

     Haiyun Luo, Fan Ye, Jerry Cheng, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;TTDD: Two-Tier Data Dissemination in Large-scale Wireless Sensor Networks</strong>,&quot; <br/><em>ACM Wireless Networks, Vol. 11, Issue 1-2, pp. 161-175,</em> January  2005.

        <a target="_blank" href="http://www-faculty.cs.uiuc.edu/~haiyun/publications/WINET05.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=99" title="Beichuan Zhang, Raymond Liu, Daniel Massey, and Lixia Zhang, &lt;strong&gt;&amp;quot;Collecting the Internet AS-level Topology&lt;/strong&gt;,&amp;quot; &lt;em&gt;ACM SIGCOMM Computer Communication Review (CCR) special issue on Internet Vital Statistics&lt;/em&gt;, January  2005. "><img src="/images/extensions/bib.png" /></a>

     Beichuan Zhang, Raymond Liu, Daniel Massey, and Lixia Zhang, <br/><strong>&quot;Collecting the Internet AS-level Topology</strong>,&quot; <br/><em>ACM SIGCOMM Computer Communication Review (CCR) special issue on Internet Vital Statistics</em>, January  2005.

        <a target="_blank" href="/papers/05-ccr-topology.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=100" title="Xiaoqiao Meng, Zhiguo Xu, Beichuan Zhang, Geoff Huston, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;IPv4 Address Allocation and BGP Routing Table Evolution&lt;/strong&gt;,&amp;quot; &lt;em&gt;ACM SIGCOMM Computer Communication Review (CCR) special issue on Internet Vital Statistics&lt;/em&gt;, January  2005. "><img src="/images/extensions/bib.png" /></a>

     Xiaoqiao Meng, Zhiguo Xu, Beichuan Zhang, Geoff Huston, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;IPv4 Address Allocation and BGP Routing Table Evolution</strong>,&quot; <br/><em>ACM SIGCOMM Computer Communication Review (CCR) special issue on Internet Vital Statistics</em>, January  2005.

        <a target="_blank" href="/papers/05-ccr-address.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=101" title="Fan Ye, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;A Randomized Energy-Conservation Protocol for Resilient Sensor Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;ACM Wireless Networks&lt;/em&gt;, January  2005. "><img src="/images/extensions/bib.png" /></a>

     Fan Ye, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;A Randomized Energy-Conservation Protocol for Resilient Sensor Networks</strong>,&quot; <br/><em>ACM Wireless Networks</em>, January  2005.

        <a target="_blank" href="/papers/peas-winet.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>

</ul><h3>2004</h3>
<ul>


<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=102" title="Haiyun Luo, Jiejun Kong, Petros Zerfos, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;URSA: Ubiquitous and Robust Access Control for Mobile Ad-Hoc Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE/ACM Transactions on Networking (pp1049-1063)&lt;/em&gt;, December  2004. "><img src="/images/extensions/bib.png" /></a>

     Haiyun Luo, Jiejun Kong, Petros Zerfos, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;URSA: Ubiquitous and Robust Access Control for Mobile Ad-Hoc Networks</strong>,&quot; <br/><em>IEEE/ACM Transactions on Networking (pp1049-1063)</em>, December  2004.

        <a target="_blank" href="/papers/Luo.TON04.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=103" title="V. Pappas, Z. Xu, S. Lu, D. Massey, A. Terzis, and L. Zhang, &lt;strong&gt;&amp;quot;Impact of Configuration Errors on DNS Robustness&amp;quot;&lt;/strong&gt;,&amp;quot; in &lt;em&gt;Proceedings of ACM SIGCOMM&lt;/em&gt;, August  2004. "><img src="/images/extensions/bib.png" /></a>

     V. Pappas, Z. Xu, S. Lu, D. Massey, A. Terzis, and L. Zhang, <br/><strong>&quot;Impact of Configuration Errors on DNS Robustness&quot;</strong>,&quot; <br/>in <em>Proceedings of ACM SIGCOMM</em>, August  2004.

        <a target="_blank" href="/papers/vp_sigcomm04.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=104" title="V. Pappas, P.Faltstrom, D. Massey, and L. Zhang, &lt;strong&gt;&amp;quot;Distributed DNS Troubleshooting&lt;/strong&gt;,&amp;quot; in &lt;em&gt;Proceedings of ACM SIGCOMM Network Troubleshooting Workshop&lt;/em&gt;, August  2004. "><img src="/images/extensions/bib.png" /></a>

     V. Pappas, P.Faltstrom, D. Massey, and L. Zhang, <br/><strong>&quot;Distributed DNS Troubleshooting</strong>,&quot; <br/>in <em>Proceedings of ACM SIGCOMM Network Troubleshooting Workshop</em>, August  2004.

        <a target="_blank" href="/papers/vp_nts04.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=105" title="Fan Ye, Haiyun Luo, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;Statistical En-route Detection and Filtering of Injected False Data in Sensor Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE INFOCOM&lt;/em&gt;, August  2004. "><img src="/images/extensions/bib.png" /></a>

     Fan Ye, Haiyun Luo, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;Statistical En-route Detection and Filtering of Injected False Data in Sensor Networks</strong>,&quot; <br/><em>IEEE INFOCOM</em>, August  2004.

        <a target="_blank" href="/papers/fan_sef_infocom04.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=106" title="Yuval Shavitt, Dan Raz, and Lixia Zhang, &lt;strong&gt;&amp;quot;Distributed Council Election&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE/ACM Transactions on Networking, 12 (3):483-492&lt;/em&gt;, June  2004. "><img src="/images/extensions/bib.png" /></a>

     Yuval Shavitt, Dan Raz, and Lixia Zhang, <br/><strong>&quot;Distributed Council Election</strong>,&quot; <br/><em>IEEE/ACM Transactions on Networking, 12 (3):483-492</em>, June  2004.

        <a target="_blank" href="/papers/dce-2004-06.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=107" title="Hao Yang, Haiyun Luo, Yang Yi, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;HOURS: Achieving DoS Resilience in an Open Service Hierarchy&lt;/strong&gt;,&amp;quot; &lt;em&gt;The International Conference on Dependable Systems and Networks (DSN), Florence, Italy&lt;/em&gt;, June  2004. "><img src="/images/extensions/bib.png" /></a>

     Hao Yang, Haiyun Luo, Yang Yi, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;HOURS: Achieving DoS Resilience in an Open Service Hierarchy</strong>,&quot; <br/><em>The International Conference on Dependable Systems and Networks (DSN), Florence, Italy</em>, June  2004.

        <a target="_blank" href="/papers/DSN04.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=108" title="Dan Pei, Dan Massey, , and Lixia Zhang, &lt;strong&gt;&amp;quot;A Framework for Resilient Internet Routing Protocols&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE Network special issue on Protection, Restoration, and Disaster Recovery&lt;/em&gt;, April  2004. "><img src="/images/extensions/bib.png" /></a>

     Dan Pei, Dan Massey, , and Lixia Zhang, <br/><strong>&quot;A Framework for Resilient Internet Routing Protocols</strong>,&quot; <br/><em>IEEE Network special issue on Protection, Restoration, and Disaster Recovery</em>, April  2004.

        <a target="_blank" href="http://www.cs.ucla.edu/%7Epeidan/network-resilient.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=109" title="Lan Wang, Xiaoliang Zhao, Dan Pei, Randy Bush, Dan Massey, , and Lixia Zhang, &lt;strong&gt;&amp;quot;Protecting BGP Routes to Top Level DNS Servers&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE Transactions on Parallel and Distributed Systems&lt;/em&gt;, April  2004. "><img src="/images/extensions/bib.png" /></a>

     Lan Wang, Xiaoliang Zhao, Dan Pei, Randy Bush, Dan Massey, , and Lixia Zhang, <br/><strong>&quot;Protecting BGP Routes to Top Level DNS Servers</strong>,&quot; <br/><em>IEEE Transactions on Parallel and Distributed Systems</em>, April  2004.

        <a target="_blank" href="http://www.cs.ucla.edu/~lixia/papers/03TPDS.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=110" title="Dan Pei, Matt Azuma, Dan Massey, and Lixia Zhang, &lt;strong&gt;&amp;quot;BGP-RCN: Improving BGP Convergence Through Root Cause Notification&lt;/strong&gt;,&amp;quot; &lt;em&gt;Computer Networks&lt;/em&gt;, April  2004. "><img src="/images/extensions/bib.png" /></a>

     Dan Pei, Matt Azuma, Dan Massey, and Lixia Zhang, <br/><strong>&quot;BGP-RCN: Improving BGP Convergence Through Root Cause Notification</strong>,&quot; <br/><em>Computer Networks</em>, April  2004.

        <a target="_blank" href="/data/files/papers/BGP-RCN.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=111" title="B. Zhang, D. Massey, and L. Zhang, &lt;strong&gt;&amp;quot;Destination Reachability and BGP Convergence Time&lt;/strong&gt;,&amp;quot; &lt;em&gt;GLOBECOM&lt;/em&gt;, April  2004. "><img src="/images/extensions/bib.png" /></a>

     B. Zhang, D. Massey, and L. Zhang, <br/><strong>&quot;Destination Reachability and BGP Convergence Time</strong>,&quot; <br/><em>GLOBECOM</em>, April  2004.

        <a target="_blank" href="/papers/PID43182.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=112" title="Lan Wang, Dan Massey, Keyur Patel, and Lixia Zhang, &lt;strong&gt;&amp;quot;FRTR: A Scalable Mechanism to Restore Routing Table Consistency&lt;/strong&gt;,&amp;quot; &lt;em&gt;DSN&lt;/em&gt;, April  2004. "><img src="/images/extensions/bib.png" /></a>

     Lan Wang, Dan Massey, Keyur Patel, and Lixia Zhang, <br/><strong>&quot;FRTR: A Scalable Mechanism to Restore Routing Table Consistency</strong>,&quot; <br/><em>DSN</em>, April  2004.

        <a target="_blank" href="/papers/frtr.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=113" title="Mohit Lad, Dan Massey, and Lixia Zhang, &lt;strong&gt;&amp;quot;Link-Rank: A Graphical Tool for Capturing Routing Dynamics&lt;/strong&gt;,&amp;quot; &lt;em&gt;Proceedings of The IEEE/IPIF Network Operations and Management Symposium (NOMS)&lt;/em&gt;, April  2004. "><img src="/images/extensions/bib.png" /></a>

     Mohit Lad, Dan Massey, and Lixia Zhang, <br/><strong>&quot;Link-Rank: A Graphical Tool for Capturing Routing Dynamics</strong>,&quot; <br/><em>Proceedings of The IEEE/IPIF Network Operations and Management Symposium (NOMS)</em>, April  2004.

        <a target="_blank" href="/papers/LinkRank.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=114" title="V. Pappas, B. Zhang, A. Terzis, and L. Zhang, &lt;strong&gt;&amp;quot;Fault-Tolerant Data Delivery for Multicast Overlay Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;24th IEEE International Conference on Distributed Computing Systems (ICDCS)&lt;/em&gt;, March  2004. "><img src="/images/extensions/bib.png" /></a>

     V. Pappas, B. Zhang, A. Terzis, and L. Zhang, <br/><strong>&quot;Fault-Tolerant Data Delivery for Multicast Overlay Networks</strong>,&quot; <br/><em>24th IEEE International Conference on Distributed Computing Systems (ICDCS)</em>, March  2004.

        <a target="_blank" href="/papers/vp_icdcs04.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=115" title="Dan Pei, Xiaoliang Zhao, Dan Massey, and Lixia Zhang, &lt;strong&gt;&amp;quot;A Study of of BGP Path Vector Route Looping Behavior&lt;/strong&gt;,&amp;quot; &lt;em&gt;24th International Conference On Distributed Computing Systems (ICDCS)&lt;/em&gt;, March  2004. "><img src="/images/extensions/bib.png" /></a>

     Dan Pei, Xiaoliang Zhao, Dan Massey, and Lixia Zhang, <br/><strong>&quot;A Study of of BGP Path Vector Route Looping Behavior</strong>,&quot; <br/><em>24th International Conference On Distributed Computing Systems (ICDCS)</em>, March  2004.

        <a target="_blank" href="/data/files/papers/massey_icdcs04.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=116" title="Mohit Lad, Akash Nanavati, Dan Massey, and Lixia Zhang, &lt;strong&gt;&amp;quot;An Algorithmic Approach to Identifying Link Failures&lt;/strong&gt;,&amp;quot; &lt;em&gt;Proceedings of the 10th Pacific Rim International Symposium on Dependable Computing (PRDC)&lt;/em&gt;, March  2004. "><img src="/images/extensions/bib.png" /></a>

     Mohit Lad, Akash Nanavati, Dan Massey, and Lixia Zhang, <br/><strong>&quot;An Algorithmic Approach to Identifying Link Failures</strong>,&quot; <br/><em>Proceedings of the 10th Pacific Rim International Symposium on Dependable Computing (PRDC)</em>, March  2004.

        <a target="_blank" href="/papers/LRFault.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=117" title="Hao Yang, Haiyun Luo, Fan Ye, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;Security in Mobile Ad-Hoc Wireless Networks: Challenges and Solutions&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE Wireless Communication, Vol. 11, No. 1, pp. 38-47&lt;/em&gt;, February  2004. "><img src="/images/extensions/bib.png" /></a>

     Hao Yang, Haiyun Luo, Fan Ye, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;Security in Mobile Ad-Hoc Wireless Networks: Challenges and Solutions</strong>,&quot; <br/><em>IEEE Wireless Communication, Vol. 11, No. 1, pp. 38-47</em>, February  2004.

        <a target="_blank" href="/papers/WIRELESSCOMM04.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=118" title="Ke Zhang, Felix Wu, Amy Yen, Zhao, Massey, and Zhang, &lt;strong&gt;&amp;quot;On Detection of Anomalous Routing Dynamics in BGP&lt;/strong&gt;,&amp;quot; &lt;em&gt;Networking&lt;/em&gt;, January  2004. "><img src="/images/extensions/bib.png" /></a>

     Ke Zhang, Felix Wu, Amy Yen, Zhao, Massey, and Zhang, <br/><strong>&quot;On Detection of Anomalous Routing Dynamics in BGP</strong>,&quot; <br/><em>Networking</em>, January  2004.

        <a target="_blank" href="/papers/networking04.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>

</ul><h3>2003</h3>
<ul>


<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=119" title="Dan Pei, Dan Massey, and Lixia Zhang, &lt;strong&gt;&amp;quot;Detection of Invalid Routing Announcements in the RIP Protocol&lt;/strong&gt;,&amp;quot; &lt;em&gt;GLOBECOM&lt;/em&gt;, December  2003. "><img src="/images/extensions/bib.png" /></a>

     Dan Pei, Dan Massey, and Lixia Zhang, <br/><strong>&quot;Detection of Invalid Routing Announcements in the RIP Protocol</strong>,&quot; <br/><em>GLOBECOM</em>, December  2003.

        <a target="_blank" href="/papers/dan_detection_globalcom03.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=120" title="Mohit Lad, Xiaoliang Zhao, Beichuan Zhang, Dan Massey, and Lixia Zhang, &lt;strong&gt;&amp;quot;Analysis of BGP Update Burst during Slammer Attack&lt;/strong&gt;,&amp;quot; in &lt;em&gt;Proceedings of the 5th International Workshop on Distributed Computing&lt;/em&gt;, December  2003. "><img src="/images/extensions/bib.png" /></a>

     Mohit Lad, Xiaoliang Zhao, Beichuan Zhang, Dan Massey, and Lixia Zhang, <br/><strong>&quot;Analysis of BGP Update Burst during Slammer Attack</strong>,&quot; <br/>in <em>Proceedings of the 5th International Workshop on Distributed Computing</em>, December  2003.

        <a target="_blank" href="/papers/mohit_iwdc03.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=121" title="Fan Ye, Haiyun Luo, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;Poster Abstract: Statistical En-route Filtering of Injected False Data In Sensor Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;ACM SenSys&lt;/em&gt;, November  2003. "><img src="/images/extensions/bib.png" /></a>

     Fan Ye, Haiyun Luo, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;Poster Abstract: Statistical En-route Filtering of Injected False Data In Sensor Networks</strong>,&quot; <br/><em>ACM SenSys</em>, November  2003.

        <a target="_blank" href="/papers/fan_statistical_sensys03.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=123" title="Soon-Tee Teoh, Kwan-Liu Ma, Felix S. Wu, Dan Massey, Xiao-Liang Zhao, Dan Pei, Lan Wang, Lixia Zhang, and Randy Bush, &lt;strong&gt;&amp;quot;Visual-based Anomaly Detection for BGP Origin AS Change (OASC) Events&lt;/strong&gt;,&amp;quot; &lt;em&gt;DSOM&lt;/em&gt;, October  2003. "><img src="/images/extensions/bib.png" /></a>

     Soon-Tee Teoh, Kwan-Liu Ma, Felix S. Wu, Dan Massey, Xiao-Liang Zhao, Dan Pei, Lan Wang, Lixia Zhang, and Randy Bush, <br/><strong>&quot;Visual-based Anomaly Detection for BGP Origin AS Change (OASC) Events</strong>,&quot; <br/><em>DSOM</em>, October  2003.

        <a target="_blank" href="/papers/soontee-visual-dsom03.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=124" title="Xiaoliang Zhao, Dan Massey, Dan Pei, and Lixia Zhang, &lt;strong&gt;&amp;quot;A Study on the Routing Convergence of Latin American Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;SIGCOMM Latin America Networking Workshop&lt;/em&gt;, August  2003. "><img src="/images/extensions/bib.png" /></a>

     Xiaoliang Zhao, Dan Massey, Dan Pei, and Lixia Zhang, <br/><strong>&quot;A Study on the Routing Convergence of Latin American Networks</strong>,&quot; <br/><em>SIGCOMM Latin America Networking Workshop</em>, August  2003.

        <a target="_blank" href="/papers/xiaoliang_study_lanc03.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=125" title="Dan Pei, Lan Wang, Daniel Massey, Felix S. Wu, and Lixia Zhang, &lt;strong&gt;&amp;quot;A Study of Packet Delivery Performance during Routing Convergence&lt;/strong&gt;,&amp;quot; &lt;em&gt;DSN&lt;/em&gt;, June  2003. "><img src="/images/extensions/bib.png" /></a>

     Dan Pei, Lan Wang, Daniel Massey, Felix S. Wu, and Lixia Zhang, <br/><strong>&quot;A Study of Packet Delivery Performance during Routing Convergence</strong>,&quot; <br/><em>DSN</em>, June  2003.

        <a target="_blank" href="/papers/peid_packet_dsn03.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=126" title="Yixin Jin, Beichuan Zhang, Vasileios Pappas, Sugih Jamin, and Lixia Zhang, &lt;strong&gt;&amp;quot;DIP: A Scalable Soft-State Protocol for Large Scale Data Dissemination in IDMaps System&lt;/strong&gt;,&amp;quot; &lt;em&gt;The Eighth IEEE Symposiums on Computers and Communications (ISCC)&lt;/em&gt;, June  2003. "><img src="/images/extensions/bib.png" /></a>

     Yixin Jin, Beichuan Zhang, Vasileios Pappas, Sugih Jamin, and Lixia Zhang, <br/><strong>&quot;DIP: A Scalable Soft-State Protocol for Large Scale Data Dissemination in IDMaps System</strong>,&quot; <br/><em>The Eighth IEEE Symposiums on Computers and Communications (ISCC)</em>, June  2003.

        <a target="_blank" href="/papers/yixin_dip_iscc03.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=127" title="Fan Ye, Gary Zhong, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;PEAS: A Robust Energy Conserving Protocol for Long-lived Sensor  Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;23rd International Conference on Distributed Computing Systems (ICDCS)&lt;/em&gt;, May  2003. "><img src="/images/extensions/bib.png" /></a>

     Fan Ye, Gary Zhong, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;PEAS: A Robust Energy Conserving Protocol for Long-lived Sensor  Networks</strong>,&quot; <br/><em>23rd International Conference on Distributed Computing Systems (ICDCS)</em>, May  2003.

        <a target="_blank" href="/papers/ye-peas-icdcs03.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=128" title="Lan Wang, Xiaoliang Zhao, Dan Pei, Randy Bush, Dan Massey, Allison Mankin, Felix S. Wu, and Lixia Zhang, &lt;strong&gt;&amp;quot;Protecting BGP Routes to Top Level DNS Servers&lt;/strong&gt;,&amp;quot; &lt;em&gt;3rd International Conference on Distributed Computing Systems (ICDCS)&lt;/em&gt;, May  2003. "><img src="/images/extensions/bib.png" /></a>

     Lan Wang, Xiaoliang Zhao, Dan Pei, Randy Bush, Dan Massey, Allison Mankin, Felix S. Wu, and Lixia Zhang, <br/><strong>&quot;Protecting BGP Routes to Top Level DNS Servers</strong>,&quot; <br/><em>3rd International Conference on Distributed Computing Systems (ICDCS)</em>, May  2003.

        <a target="_blank" href="/papers/lanw-dns-filter-ICDCS-2003.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=129" title="Fan Ye, Gary Zhong, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;A Robust Data Delivery Protocol for Large Scale Sensor Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;The 2nd International Workshop on Information Processing in Sensor Networks (IPSN)&lt;/em&gt;, April  2003. "><img src="/images/extensions/bib.png" /></a>

     Fan Ye, Gary Zhong, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;A Robust Data Delivery Protocol for Large Scale Sensor Networks</strong>,&quot; <br/><em>The 2nd International Workshop on Information Processing in Sensor Networks (IPSN)</em>, April  2003.

        <a target="_blank" href="/papers/ye-ipsn-03.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=130" title="Zhiguo Xu, Xiaoqiao Meng, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;Impact of IPv4 Address Allocation Practise on BGP Routing Table Growth&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE Computer Communication Workshop&lt;/em&gt;, March  2003. "><img src="/images/extensions/bib.png" /></a>

     Zhiguo Xu, Xiaoqiao Meng, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;Impact of IPv4 Address Allocation Practise on BGP Routing Table Growth</strong>,&quot; <br/><em>IEEE Computer Communication Workshop</em>, March  2003.

        <a target="_blank" href="/papers/zhiguo_impact_ccw03.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=131" title="Haiyun Luo, Fan Ye, Jerry Cheng, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;A Two-tier Data Dissemination Model for Large-scale Wireless Sensor Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;ACM MONET&lt;/em&gt;, March  2003. "><img src="/images/extensions/bib.png" /></a>

     Haiyun Luo, Fan Ye, Jerry Cheng, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;A Two-tier Data Dissemination Model for Large-scale Wireless Sensor Networks</strong>,&quot; <br/><em>ACM MONET</em>, March  2003.

        <a target="_blank" href="/papers/ttdd-monet03.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=132" title="Zhenghua Fu, Petros Zerfos, Haiyun Luo, Songwu Lu, Lixia Zhang, and Mario Gerla`, &lt;strong&gt;&amp;quot;The Impact of Multihop Wireless Channel on TCP Throughput and Loss&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE INFOCOM&lt;/em&gt;, March  2003. "><img src="/images/extensions/bib.png" /></a>

     Zhenghua Fu, Petros Zerfos, Haiyun Luo, Songwu Lu, Lixia Zhang, and Mario Gerla`, <br/><strong>&quot;The Impact of Multihop Wireless Channel on TCP Throughput and Loss</strong>,&quot; <br/><em>IEEE INFOCOM</em>, March  2003.

        <a target="_blank" href="http://www.cs.ucla.edu/wing/pdfdocs/infocom03.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=133" title="Xiaoliang Zhao, Dan Massey, Felix S. Wu, Mohit Lad, Dan Pei, Lan Wang, and Lixia Zhang, &lt;strong&gt;&amp;quot;Understanding BGP behavior through a study of DoD prefixes&lt;/strong&gt;,&amp;quot; &lt;em&gt;DISCEX&lt;/em&gt;, February  2003. "><img src="/images/extensions/bib.png" /></a>

     Xiaoliang Zhao, Dan Massey, Felix S. Wu, Mohit Lad, Dan Pei, Lan Wang, and Lixia Zhang, <br/><strong>&quot;Understanding BGP behavior through a study of DoD prefixes</strong>,&quot; <br/><em>DISCEX</em>, February  2003.

        <a target="_blank" href="/papers/fniisc_discex03.ps"><img src="/images/extensions/ps.png"></a>

    </li>

</ul><h3>2002</h3>
<ul>


<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=134" title="Fan Ye, Gary Zhong, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;PEAS: A Robust Energy Conserving Protocol for Long-lived Sensor Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;a poster in the 10 th IEEE Internation Conference on Network Protocols (ICNP)&lt;/em&gt;, November  2002. "><img src="/images/extensions/bib.png" /></a>

     Fan Ye, Gary Zhong, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;PEAS: A Robust Energy Conserving Protocol for Long-lived Sensor Networks</strong>,&quot; <br/><em>a poster in the 10 th IEEE Internation Conference on Network Protocols (ICNP)</em>, November  2002.

        <a target="_blank" href="http://www.cs.ucla.edu/%7Eyefan/02icnp-poster.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=135" title="Lan Wang, Xiaoliang Zhao, Dan Pei, Randy Bush, Dan Massey, Allison Mankin, Felix S. Wu, and Lixia Zhang, &lt;strong&gt;&amp;quot;Observation and Analysis of BGP Behavior under Stress&lt;/strong&gt;,&amp;quot; &lt;em&gt;SIGCOMM Internet Measurement Workshop&lt;/em&gt;, November  2002. "><img src="/images/extensions/bib.png" /></a>

     Lan Wang, Xiaoliang Zhao, Dan Pei, Randy Bush, Dan Massey, Allison Mankin, Felix S. Wu, and Lixia Zhang, <br/><strong>&quot;Observation and Analysis of BGP Behavior under Stress</strong>,&quot; <br/><em>SIGCOMM Internet Measurement Workshop</em>, November  2002.

        <a target="_blank" href="/papers/lanw-imw02-bgp.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=136" title="Wenjie Wang, David Helder, Sugih Jamin, , and Lixia Zhang, &lt;strong&gt;&amp;quot;Overlay Optimizations for End-host Multicast&lt;/strong&gt;,&amp;quot; &lt;em&gt;Fourth International Workshop on Networked Group Communication (NGC)&lt;/em&gt;, October  2002. "><img src="/images/extensions/bib.png" /></a>

     Wenjie Wang, David Helder, Sugih Jamin, , and Lixia Zhang, <br/><strong>&quot;Overlay Optimizations for End-host Multicast</strong>,&quot; <br/><em>Fourth International Workshop on Networked Group Communication (NGC)</em>, October  2002.

        <a target="_blank" href="/data/files/papers/tmesh_ngc02.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=137" title="Beichuan Zhang, Sugih Jamin, and Lixia Zhang, &lt;strong&gt;&amp;quot;Universal IP Multicast Delivery&lt;/strong&gt;,&amp;quot; &lt;em&gt;Proceedings of Fourth International Workshop on Networked Group Communication (NGC)&lt;/em&gt;, October  2002. "><img src="/images/extensions/bib.png" /></a>

     Beichuan Zhang, Sugih Jamin, and Lixia Zhang, <br/><strong>&quot;Universal IP Multicast Delivery</strong>,&quot; <br/><em>Proceedings of Fourth International Workshop on Networked Group Communication (NGC)</em>, October  2002.

        <a target="_blank" href="/papers/um_ngc02.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=138" title="Fan Ye, Haiyun Luo, Jerry Cheng, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;A Two-tier Data Dissemination Model for Large-scale Wireless Sensor Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;MobiCom&lt;/em&gt;, September  2002. "><img src="/images/extensions/bib.png" /></a>

     Fan Ye, Haiyun Luo, Jerry Cheng, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;A Two-tier Data Dissemination Model for Large-scale Wireless Sensor Networks</strong>,&quot; <br/><em>MobiCom</em>, September  2002.

        <a target="_blank" href="/papers/ye-mobicom02.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=139" title="Haiyun Luo, Jiejun Kong, Petros Zerfos, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;Self-securing Ad Hoc Wireless Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE ISCC (IEEE Symposium on Computers and Communications)&lt;/em&gt;, July  2002. "><img src="/images/extensions/bib.png" /></a>

     Haiyun Luo, Jiejun Kong, Petros Zerfos, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;Self-securing Ad Hoc Wireless Networks</strong>,&quot; <br/><em>IEEE ISCC (IEEE Symposium on Computers and Communications)</em>, July  2002.

        <a target="_blank" href="http://www.cs.ucla.edu/~lixia/papers/02ISCC.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=140" title="Beichuan Zhang, Sugih Jamin, and L. Zhang, &lt;strong&gt;&amp;quot;Host Multicast: A Framework for Delivering Multicast to End Users&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE INFOCOM&lt;/em&gt;, June  2002. "><img src="/images/extensions/bib.png" /></a>

     Beichuan Zhang, Sugih Jamin, and L. Zhang, <br/><strong>&quot;Host Multicast: A Framework for Delivering Multicast to End Users</strong>,&quot; <br/><em>IEEE INFOCOM</em>, June  2002.

        <a target="_blank" href="/papers/hmcast_infocom02.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=141" title="D. Pei, X. Zhao, L. Wang, D. Massey, A. Mankin, S. F. Wu, , and L. Zhang, &lt;strong&gt;&amp;quot;Improving BGP Convergence Through Consistency Assertions&lt;/strong&gt;,&amp;quot; &lt;em&gt;IEEE INFOCOM&lt;/em&gt;, June  2002. "><img src="/images/extensions/bib.png" /></a>

     D. Pei, X. Zhao, L. Wang, D. Massey, A. Mankin, S. F. Wu, , and L. Zhang, <br/><strong>&quot;Improving BGP Convergence Through Consistency Assertions</strong>,&quot; <br/><em>IEEE INFOCOM</em>, June  2002.

        <a target="_blank" href="/papers/dan_infocom2002.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=142" title="Jun Li, Jelena Mirkovic, Mengqiu Wang, Peter Reiher, and Lixia Zhang, &lt;strong&gt;&amp;quot;SAVE: Source Address Validity Enforcement Protocol&lt;/strong&gt;,&amp;quot; &lt;em&gt;INFOCOM&lt;/em&gt;, June  2002. "><img src="/images/extensions/bib.png" /></a>

     Jun Li, Jelena Mirkovic, Mengqiu Wang, Peter Reiher, and Lixia Zhang, <br/><strong>&quot;SAVE: Source Address Validity Enforcement Protocol</strong>,&quot; <br/><em>INFOCOM</em>, June  2002.

        <a target="_blank" href="/papers/save_infocom.pdf"><img src="/images/extensions/pdf.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=143" title="Xiaoliang Zhao, Dan Pei, Lan Wang, Dan Massey, Allison Mankin, Felix S. Wu, and Lixia Zhang, &lt;strong&gt;&amp;quot;Detection of Invalid Routing Announcement in the Internet&lt;/strong&gt;,&amp;quot; &lt;em&gt;Proceedings of International Conference on Dependable Systems &amp;amp; Networks (DSN)&lt;/em&gt;, June  2002. "><img src="/images/extensions/bib.png" /></a>

     Xiaoliang Zhao, Dan Pei, Lan Wang, Dan Massey, Allison Mankin, Felix S. Wu, and Lixia Zhang, <br/><strong>&quot;Detection of Invalid Routing Announcement in the Internet</strong>,&quot; <br/><em>Proceedings of International Conference on Dependable Systems &amp; Networks (DSN)</em>, June  2002.

        <a target="_blank" href="/papers/fniisc_dsn02.ps"><img src="/images/extensions/ps.png"></a>

    </li>



<li style="margin-top:14px">
    <a class="smoothbox_small" href="/bibwiki/bibtex?id=144" title="Jelena Mirkovic, Songwu Lu, and Lixia Zhang, &lt;strong&gt;&amp;quot;A Self-Organizing Approach to Data Forwarding in Wireless Sensor Networks&lt;/strong&gt;,&amp;quot; &lt;em&gt;ICC&lt;/em&gt;, June  2002. "><img src="/images/extensions/bib.png" /></a>

     Jelena Mirkovic, Songwu Lu, and Lixia Zhang, <br/><strong>&quot;A Self-Organizing Approach to Data Forwarding in Wireless Sensor Networks</strong>,&quot; <br/><em>ICC</em>, June  2002.

        <a target="_blank" href="/papers/icc2001-jelena.ps"><img src="/images/extensions/ps.png"></a>

    </li>

</ul><h3>2001</h3>
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
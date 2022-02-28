## Disruption-Tolerant Networking Implementations of the Bundle Protocol 7

In disruption-tolerant networking (DTN), data is transmitted in a store-carry-forward fashion from network node to network node.
Other places also refer to the name delay-tolerant networking, which is the same in this context.

We are presenting free and open source DTN implementations of the recently released Bundle Protocol Version 7 [(RFC 9171)][RFC9171].

[DTN7-go][dtn7-go] is written in Go and provides features like memory safety and concurrent execution.
With its modular design and interchangeable components, DTN7-go facilitates DTN research and application development.
Furthermore, we did an experimental evaluation of DTN7-go and other DTN systems including Serval, IBR-DTN, and Forban.
Our results indicate that DTN7 is a flexible and efficient open-source multi-platform implementation of the most recent Bundle Protocol Version 7.

[DTN7-rs][dtn7-rs] is written in Rust and provides an implementation focused on speed, safety, and flexibility.
Due to its modular design, the actual bundle encoding can be used standalone if needed without the actual dtn7 bundle agent.
A conducted evaluation shows that the Rust implementation and WebAssembly as a platform provide enough performance for even higher bundle workloads, while at the same time leaving only a minimal memory/storage footprint.
Furthermore, different storage backends, routing, and convergence layer agents exist in the dtn7 daemon for various use-cases.

[DTN7-kotlin][dtn7-kotlin] is written in Kotlin, well unit-tested and compatible with DTN7-go's bpv7 suite.
It implements the Bundle Protocol Security Specification.

[dtn7-go]:https://github.com/dtn7/dtn7-go
[dtn7-kotlin]:https://github.com/NodleCode/dtn7-kotlin/
[dtn7-rs]:https://github.com/dtn7/dtn7-rs
[RFC9171]:https://datatracker.ietf.org/doc/rfc9171/
[RFC9172]:https://datatracker.ietf.org/doc/rfc9172/
[RFC9173]:https://datatracker.ietf.org/doc/rfc9173/
[RFC9174]:https://datatracker.ietf.org/doc/rfc9174/


## News

### Happy Birthday Bundle Protocol Version 7!
##### 2022 Feb 1

The waiting is over!
The bundle protocol version 7 draft finally turned into [RFC 9171][RFC9171] together with [BPSec][RFC9172], [security contexts for BPSec][RFC9173] and [TCP CL][RFC9174]. 

<!-- Force another paragraph for more space between the news items. -->
&nbsp;

[awesome-dtn]:https://github.com/dtn7/awesome-dtn


### Awesome DTN
##### 2021 Mar 2

We started an [awesome DTN][awesome-dtn] list with links to different DTN and bundle protocol implementations plus various video resources, etc.

<!-- Force another paragraph for more space between the news items. -->
&nbsp;

[awesome-dtn]:https://github.com/dtn7/awesome-dtn


### DTNs Explained
##### 2020 May 12

<style>
    .embed-container {
        position: relative;
        padding-bottom: 56.25%;
        height: 0;
        overflow: hidden;
        max-width: 100%;
    }
    .embed-container iframe, .embed-container object, .embed-container embed {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
    }
</style>

<div class='embed-container'>
  <iframe
    src='https://www.youtube-nocookie.com/embed/BGQD1UN_q_g'
    frameborder='0'
    allowfullscreen>
  </iframe>
</div>

<!-- Force another paragraph for more space between the news items. -->
&nbsp;

### DTN7-kotlin: A new Implementation
##### 2021 Feb 22

We are very pleased to announce that there is a new DTN implementation which also follows the DTN7 naming scheme, [DTN7-kotlin][dtn7-kotlin].
This implementation from Lucien Loiseau, Nodle.io, is well unit-tested and compatible with DTN7-go's bpv7 suite.
It also implements the Bundle Protocol Security Specification [(draft 26)][ietf-dtn-bpsec-26].


### Getting Started with dtn7-rs
##### 2020 Dec 1

We prepared a [getting-started][getting-started-dtn7-rs] documet for [dtn7-rs][dtn7-rs] that describes how to use and setup dtn7 in combination with the [core network emulator][coreemu]. 
The steps are also avaibable as a video demonstration.

<style>
    .embed-container {
        position: relative;
        padding-bottom: 56.25%;
        height: 0;
        overflow: hidden;
        max-width: 100%;
    }
    .embed-container iframe, .embed-container object, .embed-container embed {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
    }
</style>

<div class='embed-container'>
  <iframe
    src='https://www.youtube-nocookie.com/embed/7xwJEZyL_Ns'
    frameborder='0'
    allowfullscreen>
  </iframe>
</div>

<!-- Force another paragraph for more space between the news items. -->
&nbsp;

[getting-started-dtn7-rs]:https://github.com/dtn7/dtn7-rs/blob/master/doc/getting-started.md
[coreemu]:https://github.com/coreemu/core


### GHTC 2020 Conference
##### 2020 Oct 31

We presented a simple short messaging system based upon [dtn7-rs][dtn7-rs] including an evaluation of different compression algorithms at [GHTC 2020][ghtc-2020].
The main focus of this research was on making the most of the limited resources available with LoRa networks.
A preprint of the paper [is available here][ghtc-2020-preprint].

```bibtex
@inproceedings{baumgaertner2020loragent,
  author = {Baumgärtner, Lars and Lieser, Patrick and Zobel, Julian and Bastian, Bloessl and Steinmetz, Ralf and Mezini, Mira},
  title = {LoRAgent: A DTN-based Location-aware Communication System using LoRa},
  booktitle = {IEEE Global Humanitarian Technology Conference (GHTC 2020)},
  address = {Seattle, Washington, USA},
  month = oct,
  year = {2020},
  keywords = {LoRa, Disaster Communication, Messaging},
  organization={IEEE},
}
```

[ghtc-2020]:https://ieeeghtc.org/archives/ghtc-2020/
[ghtc-2020-preprint]:https://www.bastibl.net/bib/baumgaertner2020loragent/baumgaertner2020loragent.pdf


### Bundle Protocol Version 7, Draft 25
##### 2020 May 22

In the recently published Bundle Protocol Version 7 [draft version 25][ietf-dtn-bpbis-25] our two implementations were mentioned.
The _Implementation Status_ section shows known implementations.
This list now also includes [DTN7-go][dtn7-go] and [DTN7-rs][dtn7-rs].

[ietf-dtn-bpbis-25]:https://tools.ietf.org/html/draft-ietf-dtn-bpbis-25


### ISCRAM 2020 Conference
##### 2020 Feb 14

Our paper presenting an approach to facilitate long-range device-to-device communication via smartphones in crisis scenarios got accepted at [ISCRAM 2020][iscram-2020].
An integration of LoRa into DTN7 was presented and evaluated in the paper.
A preprint of the paper [is available here][iscram-2020-preprint], the experiment fragments are available in the respective [GitHub repository][iscram-2020-experiment].

Due to the COVID19-pandemic, the ISCRAM 2020 conference unfortunately did not take place.
Therefore Artur Sterz will probably present our paper next year.


```bibtex
@inproceedings{hoechst2020lora,
  author = {Höchst, Jonas and Baumgärtner, Lars and Kuntke, Franz and Penning, Alvar and Sterz, Artur and Freisleben, Bernd},
  title = {LoRa-based Device-to-Device Smartphone Communication for Crisis Scenarios},
  booktitle = {17th International Conference on Information Systems for Crisis Response and Management (ISCRAM 2020)},
  address = {Blacksburg, Virginia, USA},
  month = may,
  year = {2020},
  keywords = {LoRa, Disaster Communication, Device-To-Device Communication},
}
```

[iscram-2020]:https://www.drrm.fralin.vt.edu/iscram2020/index.php
[iscram-2020-preprint]:{{ site.baseurl }}{% link assets/hoechst2020lora.pdf %}
[iscram-2020-experiment]:https://github.com/umr-ds/hoechst2020lora


### 36th Chaos Communication Congress
##### 2019 Dec 28

Alvar Penning presented a [Lightning Talk at 36c3][36c3-lt] in Leipzig, Germany.
The talk is available both at [media.ccc.de][36c3-lt-media-ccc] and [YouTube][36c3-lt-youtube], the [slides are available online][36c3-lt-slides].

<style>
    .embed-container {
        position: relative;
        padding-bottom: 56.25%;
        height: 0;
        overflow: hidden;
        max-width: 100%;
    }
    .embed-container iframe, .embed-container object, .embed-container embed {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
    }
</style>

<div class='embed-container'>
  <iframe
    src='https://www.youtube-nocookie.com/embed/ZdnXO56QR7g?start=3780'
    frameborder='0'
    allowfullscreen>
  </iframe>
</div>

<!-- Force another paragraph for more space between the news items. -->
&nbsp;

[36c3-lt]:https://events.ccc.de/congress/2019/wiki/index.php/Static:Lightning_Talks
[36c3-lt-media-ccc]:https://media.ccc.de/v/36c3-10524-lightning_talks_day_2
[36c3-lt-youtube]:https://youtu.be/ZdnXO56QR7g?t=3780
[36c3-lt-slides]:{{ site.baseurl }}{% link assets/36c3lt.pdf %}


### ICT-DM 2019 Conference
##### 2019 Dec 18

We presented a paper on browser-based DTN at the [ICT-DM 2019 conference][ict-dm-2019] in Paris at 18th to 20th of December 2019.
Lars Baumgärtner gave his talk in the the 2nd plenary session "Wireless communications for disaster management" December 18th at 4:20 pm.
The [research paper][ict-dm-2019-paper] and the [slides of the talk][ict-dm-2019-slides] are available online.

```bibtex
@inproceedings{baumgaertner2019bdtn7,
  title={B-DTN7: Browser-based Disruption-tolerant Networking via Bundle Protocol 7},
  author={Baumgärtner, Lars and Höchst, Jonas and Meuser, Tobias},
  booktitle={International Conference on Information and Communication Technologies for Disaster Management (ICT-DM'19)},
  address={Paris, France},
  year={2019},
  keywords={DTN; WASM; Emergency Communication},
  organization={IEEE},
}
```

[ict-dm-2019]:https://ict-dm2019.esiee.fr
[ict-dm-2019-paper]:{{ site.baseurl }}{% link assets/baumgaertner2019bdtn7.pdf %}
[ict-dm-2019-slides]:{{ site.baseurl }}{% link assets/baumgaertner2019bdtn7-slides.pdf %}


### AdHoc-Now 2019 Conference
##### 2019 Oct 01

We presented our initial paper on the [AdHoc-Now 2019 conference][adhoc-now-2019] in Luxembourg at 1st to 3rd October 2019.
The talk by Alvar Penning took place in the 3rd technical session "Routing Strategies for WSN".
Download and read the [research paper][adhoc-now-2019-paper].
Download the [slides of the talk][adhoc-now-2019-slides].

```bibtex
@inproceedings{penning2019dtn7,
  title={DTN7: An Open-Source Disruption-tolerant Networking Implementation of Bundle Protocol 7},
  author={Penning, Alvar and Baumgärtner, Lars and Höchst, Jonas and Sterz, Artur and Mezini, Mira and Freisleben, Bernd},
  booktitle={International Conference on Ad-Hoc Networks and Wireless (AdHoc-Now 2019)},
  address={Luxembourg, Luxembourg},
  pages={196--209},
  year={2019},
  organization={Springer},
}
```

[adhoc-now-2019]:https://www.adhocnow2019.lu/programme/programme/
[adhoc-now-2019-paper]:{{ site.baseurl }}{% link assets/penning2019dtn.pdf %}
[adhoc-now-2019-slides]:{{ site.baseurl }}{% link assets/penning2019dtn-slides.pdf %}


<!-- vim: set ts=2 ft=markdown spell: -->

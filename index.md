## Disruption-Tolerant Networking Implementations of Bundle Protocol 7

In disruption-tolerant networking (DTN), data is transmitted in a
store-carry-forward fashion from network node to network node.  We are
presenting two free and open source DTN implementations of the recently released
Bundle Protocol Version 7 [(draft version 23)][ietf-dtn-bpbis-23].

__DTN7-go__ is written in Go and provides features like memory safety and
concurrent execution. With its modular design and interchangeable components,
DTN7-go facilitates DTN research and application development. Furthermore, we
did an experimental evaluation of DTN7-go and other DTN systems including
Serval, IBR-DTN, and Forban. Our results indicate that DTN7 is a flexible and
efficient open-source multi-platform implementation of the most recent Bundle
Protocol Version 7.

__DTN7-rs__ is written in Rust and provides an implementation focused on speed.
With the rust compiler working with the LLVM backend, it can be compiled for a
huge amount of platforms, including WebAssembly to be executed in a browser. A
conducted evaluation shows, that the Rust implementation and WebAssembly as a
platform provides enough performance for even higher bundle workloads, while at
the same time leaving only a minimal memory/storage footprint.


### Free and Open Source

- DTN7-go is available online in the [corresponding GitHub repository][dtn7-go]
  under the [GNU General Public License v3.0][dtn7-go-gpl3].
- DTN7-rs is also [available online][dtn7-rs] and licensed under either of
  [Apache License, Version 2.0][dtn7-rs-apl2] or [MIT license][dtn7-rs-mit] at
  your option.

Questions, comments and pull requests are very welcome.

## Usage

### DTN7-go

Installation is as easy as:

```bash
git clone https://github.com/dtn7/dtn7-go.git
cd dtn7-go
go build ./cmd/dtnd
```

Check out the detailed installation guide and some examples to [using
DTN7-go][dtn7-go-installation].


### DTN7-rs

Installation is as easy as:

```bash
cargo install dtn7
```

Check out more information about [using DTN7-rs][dtn7-rs].


[dtn7-go]:https://github.com/dtn7/dtn7-go
[dtn7-go-installation]:https://github.com/dtn7/dtn7-go#installation
[dtn7-go-gpl3]:https://github.com/dtn7/dtn7-go/blob/master/LICENSE
[dtn7-rs]:https://github.com/dtn7/dtn7-rs
[dtn7-rs-apl2]:https://github.com/dtn7/dtn7-rs/blob/master/LICENSE-APACHE
[dtn7-rs-mit]:https://github.com/dtn7/dtn7-rs/blob/master/LICENSE-MIT
[ietf-dtn-bpbis-23]:https://tools.ietf.org/html/draft-ietf-dtn-bpbis-23


## News

### ISCRAM 2020 Conference
##### 2020 Feb 14

Our paper presenting an approach to facilitate long-range device-to-device
communication via smartphones in crisis scenarios got accepted at [ISCRAM
2020][iscram-2020]. An integration of LoRa into DTN7 was presented and evaluated
in the paper. A preprint of the paper [is available here][iscram-2020-preprint],
the experiment fragments are available in the respective
[GitHub repository][iscram-2020-experiment].

Due to the COVID19-pandemic, the ISCRAM 2020 conference unfortunately did not
take place. Therefore Artur Sterz will probably present our paper next year.


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
The talk is available both at [media.ccc.de][36c3-lt-media-ccc] and
[YouTube][36c3-lt-youtube], the [slides are available online][36c3-lt-slides].

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

We presented a paper on browser-based DTN at the [ICT-DM 2019
conference][ict-dm-2019] in Paris at 18th to 20th of December 2019. Lars
Baumgärtner gave his talk in the the 2nd plenary session "Wireless
communications for disaster management" December 18th at 4:20 pm. The [research
paper][ict-dm-2019-paper] and the [slides of the talk][ict-dm-2019-slides] are
available online.

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

We presented our initial paper on the [AdHoc-Now 2019
conference][adhoc-now-2019] in Luxembourg at 1st to 3rd October 2019. The talk
by Alvar Penning took place in the 3rd technical session "Routing Strategies for
WSN". Download and read the [research paper][adhoc-now-2019-paper]. Download the
[slides of the talk][adhoc-now-2019-slides].

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


<!-- vim: set tw=80 ts=2 ft=markdown: -->

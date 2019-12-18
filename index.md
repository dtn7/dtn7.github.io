## An Open-Source Disruption-tolerant Networking Implementation of Bundle Protocol 7

In disruption-tolerant networking (DTN), data is transmitted in a store-carry-forward fashion from network node to network node. In this work, we present an open source DTN implementation, called DTN7, of the recently released Bundle Protocol Version 7 (draft version 17). Currently there are two implementations maintained in our project

**DTN7-go** is written in Go and provides features like memory safety and concurrent execution. With its modular design and interchangeable components, DTN7 facilitates DTN research and application development. 
Furthermore, we did an experimental evaluation of DTN7 and other DTN systems including Serval, IBR-DTN, and Forban. Our results indicate that DTN7 is a flexible and efficient open-source multi-platform implementation of the most recent Bundle Protocol Version 7.

**DTN7-rs** is written in Rust and provides an implementation focused on speed. With the rust compiler working with the LLVM backend, it can be compiled for a huge amount of platforms, including WebAssembly to be executed in a browser.
A conducted evaluation shows, that the Rust implementation and WebAssembly as a platform provides enough performance for even higher bundle workloads, while at the same time leaving only a minimal memory/storage footprint. 

### Free and Open Source

DTN7-go is available online in the [corresponding GitHub repository](https://github.com/dtn7/dtn7-go) under the [GNU General Public License v3.0](https://github.com/dtn7/dtn7-go/blob/master/LICENSE). DTN7-rs is also [available online](https://github.com/dtn7/dtn7-rs/) and
licensed under either of <a href="https://github.com/dtn7/dtn7-rs/blob/master/LICENSE-APACHE">Apache License, Version 2.0</a> or <a href="https://github.com/dtn7/dtn7-rs/blob/master/LICENSE-MIT">MIT license</a> at your option.

Questions, comments and pull requests are very welcome. 

## Usage

Installation is as easy as: 

```bash
git clone https://github.com/dtn7/dtn7-go.git
cd dtn7-go
go build ./cmd/dtnd
```

Check out the detailed installation guide and some examples to [using DTN7](https://github.com/dtn7/dtn7-go#installation).

## News

### ICT-DM 2019 Conference 
##### 2019 Dec 18

We are presenting a paper on browser-based DTN at the [ICT-DM 2019 conference](https://ict-dm2019.esiee.fr) in Paris at 18th to 20th of December 2019. Lars Baumgärtner will give his talk in the the 2nd plenary session "Wireless communications for disaster management" December 18th at 4:20 pm. The [research paper](assets/baumgaertner2019bdtn7.pdf) and the [slides of the talk](assets/baumgaertner2019bdtn7-slides.pdf) are available online.

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


### [DTN7-go v0.5.0](https://github.com/dtn7/dtn7-go/releases/tag/v0.5.0)
##### 2019 Nov 08
LoRa-based Convergency Layer and Bundle Protocol [dtn-bpbis-17](https://tools.ietf.org/html/draft-ietf-dtn-bpbis-17).


### [DTN7-go v0.4.0 released](https://github.com/dtn7/dtn7-go/releases/tag/v0.4.0)
##### 2019 Oct 11
This release implements the Delay-Tolerant Networking TCP Convergence Layer Protocol Version 4 for a bidirectional Bundle exchange.
Furthermore, the PRoPHET routing protocol was added.


### AdHoc-Now 2019 Conference 
##### 2019 Oct 01
We are presenting our initial paper on the [AdHoc-Now 2019 conference](https://www.adhocnow2019.lu/programme/programme/) in Luxembourg from 1st to 3rd October 2019. The talk by Alvar Penning takes place in the 3rd technical session "Routing Strategies for WSN". Download and read the [research paper](assets/penning2019dtn.pdf). Download the [slides of the talk](assets/penning2019dtn-slides.pdf).

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

### [DTN7-go v0.3.0: DTLSR, MTCP Keep Alive](https://github.com/dtn7/dtn7-go/releases/tag/v0.3.0)
##### 2019 Sep 06
This release features Delay-Tolerant Link State Routing (DTLSR) and a MTCP keep-alive mechanism to cope with link failures.


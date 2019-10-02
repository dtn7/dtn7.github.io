## An Open-Source Disruption-tolerant Networking Implementation of Bundle Protocol 7

In disruption-tolerant networking (DTN), data is transmitted in a store-carry-forward fashion from network node to network node. In this paper, we present an open source DTN implementation, called DTN7, of the recently released Bundle Protocol Version 7 (draft version 13). DTN7 is written in Go and provides features like memory safety and concurrent execution. With its modular design and interchangeable components, DTN7 facilitates DTN research and application development. Furthermore, we present results of a comparative experimental evaluation of DTN7 and other DTN systems including Serval, IBR-DTN, and Forban. Our results indicate that DTN7 is a flexible and efficient open-source multi-platform implementation of the most recent Bundle Protocol Version 7.


## Free and Open Source

Our implementation of Bundle Protocol Version 7 is available online in the [corresponding GitHub repository](https://github.com/dtn7/dtn7-go) under the [GNU General Public License v3.0](https://github.com/dtn7/dtn7-go/blob/master/LICENSE). Questions, comments and pull requests are very welcome. 

## Usage

Installation is as easy as: 

```bash
git clone https://github.com/dtn7/dtn7-go.git
cd dtn7-go
go build ./cmd/dtnd
```

Check out the detailed installation guide and some examples to [using DTN7](https://github.com/dtn7/dtn7-go#installation).

## News

### AdHoc-Now 2019 Conference 
##### 2019 Oct 01
We are presenting our initial paper on the [AdHoc-Now 2019 conference](https://www.adhocnow2019.lu/programme/programme/) in Luxembourg from 1st to 3rd October 2019. The talk by Alvar Penning takes place in the 3rd technical session "Routing Strategies for WSN". Download and read the research [paper](https://github.com/dtn7/adhocnow2019/releases/download/v1.0/penning2019dtn.pdf). Download the [slides of the talk](https://github.com/dtn7/adhocnow2019-slides/releases/download/v0.1.0/penning2019dtn-slides.pdf).

```bibtex
@inproceedings{penning2019dtn7,
  title={DTN7: An Open-Source Disruption-tolerant Networking Implementation of Bundle Protocol 7},
  author={Penning, Alvar and Baumg{\"a}rtner, Lars and H{\"o}chst, Jonas and Sterz, Artur and Mezini, Mira and Freisleben, Bernd},
  booktitle={International Conference on Ad-Hoc Networks and Wireless},
  pages={196--209},
  year={2019},
  organization={Springer}
}
```

### DTN7 v0.3.0 released
##### 2019 Sep 06
This release features Delay-Tolerant Link State Routing (DTLSR) and a MTCP keep-alive mechanism to cope with link failures.


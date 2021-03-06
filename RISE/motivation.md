# Routing in the Internet with Semantic Enhancements
## RISE Proposed Research Group
## Motivation : Revision 07 : 2021-11-02

Upper-layer applications are placing increasingly sophisticated demands on the network for better quality, more predictability, and increasing reliability. Some of these applications are futuristic predictions (for example, holographic conferencing), but many are rapidly developing sectors with established revenue streams (such as multiplayer immersive gaming).

At the same time, lower-layer network technologies are advancing rapidly providing increased bandwidth to the home and to mobile hand-held devices. These advances create an environment that enables the potential of advanced applications being run by very many end-users. This coincides with a growing trend to extend end-to-end communications to include machines and services, and to introduce routing and addressing behaviors and semantics specific to a particular use case and set of requirements applied within a limited region or domain of the Internet. Examples of these three developments include 5G, predicted wireless evolutions, IoT and vehicular connectivity, space-terrestrial communication, industrial networks, cloud computing, service function chaining and network functions virtualization, digital twins, and data-centric data brokerage platforms.

Despite this plurality of communication scenarios, IP-based addressing and network layer routing have remained focused on identifying locations of communication and determining paths between those locations. This has previously depended on higher-layer capabilities (e.g., for name-to-location resolution) to support those comprehensive communication scenarios, but that approach introduces latency and dependencies (e.g., changing locator assignments may depend on the capabilities of the upper-layer capability that are outside the core addressing and routing system). Furthermore, multi-layer lookups and interactions may impact the efficacy of communication scenarios, particularly those that employ different routing and addressing approaches beyond just locators.

The performance of routing functions based on addresses with enhanced semantics and other properties of packets is called ???semantic routing???. Semantic routing proposes to place the support for advanced routing and location functions directly at the packet routing layer, such as through extensions to the identification properties of addresses (what is being identified beyond just network locations) or through performing routing functions on an extended set of inputs (for example, other fields carried in packet headers). Such an approach would preserve the Internet architecture as it is today while enabling additional routing function. 

As with all advances in Internet protocols, semantic routing may be considered for Internet-wide deployment or may be restricted (possibly only initially) to well-defined and contained networks referred to as ???limited domains??? (see RFC 8799). Semantic enhancements may be opaque within the network (in other words, the additional information it carries is not visible by the routers), may be transparent (so that routers may see the information, but their processing does not need to be changed to accommodate the information or ites encoding), or may be actve (so that semantic routing is enabled). Semantic routing may select paths in one domain that are not consistent with the paths selected in other domains. In any case, a concern and consideration must be coexistence with, and backward compatibility to, existing routing and addressing schemes that are widely deployed.

A strategic objective of semantic routing and its associated semantic enhancements is to enable Service Providers to modify the default forwarding behaviour to be based on other information present in the packet and policy configured or dynamically programmed into the routers and devices. This is aimed to cause new and alternative path processing by routers, including:

* Determinism of quality of delivery in terms of throughput, latency, jitter, drop precedence. 
* Determinism of resilience in terms of survival of network failures and delivery degradation.
* Determinism of routing performance in terms of the volume of data that has to be exchanged both to establish and to maintain the routing tables.
* Deployability in terms of configuration, training, development of new hardware/software, and interaction with pre-existing network technologies and uses.
* Efficiency of manageability in terms of i. diagnostic management, ii. management of Service KPIs with/without guarantees, and iii. dynamic and controlled instantiation of management information in the packets."

Efforts to develop new approaches to routing have been ongoing within the IETF/IRTF and wider academia for some years (see draft-king-irtf-semantic-routing-survey for a partial list). The ICNRG has looked at extending the scope of routing to information retrieval scenarios and for distributed computing, and COINRG has discussed the need to incorporate in-network computational resources into the communications and associated addressing with the possible impact on network capabilities like routing and transport. Application constraints have been considered in a number of routing proposals (such as the APN BoF in the IETF). Although routing plays a role in those efforts, it is not the central focus.

Issues of security and privacy have been largely overlooked within the routing systems. However, there is increasing concern that attacks on routing systems can not only be disruptive (for example, causing traffic to be dropped), but may cause traffic to be routed via inspection points that can breach the security or privacy of the payloads. While semantic routing may offer tools for increasing security and privacy, it is possible that semantic routing and associated semantic enhancements may provide vectors for attacks or compromise privacy. This must form an element of any research into the topic.

There has been some background work to bring together ideas and researchers in the field of semantic routing. This has manifested through conferences, workshops, Internet-Drafts, and a mailing list.

* Workshops at academic conferences
    * 28th International Conference on Telecommunications
        * 1-3 June 2021
        * https://ict-21.org/
        * Special session ???Special Session 1: Re-thinking the Data & Forwarding Plane for 6G and More???
    * IEEE International Conference on High Performance Switching and Routing
        * 7-10 June, 2021
        * https://hpsr2021.ieee-hpsr.org/sarnet-21/
        * Workshop on ???Semantic Addressing and Routing for Future Network (SARNET-21)???
    * 29th IEEE International Conference on Network Protocols
        * November 1-5, 2021
        * https://nipaa21.wordpress.com/
        * 2nd Workshop on New Internetworking Protocols, Architecture and Algorithms
* Side meetings at the IETF
    * IETF-111 ???Routing Research Challenges Arising from Evolving Beyond and Revitalizing the Internet???
        * 28th July, 2021
        * https://github.com/danielkinguk/sarah/tree/main/IETF-111
    * Interim workshop on ???Evolving Routing Security in the Internet???
        * 30th September, 2021
        * https://github.com/danielkinguk/sarah/tree/main/conferences/security-workshop
    * IETF-112 ???Service Routing and Addressing???,
        * 10th November, 2021
        * https://github.com/danielkinguk/sarah/tree/main/conferences/ietf-112
* Mailing list
    * Semantic Address Routing and Hardware (SARAH) list,
        * https://www.jiscmail.ac.uk/cgi-bin/webadmin?A0=SARAH
* Internet-Drafts
    * ???An Introduction to Semantic Routing???
        * An overview of the concept of semantic routing
        * https://datatracker.ietf.org/doc/html/draft-farrel-irtf-introduction-to-semantic-routing/
    * ???Challenges for the Internet Routing Infrastructure Introduced by Changes in Address Semantics??? 
        * Presents a set of research questions and issues to be considered when considering semantic routing and assocuated semantic enhancements.
        * https://datatracker.ietf.org/doc/html/draft-king-irtf-challenges-in-routing/
    * ???A Survey of Semantic Internet Routing Techniques???
        * A partial survey of recent and historic work on semantic routing and associated semantic enhancements.
        * https://datatracker.ietf.org/doc/html/draft-king-irtf-semantic-routing-survey/
    * ???Semantic Addressing and Routing for Future Networks (SARNET-21) Workshop Report???
        * A report of the main issues discussed during the SARNET-21 workshop
        * https://datatracker.ietf.org/doc/html/draft-galis-irtf-sarnet21-report
    * ???Innovation in Internet Routing and Addressing???
        * A call to arms for researchers in routing and addressing.
        * https://datatracker.ietf.org/doc/draft-iannone-routing-and-addressing-manifesto

This ongoing work has encouraged the idea of forming a ???Routing in the Internet with Semantic Enhancements??? (RISE) Proposed Research Group within the IRTF to provide a forum for researchers and practitioners to explore new Internet routing technologies. In particular, to work on challenges faced by routing systems in the Internet as pressure is placed on them by increasing demands from applications for predictable, differentiated, quality-enhanced connectivity, and service functions.

A draft charter for this Proposed RG is presented in a separate document. In summary, RAISE would aim to:
* Bring significant relevant research and outcomes to the IRTF for broader dissemination.
* Identify existing and future challenges to the Internet routing systems.
* Determine what the basis would be for deciding whether semantic routing and the associated semantic enhancements are viable.
* Encourage research and debate into semantic routing systems and architectures both within the IRTF and via outreach to other conferences.

More specifically, the work of the Proposed RG would be delivered by the research questions derived from draft-king-irtf-challenges-in-routing and set out in the draft charter. 

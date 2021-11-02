# Routing in the Internet with Semantic Enhancements
## RISE Proposed Research Group
## IRTF Draft Charter : Revision 07 : 2021-11-02

Upper-layer applications are placing increasingly sophisticated demands on the network for better quality, more predictability, and increasing reliability. Lower-layer network technologies are advancing rapidly with end-to-end communications extended to include machines and services. These changes have encouraged proposals to introduce routing and addressing behaviors and semantics specific to particular use cases and sets of requirements.

IP-based addressing and network layer routing remain focused on identifying locations of communication and determining paths between those locations. This depends on higher-layer capabilities (e.g., for name-to-location resolution), which can introduce latency and dependencies. New developments in network functions virtualization allow micro-services to be established faster than name resolution lookups or configuration/convergence of routing services making latency and dependencies a real problem.

The performance of routing functions based on the addition of meaning to IP addresses and other properties of packets is called “semantic routing”. Semantic routing proposes to place the support for advanced routing and location functions directly at the packet routing layer, such as through extensions to the identification properties of addresses (what is being identified beyond just network locations) or through performing routing functions on an extended set of inputs (for example, other fields carried in packet headers). 

Such an approach should preserve the Internet architecture as it is today while enabling additional routing function for Service Providers allowing them to modify the default forwarding behaviour based on other information present in the packet and policy configured or dynamically programmed into the routers and devices.

As with all advances in Internet protocols, semantic routing may be considered for Internet-wide deployment or may have their applicability restricted (possibly only initially) to well-defined and contained networks referred to as “limited domains”. Semantic extensions may be opaque within the network (in other words, the additional information it carries is not known by the routers), or may be transparent (so that routers are able, or expected, to act on the information carried in the address). In any case, a concern and consideration must be coexistence with and backward compatibility to existing routing and addressing schemes that are widely deployed.

The Routing in the Internet with Semantic Enhancements (RISE) Proposed Research Group provides a forum for researchers and practitioners to explore new Internet routing technologies. In particular, RISE will work on challenges faced by routing systems in the Internet as pressure is placed on them by increasing demands from applications for predictable, differentiated, quality-enhanced connectivity, and service functions.
The RISE Proposed Research Group will focus on four aspects:
* Surveying proposals and prior work related to semantic enhancements, e.g., to the semantics of the source and destination IP addresses, for the purpose of routing on those enhanced semantics. Bringing significant research work and outcomes to the IRTF for broader dissemination.
* Identifying existing and future challenges to the Internet routing systems that may be mitigated or exacerbated by semantic routing proposals. Examples include the growth of routing tables, convergence times for more extensive networks, the granularity of routing decisions, load-sharing, packet overhead, etc.
* Determining what the basis would be for deciding whether semantic routing and its required semantic enhancements is viable. Plotting out a problem space for semantic routing. Examining the implications and potential consequences of semantic routing and the necessary semantic enhancements to the Internet architecture and routing within the Internet.
* Encouraging research and debate into semantic routing systems and architectures to include considerations of limited domains and their interconnection, additional routing functions, and the scaling and stability of systems with different routing semantics. Providing a forum to introduce researchers working on semantic routing into the IRTF.

The group will report its progress through a publicly accessible website and presentations at IETF meetings and at academic conferences. Documents developed by RISE will be submitted for publication as Experimental or Informational RFCs.

### Research Questions
RISE is driven by a number of key research questions. These are set out in more detail in draft-king-irtf-challenges-in-routing. In all cases, the attention to and consideration of semantic routing are implicit.

* In what network scopes (global, overlay, backbone, limited domain) is it applicable to consider modifications to routing protocols and paradigms? How can limited domains be connected together across the Internet?
* How can the existing routing infrastructure be protected from new developments in routing and the associated semantic enhancements? Must new developments be constrained to isolated domains or run as overlays, or can interworking and co-existence be considered? Do address mappers and protocol gateways introduce fragility and fragmentation? How does the answer to this question change the likelihood of adoption and deployment?
* What features and functions are demanded by new and developing applications that cannot be delivered using existing routing techniques?
* What questions (such as scalability, privacy, robustness, manageability, power consumption) are given insufficient attention during research into new approaches for routing?

The work plan, below, sets out how RISE will approach these questions.

### Meetings
Regular working meetings will be held three to five times per year at locations convenient to the majority of the participants, or online as appropriate. Working meetings will vary from one- or two-hour working sessions (typically held as part of IETF meetings) to day-long meetings when co-located with conferences or events. RISE will assist in the continued organization of workshops and dedicated sessions at relevant external events.

### Work Plan
An initial set of work items to investigate the topics-mentioned above are itemized below. This list will help to better scope the activities of RISE, and it is expected that the list will evolve over time according to research and discussions.
1. Survey and catalog prior art and ongoing research on topics related to applying additional routing semantics.
2. Research and document taxonomy and ontology of routing schemes and associated semantic enhancements (together with their forwarding plane logic) that can flexibly and efficiently adapt to different routing semantics.
3. Describe the technical, commercial, and practical benefits and drawbacks of applying routing schemes and associated semantic enhancements within limited domains. Analyze the requirements for domain identification, domain capability recognition, and domain isolation. Document architectures for interconnecting limited domains across the Internet using overlays, gateways, and integrated routing.
4. Define, collect, and detail the research questions that need to form part of the experimentation and validation of flexible routing and schemes.
    * Research the impact on routing scalability of the various semantic routing schemes, both in terms of convergence times and routing table size.
    * Study methods to enable the co-existence of multiple routing semantics within the same network, such as service-based routing and topology-based routing in the same edge network. This includes consideration of interoperability between devices and network domains directly, using tunnels/layering, or through gateways.
    * Research the potential impact to the control and forwarding plane through the need for suitable address assignment, advertisement, routing protocols and forwarding behaviors, which would meet the new action models that underlie the routing and addressing.
    * In collaboration with PEARG, discuss, assess, research, and document the applicability of semantic routing technologies as methods to ensure routing security and privacy.
    * Search for possible detrimental effects of semantic routing schemes and their associated semantic enhancements, and investigate potential mitigations.

RISE will redirect work to the IETF when appropriate engineering projects are identified. RISE is expected to cooperate with other research groups, especially ICNRG, COINRG, and PEARG, to determine the correct place to focus efforts and to reduce duplication while supporting the activities of each research group.

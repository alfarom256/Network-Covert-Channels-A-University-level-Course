# Network Information Hiding 101: Terminology, Methodology of Network Steganography / Network Covert Channels

### Prof. Dr. Steffen Wendzel, [website](https://www.wendzel.de)
Worms University of Applied Sciences, contact: wendzel (at) hs-worms (dot) de

## Introduction
This is a open online course for network covert channels. The course contains video material and slides that I use in my undergraduate and graduate courses at Worms University of Applied Sciences, Germany. (I recorded the videos anyway, so why shouldn't I make them public.) I also used the slides at other universities, summer schools etc. over the years.

*Note:* More material will be added. You can always find the latest version of my slides here, as I updated these slides over the years and will continue to do so. Feel free to use my slides in your own class.

I made sure that references are using links so that you and your students can get easier access to the publications.

Please note that most content of this class is based on the book W. Mazurczyk, S. Wendzel, S. Zander, A. Houmansadr, K. Szczypiorski: [Information Hiding in Communication Networks](https://ieeexplore.ieee.org/book/7434879), WILEY-IEEE, 2016. If you are an IEEE member, you should be able to download the book for free.

## Outline

*This online class **starts on May 5th, 2020 but all content will remain online on Github for those who want to start later (or in a few years)**. I will upload videos once in a week.* Please note that some weeks contain multiple videos:


| Week      | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|-----------|---|---|---|---|---|---|---|---|
| Chapter 1 | X *N,M* |   |   |   |   |   |   |   |
| Chapter 2 |   | X *M* |   |   |   |   |   |   |
| Chapter 3 |   | X *M* |   |   |   |   |   |   |
| Chapter 4 |   |   | X *N,M* |   |   |   |   |   |
| Chapter 5 |   |   | X *N,M*|   |   |   |   |   |
| Chapter 6 |   |   |   | X *M* |   |   |   |   |
| Chapter 7a|   |   |   |   | X *N,M* |   |   |   |
| Chapter 7b|   |   |   |   | X *M* |   |   |   |
| Chapter 8 |   |   |   |   |   | X *M* |   |   |
| Chapter 9 |   |   |   |   |   | X |   |   |
| Chapter 10a|   |   |   |   |   |   | X |   |
| Chapter 10b|   |   |   |   |   |   | X |   |
| Chapter 11|   |   |   |   |   |   |   | X |

- *N*: relevant for *Network Security* class (B.Sc. level)
- *M*: relevant for *Mobile Security* class (M.Sc. level)

### Week 1: Chapter 1 - Introduction to Steganography and Covert Channels (May 5th, 2020)
This chapter provides an overview of the whole class. Afterwards, fundamental terminology, taxonomy and history of information hiding will be covered. The chapter also highlights some use-cases (legitimate and criminal ones) and tells you a bit about the CUING initiative.

- **Video:** [YouTube](https://www.youtube.com/watch?v=7YXXrbTah_s)

- **Slides:** [PDF](https://github.com/cdpxe/Network-Covert-Channels-A-University-level-Course/blob/master/slides/NIH_Ch1.pdf)

- **Reading Assignment:**
	- W. Mazurczyk, S. Wendzel, S. Zander, A. Houmansadr, K. Szczypiorski: [Information Hiding in Communication Networks, **Chapters 1 and 2**](https://ieeexplore.ieee.org/book/7434879), WILEY-IEEE, 2016.

- **Optional Papers to Read:**
	- F. Petitcolas, R. Anderson, M. Kuhn: [Information Hiding – A Survey](https://ieeexplore.ieee.org/abstract/document/771065), Proc. IEEE, 87(7), 1999.
	- B. Pfitzmann: [Information Hiding Terminology](https://doi.org/10.1007/3-540-61996-8_52), Proc. 1st Information Hiding Workshop, Springer, 1996.
	- E. Zielinska, W. Mazurczyk, K. Szczypiorski: [Trends in Steganography](https://dl.acm.org/doi/10.1145/2566590.2566610), Comm. ACM, 2014.
	-  K. Cabaj, L. Caviglione, W. Mazurczyk, S. Wendzel, A. Woodward, S. Zander: [The New Threats of Information Hiding: the Road Ahead](https://ieeexplore.ieee.org/document/8378979/), IT Professional, IEEE, 2018.
	- L. Caviglione: [Steg in the Wild](https://github.com/lucacav/steg-in-the-wild) (A list of attacks and malware using steganography or information hiding), Github repository.

- **Exercise:**
	- Explain one historic method of steganography that was not explained during the lecture in a short talk in front of the other students.
	- Is there a terminological inconsistency for the terms covert channel, network covert channel, steganography and network steganography given the introduced taxonomy? If yes: explain. (Chapter 2 of W. Mazurczyk et al., 2016)
	- Can Information Hiding methods be applied to deduce cryptography keys from encryption/decryption tools? If yes: how?
___


### Week 2-a: Chapter 2 - Introduction to classic covert channels (May 12th, 2020)
First, simple methods for local (system-internal) covert channels are discussed. Second, covert channels between Docker containers and for Android are shown.

- **Video:** [YouTube](https://youtu.be/MBV-NFQLH34)

- **Slides:** [PDF](https://github.com/cdpxe/Network-Covert-Channels-A-University-level-Course/blob/master/slides/NIH_Ch2.pdf)

- **Reading Assignment:**
	- none for this chapter

- **Optional Papers to Read:**
	- W. Mazurczyk, L. Caviglione: [Steganography in Modern Smartphones and Mitigation Techniques](https://ieeexplore.ieee.org/abstract/document/6884798), IEEE Communications Surveys & Tutorials, Vol. 17(1), 2014.
	- J.-F. Lalande, S. Wendzel: [Hiding privacy leaks in Android applications using low-attention raising covert channels](https://ieeexplore.ieee.org/abstract/document/6657308/), Proc. 8th ARES, Regensburg, DE, IEEE, 2013.

- **Exercise:**
	- Low-attention raising covert channels (such as described in the paper by Lalande and Wendzel above) are usually linked to a small bitrate. Explain why such channels can be considered valuable especially in network environments.
	- Given the rising trend of censorship circumvention, why do you think is Information Hiding not applied by a large number of people? (And who does actually apply it?)

___

### Week 2-b: Chapter 3 - Fundamental countermeasures (not network-specific) (May 12th, 2020)
In this chapter, you will learn how covert channels can be detected, eliminated, and limited on the basis of exemplary countermeasures. These countermeasures can be applied at different states of a system's lifetime (design-phase to operation phase). In particular, I cover the Shared Resource Matrix (SRM) methodology, Covert Flow Trees (CFT), Fuzzy Time, and the Spurious Processes Approach.

- **Video:** [YouTube](https://youtu.be/6cjsPzLscd8)

- **Slides:** [PDF](https://github.com/cdpxe/Network-Covert-Channels-A-University-level-Course/blob/master/slides/NIH_Ch3.pdf)

- **Reading Assignment:**
	- R. Kemmerer, P. Porras: Covert Flow Trees: A Visual Approach to Analyzing Covert Storage Channels, Trans. Software Engineering, IEEE, 1991.

- **Optional Papers to Read:**
	- *in German:* I discuss SRM, extended SRM (Gypsy SRM), CFT, the Pump, and several other fundamental anti-covert channel concepts in my book S. Wendzel: *Tunnel und verdeckte Kanäle im Netz*, Springer, 2012 (**[Chapter 6](https://link.springer.com/chapter/10.1007/978-3-8348-2143-0_6)**).

- **Exercise:**
	- Which method would you apply to eliminate/spot covert channels in the following situations:
		- The company you are working for wishes to get a certificate (e.g. a high level of EAL) for their product; the certificate requires a code-level audit that lists all possible covert storage channels.
		- You plan to design a new product (not implemented in code). You need to perform a covert channel analysis using the product’s specification.
		- Your company plans to sell a product to a military customer. The customer requires a covert timing channel audit, which you performed. However, the customer will only accept covert channels with a channel capacity below 1 bit/s.
	- How could you create a policy-breaking covert channel during your exam in order to secretly exchange answers to exam questions?
		- Link this scenario to the Prisoner’s Problem.


___

### Week 3-a: Chapter 4 - Fundamental network information hiding techniques (May 19th, 2020)
This chapter introduces basic methods for realizing network covert channels and their different types, in particular active and passive covert channels, intentional and unintentional (side) channels, and direct and indirect covert channels.

- **Video:** [YouTube](https://www.youtube.com/watch?v=29s696QwHVM)

- **Slides:** [PDF](https://github.com/cdpxe/Network-Covert-Channels-A-University-level-Course/blob/master/slides/NIH_Ch4.pdf)

- **Reading Assignment:**
	- L. Caviglione, W. Mazurczyk: [Understanding Information Hiding in iOS](https://ieeexplore.ieee.org/abstract/document/7030266), IEEE Computer, Vol. 48(1), 2015.

- **Exercise:**
	- In the paper of the reading assignment, you will find a steganographic method called *iStegSiri* for iOS published by Caviglione and Mazurczyk. Explain how it works! Also, [here](https://spectrum.ieee.org/tech-talk/telecom/security/malware-could-steal-data-from-iphones-using-siri) is a news article about iStegSiri.

___

### Week 3-b: Chapter 5 - Getting the big picture: hiding patterns (May 19th, 2020)
In this chapter, so-called *hiding patterns* are introduced. Patterns are a universal tool that is popular in software engineering and other disciplines, even outside of informatics. Hiding patterns are an easy way to describe and understand how data can be hidden using network covert channels. Instead of studying hundreds of separate hiding techniques, one can simply grasp all their core ideas using hiding patterns.

- **Video:** [YouTube](https://www.youtube.com/watch?v=0ztPHur0LUY)

- **Slides:** [PDF](https://github.com/cdpxe/Network-Covert-Channels-A-University-level-Course/blob/master/slides/NIH_Ch5.pdf)

- **Reading Assignment:**
	- S. Wendzel, S. Zander, B. Fechner, C. Herdin: [Pattern-based survey and categorization of network covert channel techniques](https://doi.org/10.1145/2684195), ACM Computing Survey (CSUR), Vol. 47(3), ACM, 2015.
	- W. Mazurczyk, S. Wendzel, S. Zander, A. Houmansadr, K. Szczypiorski: [Information Hiding in Communication Networks, **Chapter 3**](https://ieeexplore.ieee.org/book/7434879), WILEY-IEEE, 2016.

- **Optional Papers to Read:**
	- W. Mazurczyk, S. Wendzel, K. Cabaj: [Towards Deriving Insights into Data Hiding Methods Using Pattern-based Approach](https://doi.org/10.1145/3230833.3233261), in Proc. ARES, ACM, 2018.

- **Exercise:**
	- Get an overview of the [CCEAP tool and its protocol](https://ih-patterns.blogspot.com/p/cceap.html). Work through the provided sample [exercises](https://github.com/cdpxe/CCEAP/tree/master/sample_exercises) and try to understand the provided solutions.

___

### Week 4: Chapter 6 - Staying under the radar: sophisticated hiding methods and distributed hiding patterns (May 26th, 2020)
This chapter covers distributed hiding methods, including pattern variation, pattern hopping, protocol switching (protocol channels, protocol hopping covert channels), dynamic overlay routing for covert channels, micro protocols (covert channel internal control protocols, including their optimization), reversible data hiding (RDH), and dead drops that exploit network caches.

- **Video:** [YouTube](https://www.youtube.com/watch?v=YicdOu10FmE)

- **Slides:** [PDF](https://github.com/cdpxe/Network-Covert-Channels-A-University-level-Course/blob/master/slides/NIH_Ch6.pdf)

- **Reading Assignment:**
	- W. Mazurczyk, P. Szary, S. Wendzel and L. Caviglione: [Towards Reversible Storage Network Covert Channels](https://doi.org/10.1145/3339252.3341493), in Proc. Third International Workshop on Criminal Use of Information Hiding (CUING 2019), pp. 69:1-69:8, ACM, 2019.
	- W. Mazurczyk, S. Wendzel, S. Zander et al.: [Information Hiding in Communication Networks, **Chapter 4**](https://ieeexplore.ieee.org/book/7434879), Wiley-IEEE, 2016.

- **Optional Papers to Read:**
	- Yarochkin, F. et al.: [Towards adaptive covert communication system](https://ieeexplore.ieee.org/abstract/document/4725291/), in Proc. 14th IEEE Pacific Rim International Symposium on Dependable Computing. IEEE, 2008.
	- S. Wendzel, J. Keller: [Hidden and UnderControl](https://doi.org/10.1007/s12243-014-0423-x), Annals of Telecommunications (ANTE), Springer, 2014.
	- S. Wendzel, J. Keller: [Systematic Engineering of Control Protocols for Covert Channels](https://link.springer.com/chapter/10.1007/978-3-642-32805-3_11), in Proc. Communications & Multimedia Security (CMS), Springer, 2012.
	- C. Krätzer, J. Dittmann, A. Lang, T. Kühne: [WLAN steganography: a first practical review](https://doi.org/10.1145/1161366.1161371), in Proc. 8th Workshop on Multimedia and Security (MM&Sec), ACM, 2006.
	- S. Schmidt, W. Mazurczyk, R. Kulesza, J. Keller, C. Caviglione: [Exploiting IP telephony with silence suppression for hidden data transfers](https://www.sciencedirect.com/science/article/pii/S0167404818305777), Computers & Security, Vol. 79, 2018.
	- Szczypiorski, K., Margasiński, I., Mazurczyk, W., Cabajetal.: [TrustMAS: Trusted communication platform for multi-agent  systems](https://link.springer.com/chapter/10.1007/978-3-540-88873-4_7), in Proc. OTM On the Move to Meaningful Internet Systems, Springer, 2008.

- **Exercise:**
	- Which pattern-based distributed hiding methods do protocol channels and protocol hopping covert channels belong to?
	- Is the micro protocol grammar shown in the slides a language-subset of the cover protocol language?
	- Have a look at the above-mentioned paper on by Schmidt et al.: How do the authors hide data in IP telephony traffic?
	- Why was it beneficial to [improve the NEL phase](https://dl.gi.de/handle/20.500.12116/18270)? Why does the original NEL phase suffer from a *Two-army Problem* and what is a Two-army Problem?
	- In the paper referenced above by Krätzer et al. you can read about a network steganography method for IEEE 802.11 (WLAN) networks. How does it work? Can you link the hiding approach to a particular pattern?
	- How do you think that distributed hiding methods could be detected or limited? (Will be answered in the next chapter.)

___

### Week 5: Chapter 7 - Selected network-level countermeasures (June 2nd, 2020)
Chapter 7 finally introduces methods to combat network covert channels. The chapter is separated into two parts. **Part A** covers selected basic methods, namely traffic normalization (preventing/limiting), three methods by Berk et al. and Cabuk et al. (detection of inter-packet times pattern), and finally, the so-called *countermeasure variation*. **Part B** introduces countermeasures that help limiting and detecting sophisticated network covert channels, namely the protocol switching covert channels and the NEL phase. These methods are the *protocol (switching covert) channel-aware active warden* (PCAW) and the *dynamic warden*.

- **Video:** [part A, YouTube](https://www.youtube.com/watch?v=DW8eT5NtoxE), [part B, YouTube](https://www.youtube.com/watch?v=v3AeSPAmF8Y)

- **Slides:** [part A, PDF](https://github.com/cdpxe/Network-Covert-Channels-A-University-level-Course/blob/master/slides/NIH_Ch7a.pdf), [part B, PDF](https://github.com/cdpxe/Network-Covert-Channels-A-University-level-Course/blob/master/slides/NIH_Ch7b.pdf)

- **Reading Assignment:**
	- W. Mazurczyk, S. Wendzel, S. Zander et al.: [Information Hiding in Communication Networks, **Chapter 8**](https://ieeexplore.ieee.org/book/7434879), Wiley-IEEE, 2016.
	- S. Wendzel, F. Link, D. Eller, W. Mazurczyk: [Detection of Size Modulation Covert Channels Using Countermeasure Variation](http://www.jucs.org/jucs_25_11/detection_of_size_modulation), Journal of Universal Computer Science (J.UCS), Vol. 25(11), pp. 1396-1416, 2019.

- **Optional Papers to Read:**
	- S. Cabuk, C. E. Brodley, C. Shields: [IP covert channel detection](https://dl.acm.org/doi/abs/10.1145/1513601.1513604), Trans. Information and System Security (TISSEC) Vol. 12(4), ACM, 2009.
	- W. Mazurczyk, S. Wendzel, M. Chourib, J. Keller: [Countering Adaptive Network Covert Communication with Dynamic Wardens](https://doi.org/10.1016/j.future.2018.12.047), Future Generation Computer Systems (FGCS), Vol. 94, pp. 712-725, Elsevier, 2019.

- **Exercise:**
	- t.b.d., will be added in the next semester(s) using the *NeFiAS* tool I currently implement (not published, yet)

___

### Week 6-a: Chapter 8 - Replicating experiments for scientific advancement (June 9th, 2020)
First, I briefly discuss why we need replication studies and which obstacles prevent the conduction of these studies. Second, I show one study that we conducted ourselves.

- **Video:** [YouTube](https://www.youtube.com/watch?v=hs_nPTwQXXA)

- **Slides:** [PDF](https://github.com/cdpxe/Network-Covert-Channels-A-University-level-Course/blob/master/slides/NIH_Ch8.pdf)

- **Optional Papers to Read:**
	- S. Wendzel, L. Caviglione, W. Mazurczyk, J.-F. Lalande: [Network Information Hiding and Science 2.0: Can it be a Match?](https://www.researchgate.net/publication/316215336_Network_Information_Hiding_and_Science_20_Can_it_be_a_Match), International Journal of Electronics and Telecommunications 63(2), 2017.

- **Exercise:**
	- Answer the following questions:
		- Why is it essential to replicate experiments?
		- What can scientists do to support experimental replications of their *own* work?
		- What is commonly referred to under the term *Open Science*?

___

### Week 6-b: Chapter 9 - *OMG! I found a new hiding method. How do I become famous?!1!* a.k.a. How to describe a new hiding method in a paper? (June 9th, 2020)
When a new hiding technique is found, how should it be described in a way that other authors can easily access it? How to ease replication studies? How to ease the process of finding out what still needs to be done? These questions can be answered with the *unified description method* for network information hiding techniques explained in this chapter. Moreover do I introduce the *creativity metric* that helps to decide about the novelty of a research contribution.

- **Video:** [YouTube](https://www.youtube.com/watch?v=viieBAdAQh0)

- **Slides:** [PDF](https://github.com/cdpxe/Network-Covert-Channels-A-University-level-Course/blob/master/slides/NIH_Ch9.pdf)

- **Reading Assignment:**
	- S. Wendzel, W. Mazurczyk, S. Zander: [Unified Description Method for Network Information Hiding Methods](http://dx.doi.org/10.3217/jucs-022-11-1456), Journal of Universal Computer Science (J.UCS), Vol. 22(11), 2016.

- **Exercise:**
	- Read the above-mentioned paper on the unified description method and answer the following questions:
		- What is the difference between the two attributes *required properties of the carrier* and *covert channel properties*?
		- Why is the attribute on *control protocols* not mandatory in the unified description method?
		- How does the *creativity metric* work together with the unified description method?

___

### Week 7: Chapter 10 - *My smart fridge does strange things …* a.k.a. Steganography in the Internet of Things (IoT) (June 16th, 2020)
In the Internet of Things (and Cyber-physical Systems, CPS), data can either be hidden within network communications (e.g. in IoT protocols) *or* in can be hidden the CPS *components* (e.g. unused registers or states of actuators). I will discuss these methods as well as scenarios in this conference talk below. However, please note that the PDF files contain an extended scenario. I plan to update the PDF slides in the coming years as there is still quite a lot to say about this chapter.

- **Video:** [part A, YouTube](https://www.youtube.com/watch?v=P9XYV4mcPV0), [part B, YouTube](https://www.youtube.com/watch?v=Q7eAcBzojvo). Part B is the video of the talk S. Wendzel, G. Haas, W. Mazurczyk: *Information Hiding in Cyber-physical Systems*, presented during the 2nd Int. BioSTAR workshop in late May, 2017 (IEEE Security & Privacy Workshops, San José, CA)

- **Slides:** [part A, PDF](https://github.com/cdpxe/Network-Covert-Channels-A-University-level-Course/blob/master/slides/NIH_Ch10a.pdf)
, [part B, PDF](https://github.com/cdpxe/Network-Covert-Channels-A-University-level-Course/blob/master/slides/NIH_Ch10b.pdf)

- **Reading Assignment:**
	- Steffen Wendzel, Wojciech Mazurczyk, Georg Haas: [Steganography for Cyber-physical Systems](http://www.riverpublishers.com/journaldownload.php?file=RP_Journal_2245-1439_621.pdf), Journal of Cyber Security and Mobility (JCSM), Vol. 6(2), pp. 105-126, River Publishers, 2017.
	- Aleksandar Velinov, Aleksandra Mileva, Steffen Wendzel, Wojciech Mazurczyk: [Covert Channels in the MQTT-Based Internet of Things](https://ieeexplore.ieee.org/document/8890870/), IEEE ACCESS, 2019.
	- A Mileva, A Velinov, D Stojanov: [New covert channels in Internet of Things](http://eprints.ugd.edu.mk/20423/1/securware_2018_2_10_30122.pdf), in Proc. Securware 2018.

- **Exercise:**
	- What is the difference between an intentional covert channel and an intentional side channel in a CPS? Can you name a few examples? Both terms of CPS Steganography are introduced in [this paper](https://www.researchgate.net/publication/229092563_Covert_and_Side_Channels_in_Buildings_and_the_Prototype_of_a_Building-aware_Active_Warden/link/00b495349285c92bbd000000/download). What was the solution proposed by this paper to combat both types of channels?
	- In [this paper](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=6468400&tag=1), I describe how an MLS-based filtering can prevent covert and side channels in CPS network communications (exemplified using smart buildings). How does this work? What are limitations?

___

### Week 8: Chapter 11 - Summary and Overall conclusion (June 23rd, 2020)
This chapter summarizes what we have learned in the ten previous chapters. I also highlight open research problems that might support you in finding topics for a Master or even a PhD thesis.

- **Video:** [YouTube](https://www.youtube.com/watch?v=pXo3mdmR_yM)

- **Slides:** [PDF](https://github.com/cdpxe/Network-Covert-Channels-A-University-level-Course/blob/master/slides/NIH_Ch11.pdf)

- **Reading Assignment:** none

- **Exercise:**
Congratulations, you made it through the whole class! **Now it is time for the final (big!) exercise!** Try to find a new network protocol for which there is absolutely no work available that analyzes covert channels in this protocol (use [Google Scholar](https://scholar.google.com) to find such works). Next, analyze the protocol regarding all known hiding patterns and describe all covert channels that you found using the unified description method. If you like, submit your paper to a conference (or: let me know and I can potentially link the paper at least here).

EOF.

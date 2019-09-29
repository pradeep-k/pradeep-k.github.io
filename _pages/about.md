---
permalink: /
title: ""
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am an assistant professor in the [Department of Computer Science](https://www.wm.edu/as/computerscience/), [William & Mary](https://www.wm.edu/) (The second oldest university in the USA, and the public Ivy). I completed my PhD in Computer Engineering at the George Washington University (GWU). My research interest is at the intersection of Data Science and Cyber-infrastructure, developing an eco-system to plug the emerging storage and compute hardwares in the system software stack of data analytics. This roughly translates to IO, File and Storage Systems, Memory sub-system, Data Management, and High-Performance Data Analytics with a focus on emerging Big Data applications such as Graph Processing, Stream Analytics, Machine Learning etc. I completed my Bachelor of Technology degree from Indian Institute of Technology, Dhanbad, India in the year 2007.

***If you are interested in doing research on any aspect of data that will accelerate the data-led innovation, do not hesitate to send me an email with your CV to initiate the discussion. Full scholarships are available to deserving PhD students. Admission is formally managed by the Department. See the [link](https://www.wm.edu/as/computerscience/graduate/admission/index.php) for admission process.***

## Current Research Projects

I am leading the **[Data Lab](https://github.com/the-data-lab)** in the Department of Computer Science, William and Mary. Everything that we do here are related to huge data that is a norm today. Following projects are under active research in the Data Lab, but a lot more are still in the drawing board phase:
- **Unified Graph Analytics at Scale:** A distributed Graph analytics engine that is envisioned to be a unified framework for running graph batch and stream analytics both in evolving and static graphs. This framework should be able to handle diverse classes of graphs, including social graph, property graph, provenance graph, RDF or semantic graph etc. See our conference and journal version of GraphOne to get an idea of our baseline single node system.
- **Machine Learning on Graphs:** Accuracy and Scalability both are big problems for running machine learning in the graph type data. Recent advances in deep learning has seen great accuracy and scalability on image and sequence data, but not on graph data. Graph data model is envisioned to be an universal data model to represent non-image, non-sequence type data. Hence, running deep learning on graph data can be very useful to identify important information, and take the frontier of machine learning to new heights. We are exploring our strengths in graph domain to identify opportunity for accuracy and scalability in a distributed setup. The framework is envisioned to be a graph learning system.
- **Storage Systems Research:** Data explosion has led to many advances in data-led discovery, and 21st century is all about data. Can you imagine how those data will be analyzed, if they can't fit in memory. This requires intelligent Storage system. Our team has in-depth academic and industrial expertise in handling large data utilizing the NoSQL data stores and combining them with the recent hardware technologies, such as NVMe Flash drives, Solid-State-Drives (SSDs) and Non-volatile or persistent Memories (NVMs). We have proposed changes in end-to-end storage stack starting from user-space data-store to kernel level modules. Our current work is exploring NVM for emerging applications, as well as working on modifying the storage stack to find a rightful place for NVM. Do you have an idea that can utilize the persistency property of NVM in a better way, you will be eagerly welcomed.
- **Cloud Infrastructure and Serverless Computing:** Data led discovery requires huge amount computation power. Cloud infrastructure plays a big role in providing those infrastructure. Recent advances in container technologies has enabled a quick deployment of such applications. Unfortunately, the support for stateful services (they handle data) are not sufficient, and requires more research.    


## Publication

Following papers either have been published or are about to be published. Feel free to send me an email for the paper or the code. There are many exciting works that are in the pipeline that will be submitted soon to top tier conferences and journals. If you are interested in knowing more about those papers, send me an email to initiate the discussion. * denotes the top-tier venues, that are extremely competitive to get in.

**\*[ACM Transcation on Storage]** Pradeep Kumar, Howie Huang. _GraphOne: A Data Store for Real-time Analytics on Evolving Graphs._ Extended Version of FAST'19 Paper, Accepted on 20th September, 2019. Send me an email for the paper.  
**\*[USENIX FAST'19]** Pradeep Kumar, Howie Huang. _GraphOne: A Data Store for Real-time Analytics on Evolving Graphs._ [Blog] [[PDF](https://www.usenix.org/system/files/fast19-kumar.pdf)] [[PPT](https://www.usenix.org/sites/default/files/conference/protected-files/fast19_slides_kumar.pdf)] [[Code](https://github.com/the-data-lab/GraphOne)]

GraphOne is first ever system that can perform diverse set of analytics on the same data-store, and replaces the current practice of deploying specialized systems for each type of analytics. The above two works propose following contributions:
- **GraphView Abstraction:** Unification of Batch and Stream analytics from same data-store under one system using Graph Views Abstraction: We have separated the graph ingestion from the graph analytics path. So, each analytics can focus on itself without worrying about concurrent data ingestion or any other analytics. So, there is only one global data-store, but many types of analytics can run on top it. We are able to beat all the specialized graph systems, as well as their ingestion rates.
- **Data Visibility abstraction:** Fine-grained ingestion is always costly. So, GraphOne moves the cost of fine-grained ingestion from read-path to write path, implying that if your analytics does not required to be performed in fine-grained ingested data, you don't have to worry about additional cost associated with fine-grained ingestion. But if your analytics care for it, than only your analytics will pay the cost, not the others who don't need it. We then propose optimization to reduce this cost. This helps us to support very high arrival rate of graph data at fine granularity, but offers analytics performance at the cost of batched updates.
- **Concurrent Real-time Analytics:** Due to the separation of computation from data management, we are now able to run multiple analytics of same or diverse types concurrently without copying the graph data, yes one copy of graph data, and multiple independent analytics.

**[IEEE HPEC'17]** Yang Hu, Pradeep Kumar, Guy Swope (Raytheon), H. Howie Huang. _TriX: Triangle Counting at Extreme Scale._ **Finalist, 2017 IEEE/Amazon/DARPA Graph Challenge**  
**\*[SC'16]** Pradeep Kumar, Howie Huang. G-Store: High-Performance Graph Store for Trillion-Edge Processing. [Blog] [[PDF](https://pradeep-k.github.io/files/G-Store-SC16.pdf)] [[PPT](https://pradeep-k.github.io/files/G-Store-SC16-PPT.pdf)] [[Code](https://github.com/the-data-lab/gstore)]

The above two works present graph computing with extreme scale. G-Store is first ever system to demonstrate graph computing at trillion-edge scale within a commodity server. Many techniques make this possible:  
- **SNB Format:** A new format which is space efficient (up to 8x space saving, less disk IO) as well as hardware cache friendly (algorithmic metadata takes advantage of L2 caches).
- **Physical Grouping:** Algorithmic metadata takes advantage of LLC caching, while IO is converted to sequential. Double benefit.
- **Graph Caching:** G-Store is first ever system to propose a graph specific caching policy.
- **Slide-Cache-Rewind Scheduler:** Takes advantage of IO and compute overlap, as well as utilizing even the last drop of data available in the memory before throwing them away.

**\*[USENIX ATC'17]** Pradeep Kumar, Howie Huang. _Falcon: Scaling IO Performance in Multi-SSD Volumes._ [Blog] [[PDF](https://www.usenix.org/system/files/conference/atc17/atc17-kumar.pdf)] [[PPT](https://www.usenix.org/sites/default/files/conference/protected-files/atc17_slides_kumar.pdf)] [[Code](https://github.com/the-data-lab/falcon)]

Do you Think that today's IO stack can deliver the raw performance, if multiple SSDs are combined in a volume. The answer is no, because of the per-volume convention that is hard-coded in the IO stack. We have proposed Falcon IO Stack that introduces a new convention of per-drive IO processing, that introduces a new layer in the IO stack to bring the best of each drivers that are part of the volume. Further, the Falcon IO Stack optimizes its merging, sorting, and dispatch process to make it future ready, where we have shown that our new IO stack can saturate the newer NVMe Flash.

**[IEEE Big Data Congress'17]** Pradeep Kumar, Howie Huang. _SafeNVM: A Non-Volatile Memory Store with Thread-Level Page Protection._ [Blog] [[PDF](https://pradeep-k.github.io/files/SafeNVM.pdf)] [[PPT](https://pradeep-k.github.io/files/SafeNVM-ppt.pdf)] [Code]

Storing persistent data in NVM is not safe against software induced corruptions as it used to be if stored in disks. Do know why, and what will change if we store data in NVM instead of disk. This paper discusses the unknown safety conventions that is implicitly followed when data moves from DRAM to Disks. But that convention is broken due to presence of NVM. Our techniques bring those conventions back to protect your persistent data in NVM from any software induced corruption.

## Industry Experience

I have over 6 years of industry research and development experience in the broader Systems area. During my PhD, I interned in IBM Research at their storage research group. Prior to my PhD, I worked as File System/Operating System kernel developer, and Distributed Systems Programmer for cluster-mode storage systems in NetApp Inc. at their Bangalore (India) research and development center. Prior to that I worked at Huawei technologies at their Bangalore, Shanghai and Shenzhen center.

---
permalink: /
title: ""
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am an assistant professor in the [Department of Computer Science](https://www.wm.edu/as/computerscience/), [William & Mary](https://www.wm.edu/) (The second oldest university in the USA, and the public Ivy). My research interest is at the intersection of Data Science and Computer Systems. My research group (the data lab) develops eco-systems, platforms, systems, and libraries for Data Science systems while plugging the emerging storage and compute hardware in the system software stack of data science to tackle scalability, performance, and data safety. This roughly translates to Distributed Systems, IO, File and Storage Systems, Memory sub-systems, Data Management, and High-Performance Data Analytics with a focus on emerging Big Data applications such as Graph Processing, Stream Analytics, Deep Learning, etc. 

***If you are interested in researching any aspect of data that will accelerate data-led innovation, do not hesitate to send me an email with your CV to initiate the discussion. Currently looking for students who are good at Python and C++/CUDA, and and know Deep Learning and Systems both. Knowledge of Graphs is a bonus. Full scholarships are available to deserving PhD students. Admission is formally managed by the Department. See the [link](https://www.wm.edu/as/computerscience/graduate/admission/index.php) for admission process.***

***W&M Undergraduates: Funding is now available for W&M undergraduates with strong Computer Systems or Data Science background, and who are highly motivated to do work at their intersection.***

***I am teaching a new course in Systems for Deep Learning in Fall, 2023. Current MS and PhD students, please register if you want to know the current state of the art. We will be using GraphPY as an education tool.***

## Current Research Projects

I am leading the **[Data Lab](https://github.com/the-data-lab)** in the Department of Computer Science, William & Mary. Everything that we do here is related to huge data that is a norm today. The following projects are under active research in the Data Lab, but a lot more are still in the drawing board phase:
- **Deep Learning on Sparse Data and Models (Graphs):** Accuracy and Scalability both are big problems for running machine learning in graph-type data. Recent advances in deep learning have seen great accuracy and scalability on image and sequence data, but not on graph data. The graph data model is envisioned to be a universal data model to represent non-image, non-sequence type data. Hence, running deep learning on graph data can be very useful to identify important information, and take the frontier of machine learning to new heights. We are exploring our strengths in the graph domain to identify opportunities for accuracy and scalability in a distributed setup. The framework is envisioned to be a graph learning system. **A very basic prototype is available** for handling sparsity as a first-class citizen in data and model, and a Paper is under review now. More work is in progress now. 
- **Unified Graph Analytics at Scale:** A distributed Graph analytics engine that is envisioned to be a unified framework for running graph batch and stream analytics both in evolving and static graphs. This framework should be able to handle diverse classes of graphs, including social graphs, property graphs, provenance graphs, RDF or semantic graphs, etc. It should provide data analysis on various types of windows, and non-windows efficiently, with similar programming experience. See our conference and journal version of GraphOne to get an idea of our baseline single-node system. **We now have a distributed version of GraphOne available. We now also support Windows**. A paper is under review now, while more work is in progress.
- **Storage Systems Research:** Data explosion has led to many advances in data-led discovery, and the 21st century is all about data. Can you imagine how those data will be analyzed, if they can't fit in memory? This requires an intelligent Storage system. Our team has in-depth academic and industrial expertise in handling large data utilizing the NoSQL data stores and combining them with the recent hardware technologies, such as NVMe Flash drives, Solid-State-Drives (SSDs), and Non-volatile or persistent Memories (NVMs). We have proposed changes in the end-to-end storage stack starting from user-space data store to kernel-level modules. Our current work is exploring NVM for emerging applications, as well as working on modifying the storage stack to find a rightful place for NVM. Do you have an idea that can utilize the persistency property of NVM in a better way, you will be eagerly welcomed.
- **Cloud Infrastructure and Serverless Computing:** Data-led discovery requires a huge amount of computation power. Cloud infrastructure plays a big role in providing that infrastructure. Recent advances in container technologies have enabled a quick deployment of such applications. Unfortunately, the support for stateful services (they handle data) is not sufficient and requires more research.
- **Bring your Research Problems:** The Data Lab welcomes any research questions that you are excited about in the broader field of Systems, Data Science, or analytics.


## Publication

The following papers either have been published or are about to be published. Feel free to send me an email for the paper or the code. Many exciting works are in the pipeline that will be submitted soon to top-tier conferences and journals. If you are interested in knowing more about those papers, send me an email to initiate the discussion. * denotes the top-tier venues, that are extremely competitive to get in.


**G-Bench** was accepted by GrAPL'23. Congratulations Sarah!!!

We have made **[GraphPY](https://github.com/the-data-lab/deep-codegen)**, a Platform for Systems Research and Education, open-source. If you are a systems researcher and want to use the platform to teach deep learning, please reach out to us. Congratulations Yidong for putting 2 years into this effort, which makes writing systems code independent of DL framework-- A great break-through that cuts the learning curve, that we do not need to know the internals of DL Frameworks, such as Pytorch and TensorFlow. 

**[GrAPL'23]** Pradeep Kumar, Sarah Revillar. _G-Bench: Fair Benchmarking to Support Innovations in Streaming Graph Systems._ 2023 IEEE International Parallel and Distributed Processing Symposium Workshops (IPDPSW).[[Code](https://github.com/the-data-lab/gbench)].

**\*[ACM Transcation on Storage'20]** Pradeep Kumar, Howie Huang. _GraphOne: A Data Store for Real-time Analytics on Evolving Graphs._ ACM Transaction on Storage, Volume 15, Number 4, pp 1-40. January 2020. [[LINK](https://dl.acm.org/doi/abs/10.1145/3364180)][[Code](https://github.com/the-data-lab/GraphOne)].  
**\*[USENIX FAST'19]** Pradeep Kumar, Howie Huang. _GraphOne: A Data Store for Real-time Analytics on Evolving Graphs._ [Blog] [[PDF](https://www.usenix.org/system/files/fast19-kumar.pdf)] [[PPT](https://www.usenix.org/sites/default/files/conference/protected-files/fast19_slides_kumar.pdf)] [[Code](https://github.com/the-data-lab/GraphOne)]

GraphOne is the first-ever system that can perform a diverse set of analytics on the same data-store and replaces the current practice of deploying specialized systems for each type of analytics. The above two works propose the following contributions:
- **GraphView Abstraction:** Unification of Batch and Stream analytics from the same data-store under one system using Graph Views Abstraction: We have separated the graph ingestion from the graph analytics path. So, each analytics can focus on itself without worrying about concurrent data ingestion or any other analytics. So, there is only one global data-store, but many types of analytics can run on top of it. We are able to beat all the specialized graph systems, as well as their ingestion rates.
- **Data Visibility abstraction:** Fine-grained ingestion is always costly. So, GraphOne moves the cost of fine-grained ingestion from read-path to write path, implying that if your analytics are not required to be performed in fine-grained ingested data, you don't have to worry about additional costs associated with fine-grained ingestion. But if your analytics care for it, then only your analytics will pay the cost, not the others who don't need it. We then propose optimization to reduce this cost. This helps us to support a very high arrival rate of graph data at fine granularity but offers analytics performance at the cost of batched updates.
- **Concurrent Real-time Analytics:** Due to the separation of computation from data management, we are now able to run multiple analytics of the same or diverse types concurrently without copying the graph data, yes one copy of graph data, and multiple independent analytics.

**\*[SC'16]** Pradeep Kumar, Howie Huang. _G-Store: High-Performance Graph Store for Trillion-Edge Processing._ [Blog] [[PDF](https://pradeep-k.github.io/files/G-Store-SC16.pdf)] [[PPT](https://pradeep-k.github.io/files/G-Store-SC16-PPT.pdf)] [[Code](https://github.com/the-data-lab/gstore)]  
**[IEEE HPEC'17]** Yang Hu, Pradeep Kumar, Guy Swope (Raytheon), H. Howie Huang. _TriX: Triangle Counting at Extreme Scale._ [[PDF](https://pradeep-k.github.io/files/TriX-HPEC17.pdf)]  [[PPT](https://pradeep-k.github.io/files/TriX-HPEC17-ppt.pdf)] **Finalist, 2017 IEEE/Amazon/DARPA Graph Challenge**  

The above two works present graph computing with extreme scale. G-Store is the first ever system to demonstrate graph computing at a trillion-edge scale within a commodity server. Many techniques make this possible:  
- **SNB Format:** A new format that is space efficient (up to 8x space-saving, less disk IO) as well as hardware cache friendly (algorithmic metadata takes advantage of L2 caches).
- **Physical Grouping:** Algorithmic metadata takes advantage of LLC caching, while IO is converted to sequential. Double benefit.
- **Graph Caching:** G-Store is the first ever system to propose a graph-specific caching policy.
- **Slide-Cache-Rewind Scheduler:** Takes advantage of IO and compute overlap, as well as utilizing even the last drop of data available in the memory before throwing them away.

**\*[USENIX ATC'17]** Pradeep Kumar, Howie Huang. _Falcon: Scaling IO Performance in Multi-SSD Volumes._ [Blog] [[PDF](https://www.usenix.org/system/files/conference/atc17/atc17-kumar.pdf)] [[PPT](https://www.usenix.org/sites/default/files/conference/protected-files/atc17_slides_kumar.pdf)] [[Code](https://github.com/the-data-lab/falcon)]

Do you think that today's IO stack can deliver the raw performance if multiple SSDs are combined in a volume? The answer is no, because of the per-volume convention that is hard-coded in the IO stack. We have proposed the Falcon IO Stack which introduces a new convention of per-drive IO processing, that introduces a new layer in the IO stack to bring the best out of each drive that is part of the volume. Further, the Falcon IO Stack optimizes its merging, sorting, and dispatch process to make it future-ready, where we have shown that our new IO stack can saturate the newer NVMe Flash.

**[IEEE Big Data Congress'17]** Pradeep Kumar, Howie Huang. _SafeNVM: A Non-Volatile Memory Store with Thread-Level Page Protection._ [Blog] [[PDF](https://pradeep-k.github.io/files/SafeNVM.pdf)] [[PPT](https://pradeep-k.github.io/files/SafeNVM-ppt.pdf)] [Code]

Storing persistent data in NVM is not as safe against software-induced corruptions as it used to be if stored in disks. Do know why, and what will change if we store data in NVM instead of disk? This paper discusses the unknown safety conventions that are implicitly followed when data moves from DRAM to Disks. But that convention is broken due to the presence of NVM. Our techniques bring those conventions back to protect your persistent data in NVM from any software-induced corruption.

## Industry Experience

I have over 6 years of industry research and development experience in the broader Systems area. During my PhD, I interned in IBM Research at their storage research group. Before my PhD, I worked as a File System/Operating System kernel developer, and Distributed Systems Programmer for cluster-mode storage systems in NetApp Inc. at their Bangalore (India) research and development center. Before that, I worked at Huawei Technologies at their Bangalore, Shanghai, and Shenzhen center.

## Community Engagement and Services
- NSF Panelist, Computer and Network Systems Division, 2020-2023.
- PC Member, IPDPS'23, HPDC'23, ICDCS'21 ICDCS'22
- PC Member, IEEE TPDS Special Section on Parallel and Distributed Computing Techniques for AI, ML, and DL, 2020
- PC Member, IEEE 32nd International Symposium on Computer Architecture and High-Performance Computing (SBAC-PAD 2020)
- Workshop and Tutorial Co-Chair, IEEE ACSOS’20
- PC Member, Usenix HotEdge’20
- External Reviewer, Usenix FAST’20, OOPSLA'20
- Volunteer, NSF Aspiring CSR PIs Workshop, 2018
- Figured in Best Reviewers list based on peer feedback system, Shadow PC Eurosys’18
- Sub-reviewer in ICDCS’18, NAS’18, BDCAT’18
- Student Volunteer, ACM/IEEE SC’16

## Students
- Yidong Gong, Ph.D. Student since Summer, 2020
- Sarah Revillar, MS Thesis Student, Since Fall, 2022
- Saima Afrin, PhD Student Since Spring, 2023
- Arnab Tarafder, PhD Student Since Spring, 2023 

## Funding
- NSF CRII Award (Awarded in March 2023). Thank you, NSF.
- Summer Research Grant, William & Mary, 2020
- William & Mary Startup Grant

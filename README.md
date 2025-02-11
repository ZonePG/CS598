



# CS 598: Systems for Generative AI (F'24)

## Logistics
**Lectures**: 0216 Siebel Center for Computer Science, MW: 9:30 AM – 10:45 AM
| Member (NetID) | Role | Office Hours |
| :---------------- | :--- | :----------- |
| [Fan Lai](https://fanlai.me/) (fanlai) | Instructor | 3128 Siebel Center. M 11:00 AM – 12:00 PM
| [Chengsong Zhang](https://continue-revolution.github.io/) (cz81) | TA | [Zoom](https://illinois.zoom.us/j/83482246470?pwd=3qACwpab8h6qGgAtM6bIvOgu0JxzTC.1). W 07:00 PM - 08:00 PM

**Piazza**:  *ALL* communication regarding this course must be via [Piazza](https://piazza.com/illinois/fall2024/cs598fla). This includes questions, discussions, announcements, as well as private messages.

Presentation slides and paper summaries should be emailed to [cs598-aisys-staff@lists.cs.illinois.edu](mailto:cs598-aisys-staff@lists.cs.illinois.edu).

## Course Description
**Learning Objectives**: This course will introduce the key concepts and the state-of-the-art in practical, scalable, and fault-tolerant software systems for emerging Generative AI (GenAI). At the end of the course you will be able to: 

-   Critique and evaluate the design details of state-of-the-art GenAI systems
-   Develop and utilize tools to profile and understand the performance of GenAI systems
-   Propose new research ideas in topics related to support practical GenAI

**Structure**: The course will be a mix of lectures, student presentations, seminar-style discussions, and a semester-long project on GenAI topics.  We will cover GenAI topics from top conferences that take a systems view to the relevant challenges, including:  
- Basics of GenAI models from a systems perspective; 
- Systems for GenAI lifecycle (pre-training, training, fine-tuning/alignment, inference serving, and grounding); 
- GenAI for systems and etc. 

Note that this course is **NOT focused on AI methods**.  Instead, we will *focus on how one can build software systems* so that existing AI methods can be used in practice and new AI methods can emerge. 

**Prerequisites**:  Students are expected to have good programming skills and must have taken at least one undergraduate-level systems-related course (from operating systems, databases, distributed systems, or networking). Having an undergraduate ML/AI course is helpful but not required.

## Tentative Schedule and Reading List
*This is an evolving list and subject to changes due to the breakneck pace of GenAI innovations.*
| Date    | Readings                                                                                                             | Presenter                               | Companion                            | Reviewer                                   |
| ------- | -------------------------------------------------------------------------------------------------------------------- | --------------------------------------- | ------------------------------------- | ------------------------------------------- |
| Aug 26  | **Introduction**<br>[How to Read a Paper](http://svr-sk818-web.cl.cam.ac.uk/keshav/papers/07/paper-reading.pdf) (Required)<br>[How to Give a Bad Talk](http://www.cs.berkeley.edu/~pattrsn/talks/BadTalk.pdf) (Required)<br>[Writing Reviews for Systems Conferences](http://people.inf.ethz.ch/troscoe/pubs/review-writing.pdf)<br>[The Shift from Models to Compound AI Systems](https://bair.berkeley.edu/blog/2024/02/18/compound-ai-systems/) | [Fan](./Slides/fan-overview.pdf)        |                                       |                                           |
| Aug 28  | [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) (Required)<br>[FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness](https://papers.nips.cc/paper_files/paper/2022/hash/67d57c32e20fd0a7a302cb81d36e40d5-Abstract-Conference.html) (Required)<br>[Attention Is All You Need](https://dl.acm.org/doi/10.5555/3295222.3295349)<br>[The Transformer Family Version 2.0](https://lilianweng.github.io/posts/2023-01-27-the-transformer-family-v2/) | [Banruo, Yifan](./Slides/by-transformer.pptx) |                                       |                                           |
| Sept 4  | [The Illustrated Stable Diffusion](https://jalammar.github.io/illustrated-stable-diffusion/) (Required)<br>[VideoPoet: A Large Language Model for Zero-Shot Video Generation](https://arxiv.org/pdf/2312.14125) (Required)<br>[Scalable Diffusion Models with Transformers](https://arxiv.org/pdf/2212.09748) <br> [Hierarchical Text-Conditional Image Generation with CLIP Latents](https://arxiv.org/abs/2204.06125)| [Chengsong](https://docs.google.com/presentation/d/1B4LhD2ETpzsRU5nvbdEd9NyazjnuDm6VsQO_BrbKL1c/edit?usp=sharing) |                                       |                                           |
| Sept 9  | **No Lecture / Work on Project Proposal**<br>[Worse is Better](https://en.wikipedia.org/wiki/Worse_is_better) (Required)<br>[Hints and Principles for Computer System Design](https://arxiv.org/abs/2011.02455) |                                       |                                       |                                           |
| Sept 11 | [Multimodality and Large Multimodal Models (LMMs)](https://huyenchip.com/2023/10/10/multimodal.html) (Required)<br>[Visual Instruction Tuning](https://arxiv.org/abs/2304.08485)<br>[DeepSpeed-VisualChat: Multi-Round Multi-Image Interleave Chat via Multi-Modal Causal Attention](https://arxiv.org/abs/2309.14327)<br>[Flamingo: a Visual Language Model for Few-Shot Learning](https://proceedings.neurips.cc/paper_files/paper/2022/hash/960a172bc7fbf0177ccccbb411a7d800-Abstract-Conference.html) | [Ren, Zihan, Shuangliang](./Slides/ren-mlmm.pptx)                 | Gabriella, Han-Ting, Kai-Siang          |                   |
| Sept 16 | [Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer](https://openreview.net/forum?id=B1ckMDqlg) (Required)<br>[DeepSpeed-MoE: Advancing Mixture-of-Experts Inference and Training to Power Next-Generation AI Scale](https://arxiv.org/abs/2201.05596) (Required)<br>[Switch Transformers: Scaling to Trillion Parameter Models with Simple and Efficient Sparsity](https://dl.acm.org/doi/abs/10.5555/3586589.3586709)<br>[Scaling Vision-Language Models with Sparse Mixture of Experts](https://arxiv.org/abs/2303.07226) | [Akul, Aditi, Shraddhaa](./Slides/akul-moe.pptx)                    |                        | Ayush, Ritul, Shashwat                            |
|         |  **Pre-Training** |              |	|
| Sept 18 | [The Llama 3 Herd of Models](https://arxiv.org/abs/2407.21783) (Sec 1-4, Required)<br>[Gemini: A Family of Highly Capable Multimodal Models](https://arxiv.org/abs/2312.11805) | [Enguang, Steven](./Slides/enguang_steven_llama3.pptx)                         | Haocheng, Jackson, Ziqi                 | Saad, Andrew, Yuhang                      |
| Sept 23 | [Alpa: Automating Inter- and Intra-Operator Parallelism for Distributed Deep Learning](https://www.usenix.org/conference/osdi22/presentation/zheng-lianmin) (Required)<br>[Perseus: Removing Energy Bloat from Large Model Training](https://arxiv.org/abs/2312.06902) (Required)<br>[LightSeq: Sequence Level Parallelism for Distributed Training of Long Context Transformers](https://arxiv.org/abs/2310.03294) | [Jiahao, Xinyu, Zhiyu](./Slides/zhiyu-alpa.pdf)                  | Michael, Yikang, Nikhil                | Viswajith, Arijus     & Nicholas              |
| Sept 25 | [MegaScale: Scaling Large Language Model Training to More Than 10,000 GPUs](https://arxiv.org/abs/2402.15627) (Required)<br>[RDMA over Ethernet for Distributed AI Training at Meta Scale](https://dl.acm.org/doi/10.1145/3651890.3672233) (Required)<br>[GEMINI: Fast Failure Recovery in Distributed Training with In-Memory Checkpoints](https://www.cs.rice.edu/~eugeneng/papers/SOSP23.pdf) | [Jimmy, Yiming, Kartik](./Slides/jimmy-mega.pptx)                  | Saad, Andrew, Yuhang                   | Yueshen, Henry, Jianyuan          |
| Sept 30 | [ASTRA-sim2.0: Modeling Hierarchical Networks and Disaggregated Systems for Large-model Training at Scale](https://arxiv.org/pdf/2303.14006) (Required)<br>[LLMServingSim: A HW/SW Co-Simulation Infrastructure for LLM Inference Serving at Scale](https://arxiv.org/abs/2408.05499v1) (Required)<br>[Vidur: A Large-Scale Simulation Framework For LLM Inference](https://arxiv.org/abs/2405.05465) | [Kaizhuo](./Slides/kaizhuo-sim.pptx)                    | Akul, Aditi, Shraddhaa                  | Michael, Yikang, Nikhil                   |
| | **Alignment & Post-Training Optimization**               |	|
| Oct 2   | [LoRA: Low-Rank Adaptation of Large Language Models](https://openreview.net/forum?id=nZeVKeeFYf9) (Required)<br>[S-LoRA: Serving Thousands of Concurrent LoRA Adapters](https://arxiv.org/abs/2311.03285) (Required)<br>[Stylus: Automatic Adapter Selection for Diffusion Models](https://arxiv.org/abs/2404.18928) |   [Nicholas](./Slides/nick-lora.pdf)             |        Banruo, Yifan            | Muyan, Xin, Jiachen                      |
| Oct 7   | [LIMA: Less Is More for Alignment](https://arxiv.org/abs/2305.11206) (Required)<br>[Finetuned Language Models Are Zero-Shot Learners](https://openreview.net/forum?id=gEZrGCozdqR) (Required)<br>[Training Language Models to Follow Instructions with Human Feedback](https://proceedings.neurips.cc/paper_files/paper/2022/hash/b1efde53be364a73914f58805a001731-Abstract-Conference.html) | [Yueshen, Henry, Jianyuan](./Slides/lima.pdf)               | Kaizhuo                 | Jinwei, Yuxuan, Tengjun                  |
| Oct 9   | [LLM.int8(): 8-bit Matrix Multiplication for Transformers at Scale](https://arxiv.org/abs/2208.07339) (Required)<br>[AWQ: Activation-aware Weight Quantization for On-Device LLM Compression and Acceleration](https://arxiv.org/abs/2306.00978) (Required)<br>[GPTQ: Accurate Post-Training Quantization for Generative Pre-trained Transformers](https://arxiv.org/abs/2210.17323) | [Viswajith, Arijus](./Slides/quantization.pptx)               | Ren, Zihan, Shuangliang                | Jimmy, Yiming, Kartik                    |
|         |  **Grounding & Inference** |                 |	|
| Oct 14  | [REALM: Retrieval-Augmented Language Model Pre-Training](https://proceedings.mlr.press/v119/guu20a.html) (Required)<br>[CacheBlend: Fast Large Language Model Serving for RAG with Cached Knowledge Fusion](https://arxiv.org/abs/2405.16444) (Required)<br>[Improving Language Models by Retrieving from Trillions of Tokens](https://proceedings.mlr.press/v162/borgeaud22a.html) | [Saad, Andrew, Yuhang](./Slides/rag.pdf)                  | Muyan, Xin, Jiachen                   |      Jiahao, Xinyu, Zhiyu 
| Oct 16  | **No Lectures / Prep for the Midterm** |
| Oct 21  | **Mid-Semester Presentations** |                                       |                                       |                                           |
| Oct 23  | **Mid-Semester Presentations** |                                       |                                       |                                          |
| Oct 28  | [SpecInfer: Accelerating Large Language Model Serving with Tree-based Speculative Inference and Verification](https://arxiv.org/abs/2305.09781) (Required)<br>[PowerInfer: Fast Large Language Model Serving with a Consumer-grade GPU](https://arxiv.org/abs/2312.12456) (Required)<br>[MemGPT: Towards LLMs as Operating Systems](https://arxiv.org/abs/2310.08560) |      [Michael, Yikang, Nikhil](./Slides/SpecInfer.pptx)                | Jimmy, Yiming, Kartik                  | Haocheng, Jackson, Ziqi 
| Oct 30  | [Efficient Memory Management for Large Language Model Serving with PagedAttention](https://dl.acm.org/doi/10.1145/3600006.3613165) (Required)<br>[Taming Throughput-Latency Tradeoff in LLM Inference with Sarathi-Serve](https://arxiv.org/abs/2403.02310) (Required)<br>[SGLang: Efficient Execution of Structured Language Model Programs](https://arxiv.org/abs/2312.07104) | [Jinwei, Yuxuan, Tengjun](./Slides/vllm.pptx)                | Enguang, Steven  & Nicholas                         | Ren, Zihan, Shuangliang  & Kaizhuo                 |
| Nov 4   | [OMS-DPM: Optimizing the Model Schedule for Diffusion Probabilistic Models](https://arxiv.org/abs/2306.08860) (Required)<br>[Are More LM Calls All You Need? Towards the Scaling Properties of Compound AI Systems](https://arxiv.org/pdf/2403.02419) (Required)<br>[DistriFusion: Distributed Parallel Inference for High-Resolution Diffusion Models](https://arxiv.org/abs/2402.19481) | [Muyan, Xin, Jiachen](./Slides/compoundai.pptx)                   |   Jiahao, Xinyu, Zhiyu              | Gabriella, Han-Ting, Kai-Siang           |
|         | **ML for Systems** |                         |	| 
| Nov 6  | [NetLLM: Adapting Large Language Models for Networking](https://arxiv.org/abs/2402.02338) (Required)<br>[Talk like a Graph: Encoding Graphs for Large Language Models](https://arxiv.org/abs/2310.04560) (Required)<br>[LLM-ABR: Designing Adaptive Bitrate Algorithms via Large Language Models](https://arxiv.org/pdf/2404.01617) | [Gabriella, Han-Ting, Kai-Siang](./Slides/netllm.pptx)         | Ayush, Ritul, Shashwat                        | Enguang, Steven & Banruo, Yifan                             |
| Nov 11  | [Parrot: Efficient Serving of LLM-based Applications with Semantic Variable](https://arxiv.org/pdf/2405.19888) (Required)<br>[FLASH: Fast Model Adaptation in ML-Centric Cloud Platforms](https://haoran-qiu.com/pdf/flash.pdf) (Required)<br>[Adapting Foundation Models for Operator Data Analytics](https://conferences.sigcomm.org/hotnets/2023/papers/hotnets23_kotaru.pdf) | Haocheng, Jackson, Ziqi               | Viswajith, Arijus               | Yueshen, Henry, Jianyuan                  |
| Nov 13  | **No Lecture: Recalibrate Projects** |                                       |                                       |                                           |
| Nov 18  | [Extracting Training Data from Large Language Models](https://www.usenix.org/conference/usenixsecurity21/presentation/carlini-extracting) (Required)<br>[Extracting Training Data from Diffusion Models](https://www.usenix.org/conference/usenixsecurity23/presentation/carlini) (Required)<br>[Identifying and Mitigating the Security Risks of Generative AI](https://arxiv.org/abs/2308.14840) | Ayush, Ritul, Shashwat                        | Jinwei, Yuxuan, Tengjun                | Akul, Aditi, Shraddhaa                    |
| Nov 20   | **No Class: Prep for Final Presentation**<br>[How to Write a Great Research Paper](https://www.microsoft.com/en-us/research/academic-program/write-great-research-paper/) (Required) |                                       |                                       |                                           |
| Dec 2   | **Final Presentations**<br> |     
| Dec 4   | **Final Presentations**<br> |                                       |                                       |                                           |
| Dec 7   | **No Class: Prep for Project Report** |                                       |                                       |                                           |
 
 ## Tentative Grading
**Groups**:  All activities of this course, except your own participation :), will be performed in groups of 3 students. Form a group of 3 members and [declare your group's membership and paper preferences](https://forms.gle/xeZ49ytNtRUmWygL8) by **Sept 5**. After this date, we will form groups from the remaining students.

|                         | Weight | 
| ------------------------| ------:| 
| [Participation](#required-reading)           | 10%    | 
| [Paper Presentation](#student-lectures) & [Discussion](#post-presentation_panel_discussion)     | 15%    | 
| [Paper Summary](#lecture-summaries)           | 15%    | 
| [Project Report](#project)          | 40%    | 
| [Project Presentations](#project)   | 20%    |

**Academic integrity**: [The University's Honor Code](https://siebelschool.illinois.edu/academics/honor-code) applies to all activities related to this course. All material you submit in this course (reading responses, project reports, and presentation materials) must be your own. If you use someone else’s material, you must cite them properly. 

**AI Tool Policy**: AI tools may be used for grammar checking and refining initial brainstorms, but the final reviews and codes **must** be authored by the student. Students are responsible for the entire content and must adhere to the Academic Integrity Policy.

## Policies

### Participation
**Before Each Lecture**: Each lecture will include one or two required reading that everyone must read.   There will be *optional related reading(s)* that only the presenter(s) should be familiar with. They are optional for the rest of the class.  You are required to [submit](https://forms.gle/WNvTkRmodapagD6d7) **one insightful question** for each presented papers before each lecture. 

**During Lectures**: Active participation is crucial for both your own understanding and to improve the overall quality of the course. You are expected to attend **all** lectures (up to 2 absences allowed for legitimate reasons), and more importantly, participate in class discussions. Not everyone must have add something every day, but it is expected that everyone has something to share over the semester.

**After Lectures**: Participation also involves contributing to discussions on Piazza. The group responsible for the summary should initiate the (remaining) discussion, and the rest of the members are encouraged to participate.

### Student Lectures
The course will be conducted as a seminar. Only one group will present in each class. Each group will be assigned *at least one lecture* over the course of the semester. Presentations should last **at most 40 minutes** without interruption.
However, presenters should expect questions and interruptions throughout. 

In the presentation, you should:

* Provide a brief background to motivate the problem (e.g., simplifying this by referencing previous talks)
* Present the high level idea, approach, and/or insight (using examples, whenever appropriate) in the required reading. 
* Discuss technical details so that one can understand key details without carefully reading (quickly skim the evaluations).
* Explain the differences between related works as well as the additional reading.
* Identify strengths and weaknesses of the required reading and propose directions of future research.

*The slides for a presentation must be emailed to the instructor team (in \*.pptx format) at least 24 hours prior to the corresponding class.* 

### Post-Presentation Panel Discussion 
To foster a deeper understanding of the papers and encourage critical thinking, each lecture will be followed by a panel discussion. This discussion will involve three distinct roles played by different student groups, simulating an interactive and dynamic scholarly exchange.

#### Roles and Responsibilities

1. **The Authors**
- Group Assignment: The 'Companion' group will write the summary and play the role of the paper's authors.
- Responsibility: As authors, you are expected to defend your paper against critiques, answer questions, and discuss how you might improve or extend your research in the future, akin to writing a rebuttal during the peer-review process.


2. **The Reviewers**
- Group Assignment: The 'Reviewer' group will write the summary and will be assigned to one slot to play the role of reviewers.
- Responsibility: Reviewers critically assess the paper, posing challenging questions and highlighting potential weaknesses or areas for further investigation. 
Your goal is to engage in a constructive critique of the paper, simulating a peer review scenario.

 
3. **Rest of the Class** (including the presenters)
- Responsibility: During the panel discussions, feel free to actively **ask questions** and engage in the dialogue. 


### Lecture Summaries
Each group will also be assigned to **write summaries for roughly two lectures**: one in the 'Companion' role and the other in the 'Reviewer' role.
The summary assigned to a group will not be the reading they gave the lecture on.

A paper summary must address the following four questions in sufficient details (2-3 pages):

* What is the problem addressed in the lecture, and why is this problem important?
* What is the state of related works in this topic?
* What is the proposed solution, and what key insight guides their solution?
* What is one (or more) drawback or limitation of the proposal?
* What are potential directions for future research?

**Late reviews will not be counted.** *The paper summary of a paper must be emailed to the instructor team within 24 hours after its presentation.*  

You should use [this format](Summaries/Template.pdf) for writing your summary. Use Google doc to enable in-line comments and suggestions.

*Allocate enough time for your reading, discuss as a group, write the summary carefully, and finally, include key observations from the class discussion.*

### Project
You will have to complete substantive work an instructor-approved problem and have original contribution. Surveys are not permitted as projects; instead, each project must contain a survey of background and related work.

You must meet the following milestones (unless otherwise specified in future announcements) to ensure a high-quality project at the end of the semester:

* Turn in a 2-page draft proposal ([template](https://www.overleaf.com/read/bsrcbphcvyzc#d075e8)), plus as many pages as needed for references, by **September 26**. Remember to include the names and UIUC email addresses of the group members. 
* Each group must present mid-semester progress during class hours on **October 21 and October 23**.
* Each group must turn in an 8-page final report and your code via email **on or before 6:00PM CST on December 19.** The report must be submitted as a PDF file, with formatting similar to that of the papers you've read in the class. The self-contained (i.e., include ALL dependencies) code must be submitted as a zip file. Each zip file containing the code must include a README file with a step-by-step guide on how to compile and run the provided code.
* You can find how to access GPU resources [here](./Resources/cloudlab.md)

### **Acknowledgements**
This course is heavily inspired by other excellent system seminar courses, particularly [UMich CSE 585](https://github.com/mosharaf/eecs598/tree/w24-genai). Acknowledgments to [SymbioticLab](https://symbioticlab.org/).	

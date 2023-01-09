# ST2023
SIGTYP Shared Task 2023
Task Description
=================
Cognates are etymologically related word pairs across languages which may or may not have similar spelling, pronunciation and meaning. Cognates can be traced back to a single ancestral word form in a common earlier language stage. On the other hand, derivatives are words which have been derived directly from another word form or root, including both words inherited from an earlier stage of the same language and words borrowed from distinct languages. Cognates have been studied in various fields of linguistics with different purposes. In historical linguistics, cognates are useful in the reconstruction of proto-languages and can aid in establishing the relationship between languages; in lexicography, cognates are helpful in the development of multilingual dictionaries. Moreover, in recent years, NLP researchers have shown interest in using cognates to enhance the performance of multilingual tasks such as machine translation, lexical induction, word embeddings and many more.

As there has been little work on automatic cognate identification, it is still a challenging task, especially for less-resourced languages. Supervised identification of cognates and derivatives is expensive as we need more linguistic information and annotation; at the same time, finding linguists and annotators for less-resourced languages is impractical. Thus we propose a shared task which aims to provide a new benchmark for differentiating between cognates and derivatives and introduce new unsupervised approaches for cognate and derivative detection in less-resourced languages. 

Sub-tasks
===========
The tasks are multiclass classification tasks which require that the relationship between pairs of words be identified as either a cognate relationship, a derivative relationship, or no relationship.<br>
a. Supervised: Cognate and Derivative Detection <br>
b. Unsupervised: Cognate and Derivative Detection <br>

Data
======
We will provide 232,482 annotated word pairs in 34 languages, including both high-resourced and less-resourced languages. Each word pair is annotated with a language for each word, and with one of the three categories based on the relationship between the pair; cognate, derivative or none. This data was collected and annotated using wiktionary. <br>
In addition to this, the shared task allows participants to use external resources as long as they are openly available and can be, in theory, used by other participants for research purposes. In case participants decide to use external resources and data in their system they should use proper citation and provide the details of the dataset in the system description.

Data Formant:

| Word_1 | LId_1 |  Word_2 |  LId_2 | Labels |
| ------ | ----- | ------- | ------ | ------ |
| Yannick | en |  Yannig |  br | der         |
| creta | ca |  creta |  la | der            |
| luminescens | nn |  lumen |  la | der      |
| admonester | fr |  admoneō |  la | der|
| gnit | en |  gnit |  is | cog|
| roh | de |  raw |  en | cog|
| duodecimate | en |  duodecimatus |  la | der|
| coherent | en |  cohaērēns |  la | der|
| corpulent | en |  corpulentus |  la | der|
| prosperitat | ca |  prosperitās |  la | der|
| hélas | fr |  helaas |  nl | cog|
| mi | en |  mă |  ro | cog|
| phillumenism | en |  lumen |  la | der|

Evaluation Procedure
=======================
The standard evaluation metrics for evaluating and ranking the teams will be macro-averaged F1 scores for supervised classification. For unsupervised methods, we will follow the standard cluster performance evaluation process. The number of clusters will be same as the number of original classes and evaluated with the cluster accuracy using
			$$ Acc \eq (max_m \sum_{i=1}^n 1 (l_i=m (c_i))  \over n ) $$
$$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$
   Acc=  

$${max_m{\left( \sum_{i=1}^n \right) 1 \left( {l_i=m (c_i)} \right)} \over n}$$
where $l_i$ is the ground truth label, $c_i$ is the cluster assignment produced by the algorithm and $m$ ranges over all possible one-to-one mappings between clusters and labels.

Dates
=========
Training data Release: 9 January 2023 <br>
Test data Release: 24 February 2023 <br>
Submissions Due: 10 March 2023 <br>
Notification: 20 March 2023 <br>
Camera-ready Due: 27 March 2023 <br>
Workshop: May 2 or 6 2023 <br>

Submission
==================
Submissions should be emailed to the organizers by the end of the (Date) anywhere in the world. Submissions should follow the format of the training label files, with tab-separated file word pairs, LIds and Labels.
Files should be named as {team name}_{unsupervised/supervised} to indicate the subtask. 


Description Paper
==================
Paper submission instructions will be the same as for the workshop. Each team participating in the shared task is expected to submit a paper of 4 to 8 pages, plus additional pages for references, formatted according to the workshop guidelines. The paper should describe the system and the resources used along with the libraries used to develop the system. The methodology/strategy should be documented in such a way that the readers and other researchers are able to replicate the work from the system description in the paper. 

Important Links
==================
In order to register for the Shared Task, please fill out the form given in the link below.<br>
[Registration](https://docs.google.com/forms/d/e/1FAIpQLSd8cPggOcbDvDnbzkyNUJgBw-c1EjOMmiuq7VkCx1zUfSuGOA/viewform?usp=sf_link)

List of Task Organizers
================
Priya Rani, PhD Student, SFI  Centre for Research and Training in AI, Data Science Institute, University of Galway <br>
Koustava Goswami, Adobe Research, Bangalore, India; Former PhD Student, Insight SFI Research Centre for Data Analytics, Data Science Institute, University of Galway <br>
Adrian Doyle,  Research associate, Insight SFI Research Centre for Data Analytic, Data Science Institute, University of Galway <br>
Bernardo Stearns, Research associate, Insight SFI Research Centre for Data Analytic, Data Science Institute, University of Galway <br>
Theodorus Fransen, Postdoctoral Researcher, Insight SFI Research Centre for Data Analytics, Data Science Institute, University of Galway <br>
John P. McCrae, Assistant Professor, Insight SFI Research Centre for Data Analytics, Data Science Institute, University of Galway

Contact Details
================
If you have any queries please contact us on 
priya.rani@insight-centre.org




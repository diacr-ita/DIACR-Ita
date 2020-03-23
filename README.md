## Welcome to the DIACR-Ita task!

## Menu

- [Task Description](#task-description)
- [Data Description](#data-description)
- [Guidelines](#guidelines)
- [References](#references)
- [Important Dates](#important-dates)
- [Organizers](#organizers)


DIACR-Ita is the first task on lexical semantic change for Italian, combining together computational and historical linguistics. The task challenges participants to develop systems that can automatically detect if a given word has changed its meaning over time, given contextual information from corpora.

It is a well known fact that word meanings can evolve in different ways. They can undergo pejoration or amelioration (when
meanings become respectively more negative or more positive) or they can be object of broadening (also referred to as generalization or extension) or narrowing (also known as restriction or specialization). For instance, the Italian word "portamento" (gait) which has underwent a narrowing of the meaning, loosing the action meaning (i.e., the act of bearing) (Grossmann & Reiner (eds), 2004). Semantic changes can be further classified based on the cognitive process they result from, i.e. either from metonymy or metaphor. Lastly, it is possible to distinguish among changes due to language-internal factors or to language-external ones (Hollmann, 2009). 

In recent years, there has been a significant increase of interest in lexical semantic change detection. Many are the existing approaches, data used, and evaluation strategies to detect semantic drift. Most of the approaches rely on diachronic word embeddings, some of these created as post-processing of static word embedding, such as Hamilton et al. (2016), while others create dynamic word embeddings, where vectors share the same space for all time periods (Del Tredici et al., 2016; Yao et al., 2018; Rudolph and Blei, 2018; Dubossarsky et al., 2019). Finally, recent work exploits word sense induction algorithms to discover semantic shifts (Tahmasebi and Risse, 2017; Hu et al., 2019). A more complete state of the art is described in a critically and concise way in the latest surveys (Tahmasebi et al., 2018; Kutuzov et al., 2018; Tang, 2018). The large majority of the methods use English as the target language for the diachronic analysis, while other languages remain under-explored. To date, only one evaluation has been carried out on the Italian language using the Kronos-it dataset (Basile et al., 2019).

DIACR-Ita is a twin task of the the Semeval 2020 Task 1: Unsupervised Lexical Semantic Change Detection (https://competitions.codalab.org/competitions/20948) that  will host for the first time a task on unsupervised lexical semantic change detection.

## Task Description
The goal of the task is to establish if a set of words (target words) change their meaning across two periods, t1 and t2, where t1 precedes t2.
Following the SemEval 2020 Task 1 setting, we rely on the comparison of two time periods. In this way we tackle two issues: 1) we reduce the number of time periods for which data has to be annotated; 2) we reduces the task complexity, allowing different model architectures to be applied to it, widening the range of possible participants.
Participants will be provided with two corpora C1 and C2 (for time periods t1 and t2, respectively), and a set of target words. For each of them, systems have to decide whether a word changed or not its meaning between t1 and t2 according to the occurrences of target word(s) in sentences in C1 and C2. For instance, the meaning of the word “imbarcata” is known to have expanded (i.e, it has acquired a new sense) from t1 to t2 (originally it refers to an acrobatic manoeuvre of aeroplanes, but nowadays it is also used to refer to the state of being deeply in love with someone.) This will be reflected in different occurrences of use in sentences between C1 and C2.
The task is formulated as a closed task (i.e., participants must train their models on the data that are provided).

## Guidelines
<a href="username.github.io/folder/EVALITA_2020___DIACR_ita___Guidelines-2.pdf" target="_blank">Guidelines</a>


### References


Pierpaolo Basile, Giovanni Semeraro, and Annalina Caputo. 2019. Kronos-it: A dataset for the Italian semantic change detection task. In CEUR Workshop Proceedings, volume 2481.

Marco Del Tredici, Malvina Nissim, and Andrea Zaninello. 2016. Tracing metaphors in time through self-distance in vector spaces. In CEUR Workshop Proceedings. 3rd Italian Conference on Computational Linguistics, CLiC- it 2016 and 5th Evaluation Campaign of Natural Language Processing and Speech Tools for Italian, EVALITA 2016 ; Conference date: 05-12-2016 Through 07-12-2016.

Haim Dubossarsky, Simon Hengchen, Nina Tahmasebi, and Dominik Schlechtweg. 2019. Time-Out: Temporal Referencing for Robust Modeling of Lexical Semantic Change. In 57th Annual Meeting of the Association for Computational Linguistics, pages 457–470. Association for Computational Linguistics (ACL), sep.

Maria Grossmann, Franz Rainer (Ed.). La formazione delle parole in italiano. Berlin, Boston: De Gruyter, 2013. Web. Retrieved 10 Mar. 2020, from https://www-degruyter-com.proxy-ub.rug.nl/view/product/25447

William L. Hamilton, Jure Leskovec, and Dan Jurafsky. 2016. Diachronie word embeddings reveal statistical laws of semantic change. In 54th Annual Meeting of the Association for Computational Linguistics, ACL 2016 - Long Papers, volume 3, pages 1489–1501, may.

Willem Hollmann. 2009. Semantic change. In English Language: Description, Variation and Context, pages 301–313. Basingstoke: Palgrave.

Renfen Hu, Shen Li, and Shichen Liang. 2019. Diachronic Sense Modeling with Deep Contextualized Word Embeddings: An Ecological View. In 57th Annual Meeting of the Association for Computational Linguistics, pages 3899–3908.

Andrey Kutuzov, Lilja Øvrelid, Terrence Szymanski, and Erik Velldal. 2018. Diachronic word embeddings and semantic shifts: a survey. 27th International Conference on Computational Linguistics.

Maja Rudolph and David Blei. 2018. Dynamic Embeddings for Language Evolution. In WWW ’18: Proceedings of the 2018 World Wide Web Conference, pages 1003–1011. Association for Computing Machinery (ACM).

Dominik Schlechtweg, Sabine Schulte im Walde, and Stefanie Eckmann. 2018. Diachronic usage relatedness (DURel): A framework for the annotation of lexical semantic change. In Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technolo- gies, Volume 2 (Short Papers), pages 169–174, New Orleans, Louisiana, June. Association for Computational Linguistics.

Nina Tahmasebi and Thomas Risse. 2017. Finding IndividualWord Sense Changes and their Delay in Appearance. In International Conference Recent Advances in Natural Language Processing, pages 741–749. Assoc. for Computational Linguistics Bulgaria, nov.

Nina Tahmasebi, Lars Borin, and Adam Jatowt. 2018. Survey of Computational Approaches to Lexical Semantic Change. 1st International Workshop on Computational Approaches to Historical Language Change 2019.

Xuri Tang. 2018. A state-of-the-art of semantic change computation. Natural Language Engineering, 24(5):649– 676, sep.
Elizabeth Closs Traugott. 2006. Semantic change: Bleaching, strengthening, narrowing, extension. In Encyclope- dia of Language and Linguistics. Elsevier.

Zijun Yao, Yifan Sun, Weicong Ding, Nikhil Rao, and Hui Xiong. 2018. Dynamic word embeddings for evolving semantic discovery. In WSDM 2018 - Proceedings of the 11th ACM International Conference on Web Search and Data Mining, volume 2018-Febua, pages 673–681.

## Important Dates

- **29th May 2020**: distribution of data sets for training and development
- **4th September 2020**: distribution of datasets for testing
- **4th - 24th September 2020**: evaluation windows and collection of participants results
- **2nd October 2020**: assessment returned to participants
- **tbd**: report due from participants
- **30th November – 3rd December 2020**: [EVALITA 2020](http://www.evalita.it/) (co-located with CLiC-it 2020)


## Organizers
- Pierpaolo Basile - Università di Bari "A. Moro"
- Tommaso Caselli - Rijksuniveristeit Gronigen
- Annalina Caputo - Dublin City University
- Rossella Varvara - Università di Firenze
- Pierluigi Cassotti - Università di Bari "A. Moro"

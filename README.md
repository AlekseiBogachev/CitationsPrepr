# CitationsPrepr
The repository was created for my future employers.  
This project shows using of regular expressions.  
All valuable or confidential data has been deleted.

There are three Jupyter Notebooks used for the pre-processing of citations for a scientific report.

The input data taken from ieeexplore.ieee.org is citations in the bibtex format. The citations is collected in the file "all_article.bib". This file is similar to the example below, but is significantly longer. It contains 7000+ citations.

@INPROCEEDINGS{9535699,
  author={Krylov, Vladimir and Bogachev, Aleksei},
  booktitle={2021 23rd International Conference on Digital Signal Processing and its Applications (DSPA)}, 
  title={Digital Signal Processing of Capacitance Transients of Semiconductor Devices and Integrated Circuits}, 
  year={2021},
  volume={},
  number={},
  pages={1-4},
  keywords={}
  doi={10.1109/DSPA51283.2021.9535699}}  
@INPROCEEDINGS{9535805,
  author={Alimuradov, Alan K.},
  booktitle={2021 23rd International Conference on Digital Signal Processing and its Applications (DSPA)}, 
  title={Enhancement of Speech Signal Segmentation Using Teager Energy Operator}, 
  year={2021},
  volume={},
  number={},
  pages={1-7},
  keywords={}
  doi={10.1109/DSPA51283.2021.9535805}}


Jupyter Notebooks:

Сollaborators.ipynb - After data cleaning and preparation, it reads key pharases from the file "a_keys.txt", then select entries containing these key phrases from the file "all_article.bib". Then, it makes adjacency list with pairs of coatuthors and number of their common publications. The list is used to create graphs and further analytics.

KeyWords.ipynb - It collects key phrases from "all_article.bib", counts their number in this file, selects key phrases that are longer than one word and occur more than four times, and puts the results into a file "keycounter(key length more than 1 and number more than 4 and sorted keys).csv"

articlesfinder.ipynb - It finds citations with keywords defined in the file "keys.txt" among input data ("all_article.bib") and puts them in the file "articles_for_references.bib". There is a special field for keywords, so there is no need to use complicated techniques to detect them. The "articles_for_references.bib" served as raw data for refrences in laTeX project, so it is not utilized in the previous notebooks.

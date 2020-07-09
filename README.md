# Analysis of readability and structural accuracy in SNOMED CT - Supplemetary material

This repository contains the supplementary material for the article ***Analysis of readability and structural accuracy in SNOMED CT***. The files are described next.

## Additional file 1 --- snomed\_history\_metrics.tsv
Tabular file containing the value of all metrics along all the SNOMED CT versions considered in the article. The file contains the following columns:

* **File**: The ontology file in which the metric is calculated. The name of the files is in the format YYYYMMDD (year, month and day), indicating the SNOMED CT version.
* **Metric**: The name of the metric.
* **Value**: The metric value for the corresponding SNOMED CT version.
    
## Additional file 2 --- detailed\_files\_snomed2019
Folder containing an individual tabular file per metric applied to SNOMED CT 20190731. Each file contains concrete information for each metric. In the case of readability metrics, the columns are the following:

* **Metric**: Metric name.
* **Entity**: The individual entity that is measured by the metric. Depending on the metric, this column will be named "Class", "Object property", "Data Property", or "Annotation Property".
* **Metric Value**: The individual metric value for the entity.
* **Hierarchy**: The SNOMED CT hierarchy in which the entity is located. This value is only present if the entity is a class.

     
In the case of structural accuracy metrics, the columns are the following:

* **Metric**: Metric name.
* **Class**: The LR class that is measured.
* **Class depth**: The depth in which the LR class is located in the ontology.
* **LR**: The label of the LR class, which is a lexical regularity.
* **Positive Cases**: Number of positive cases. If metric is "Lexically suggest logically define", the value of this column is the number of classes exhibiting *LR* in their labels that are semantically related to *Class*. If metric is "Systematic naming", positive cases are the number of subclasses of *Class* that exhibit *LR*.
* **Positive cases average depth**: The average depth in which the positive cases are located in the ontology.
* **Positive cases average distance to LR class**: The average hierarchical distance from positive cases to *Class*.
* **Negative Cases**: Number of negative cases. If metric is "Lexically suggest logically define", the value of this column is the number of classes exhibiting *LR* in their labels that are not semantically related to *Class*. If metric is "Systematic naming", positive cases are the number of subclasses of *Class* that do not exhibit *LR*.
* **Negative cases average depth**: The average depth in which the negative cases are located in the ontology.
* **Negative cases average distance to LR class**: The average hierarchical distance from negative cases to *Class*.
* **Metric Value**: The individual metric value for the LR class according the formula $\frac{Positive Cases}{Positive Cases + NegativeCases}$.
* **Hierarchy**: The SNOMED CT hierarchy in which the class is located.
     
## Additional file 3 --- snomed\_last\_version\_lsld.log
Log file including information of the negative cases detected in SNOMED CT 20190731 according to LSLD metric.
    
## Additional file 4 --- snomed\_last\_version\_systematic\_naming.log
Log file including information of the negative cases detected in SNOMED CT 20190731 according to systematic naming metric.
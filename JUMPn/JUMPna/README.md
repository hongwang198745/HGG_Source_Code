# HGG_Source_Code_PI3K-AKT pathway activiy.

The Purpose of the code is to compute PI3K-AKT pathway activity in different samples, termed as a (P), based on the altered phosphoproteins with annotated functional phosphosites: 
				a(P) = ?_(i=1)^k�?Ci*Fi/vk? 
In which K is the number of proteins with different activity relative to normal cortex samples, only PI3K-AKT pathway proteins with annotated functional phosphosites changes were accepted; Fi is the averaged log2 fold change of DE phosphosites in proteini; Ci is the functional annotation of the phosphorylation events from PhosphoSitePlus database. If the phosphorylation at a specific residue is reported to play a positive role in tumorigenesis, Ci is +1; if a negative role, Ci is -1, phosphosites with conflict functional annotations in the database were not considered in the analysis. Bootstrap was performed with 10,000 replications to determine statistical significance: 22 PI3K-AKT pathway Fi values were simulated by drawing from the Fi values of all quantified phosphoryaltion events, Ci annotations were feeded to each of these simulated data points to calculate a (P). This process was repeated 10,000 times. Finally P value were calculated as the sum(a(P) > 1.45) /10,000.
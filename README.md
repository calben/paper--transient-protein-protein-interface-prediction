# Transient protein-protein interface prediction: datasets, features, algorithms, and the RAD-T predictor

Keywords:
Machine learning; Protein-protein interaction; Protein-protein interface; Feature selection; Protein datasets; Protein interface identification; Protein prediction scoring


## Paper Abstract

### Background

Transient protein-protein interactions (PPIs), which underly most biological processes, are a prime target for therapeutic development. Immense progress has been made towards computational prediction of PPIs using methods such as protein docking and sequence analysis. However, docking generally requires high resolution structures of both of the binding partners and sequence analysis requires that a significant number of recurrent patterns exist for the identification of a potential binding site. Researchers have turned to machine learning to overcome some of the other methods’ restrictions by generalising interface sites with sets of descriptive features. Best practices for dataset generation, features, and learning algorithms have not yet been identified or agreed upon, and an analysis of the overall efficacy of machine learning based PPI predictors is due, in order to highlight potential areas for improvement.

### Results

The presence of unknown interaction sites as a result of limited knowledge about protein interactions in the testing set dramatically reduces prediction accuracy. Greater accuracy in labelling the data by enforcing higher interface site rates per domain resulted in an average 44% improvement across multiple machine learning algorithms. A set of 10 biologically unrelated proteins that were consistently predicted on with high accuracy emerged through our analysis. We identify seven features with the most predictive power over multiple datasets and machine learning algorithms. Through our analysis, we created a new predictor, RAD-T, that outperforms existing non-structurally specializing machine learning protein interface predictors, with an average 59% increase in MCC score on a dataset with a high number of interactions.

### Conclusion

Current methods of evaluating machine-learning based PPI predictors tend to undervalue their performance, which may be artificially decreased by the presence of un-identified interaction sites. Changes to predictors’ training sets will be integral to the future progress of interface prediction by machine learning methods. We reveal the need for a larger test set of well studied proteins or domain-specific scoring algorithms to compensate for poor interaction site identification on proteins in general.




## Paper Conclusion

Our results show that the most useful features for machine learning protein interaction site prediction are, in order, relSESA, solvation energy, density, electrostatic potential, conservation, rate shift, and disorder, as found by feature selection across a variety of machine learning algorithms on our datasets. Relative solvent excluded surface area and solvation energy were also critical features when buried residues were excluded from the dataset (data not shown), indicating that the role of relSESA lies beyond its ability to distinguish buried and exposed residues. We found that optimisation of machine learning algorithms and feature selection produced significantly better results than their unoptimised counterparts. However, these differences are overshadowed by the change resulting from varying restrictions on labelling accuracy. Improvements to dataset labelling led to better predictions by most algorithms tested regardless of whether an optimal feature set is used. Therefore, labelling accuracy in machine learning testing sets needs to be better addressed. As such, previous machine learning predictors may perform much better than their original results suggest.

Through iterative removal we identified those proteins that scored worst, middling, and best. We believe that this method can be an important tool to better understand what makes a protein’s interaction sites highly predictable. In cases of neither obviously poor labelling accuracy nor odd structure, it remains unclear what makes a protein interface highly predictable or unpredictable. Surprisingly, the top 10 scoring proteins in our training set scored almost as well when trained with the noise of the poorly labelled proteins as they did when trained with a better labelled training set.

There are existing ways to specialise training sets, most popularly by using training proteins with high structural similarity to the given testing protein. In our study, the best performing training set that does not use the query protein as a training instance was this set of 10 proteins with low structural identity.

We believe in order for MLPIP to make further progress, future focus will need to be directed towards training set generation and specialisation, and the search for larger testing sets with fully identified interface sites for more reliable scoring and significance tests. We also believe that MLPIP, frequently compared to the more specialised and more easily scored docking, may be undervalued due to poor scores by misinterpreting hidden interface sites.

Using our conclusions and experiments to optimise the training set, feature set, and machine learning algorithm, we created a prediction program that scores substantially higher than previous non-structurally specialising machine learning predictors, with an average increase in score of 59% as compared to five other leading predictors. We expect continued improvement upon the acquisition of more proteins in the PDB both for more training instances and a better labelled testing set, as well as upon the application of specialised training sets for each query protein.

Many areas of extraordinary complexity remain difficult to address by MLPIP, such as the timing, knowledge of physiological conditions, and biochemical modifications of proteins, with regards to their effect on interactions. We wish to explore methods of modelling these phenomena as well as exploring protein interaction networks and putative interactions for use in extending the versatility of future PPI predictors.

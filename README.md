## ComplexMatrixComb: Predicting DrugCombination Doses for IC<sub>50</sub> Using Complex Numbers and Matrix Factorization

This is the original codebase for the **ComplexMatrixComb**. Finding the exact drug concentrations needed to stop cancer cells from growing is a tough and expensive problem in cancer research, particularly when you're looking at drug combinations and have to test tons of different dose pairs. Current computer models mostly predict if drugs work well together or categorize their interactions. What they don't usually do is solve the opposite problem: telling us which specific concentration pairs will produce a desired level of inhibition. That's where ComplexMatrixComb comes in. It's a new method that uses **complex numbers** to model how pairs of drugs interact with different cell lines. By representing each drug's concentration as either the real or imaginary part of a complex number, the model can understand the full dose-response relationship. This allows ComplexMatrixComb to accurately predict the concentrations needed to reach **half-maximum inhibition (IC<sub>50</sub>)**. 

We've thoroughly tested ComplexMatrixComb using three well-known datasets: **O'Neil**, **NCI-ALMANAC**, and **AZ-Dream**. Our evaluations clearly show the efficiency and generalizability of our model across these diverse datasets. We've also performed extensive evaluations to prove our method's utility.


## Datasets

This section details the datasets used in our evaluations, all of which are publicly available. To ensure a fair comparison with methods like ComboFM, we utilized the preprocessing R scripts and instructions provided in their work, accessible via this [link](https://github.com/aalto-ics-kepaco/comboFM). For evaluating our matrix factorization method against alternative models such as ElasticNet, we used the data preprocessed by the aforementioned process. Further details on these procedures can be found in our paper.


## Codebase

This section outlines the code implemented to demonstrate the effectiveness of our model.

* `Astra.ipynb`, `NCI.ipynb`, and `O'neil.ipynb` contain the code for data preprocessing and applying our method to the respective benchmark datasets.
* `Invariance_to_Drug_Pair_Ordering.ipynb` includes the code and experiments demonstrating our method's robustness to the interchange of real and imaginary components in complex numbers.
* `Alternative_Models.ipynb` presents experiments showcasing the robustness and superiority of our method over existing machine learning approaches.

<!-- ## Datasets:
This section containts the datasets used in our evaluations. it is worth noting that all of these datasets are publicly available. it is worth noting that for comparing our work to other methods such as ComboFM we have used the preprocessing r scripts that they have used in their work and followed their instructions which can be found in the following [link](https://github.com/aalto-ics-kepaco/comboFM). also, for comparing our matrix factorization method with alternative models such as ElasticNet we have used the preprocessed data made by previous process. more details on these parts can be found on the paper. 

## Codes: 
This section contains the codes that we have implemented to show the effectiveness of our model. 
> The Astra.ipynb, NCI.ipynb and O'neil.ipynb contains the codes for the preprocess and applying our method on the benchmarks.  
> the invaraicane to Drug Pair Oredering.ipynb is for the codes and experiements that show our method is robust against the change between the imaginary and real part of the complex nubmers.
> the Alternative Models.ipynb shows the experiemtns that prove robustness and superiority of our method against the current existing ML methods.   -->
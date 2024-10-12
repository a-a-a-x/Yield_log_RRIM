# Yield_log_RRIM
This is a repository for the paper "log-RRIM: Yield Prediction via Local-to-global Reaction Representation Learning and Interaction Modeling".

## Data processing
The raw datasets of USPTO500MT and Buchwald-Hartwig are provided in the folder 'Data'. The Data processing step filters out reactions without identifiable reaction centers. <br>
The sample code of this step is provided in the file [`USPTO_data_process.ipynb`](USPTO_data_process.ipynb). And the filtered datasets are also provided, Buchwald-Hartwig: [`BH_processed.csv`](BH_processed.csv), USPTO500MT: [`USPTO500MT_train_processed_100.csv`](USPTO500MT_train_processed_100.csv), [`USPTO500MT_valid_processed_100.csv`](USPTO500MT_valid_processed_100.csv), [`USPTO500MT_test_processed_100.csv`](USPTO500MT_test_processed_100.csv), sampled_CJHIF: [`sample_test_CJ_processed_final_5w_wo0.csv`](sample_test_CJ_processed_final_5w_wo0.csv). 

## Feature Generation
This step generates the reactant, reagent, and product features needed for log-RRIM. The sample code is [`USPTO_features_process.ipynb`](USPTO_features_process.ipynb). Each dataset's generated reactant, reagent, and product features are also provided in the repository. 

## Training and testing
[`test_BH.pbs`](test_BH.pbs) and [`test_USPTO.pbs`](test_USPTO.pbs) contain the commands to train and test the log-RRIM on different datasets use the basic atom features or the learned atom features, which is controlled by parameter '--use_pretrain 0'. 

## Analysis
The model comparison and the analyses between log-RRIM and T5chem can be found in the folder [`results_analysis`](results_analysis).

## Package requirements


## Contact with us
Email: hu.2823@osu.edu

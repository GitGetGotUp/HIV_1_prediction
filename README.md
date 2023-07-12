# HIV_1_prediction
using XGBoost in a classification exercise: Kaggle competition from 13 years ago:


Winner had 27 Submissions, and a Score of 0.67. That was 13 years ago. 
Today: couple lines of code + XGBoost achieve 0.81. Without hyperparamter tuning or extensive feature engineering. 

This contest focuses on using the nucleotide sequence of the Reverse Transcriptase (RT) and Protease (PR) to predict the patient's short-term progression. For the non-Biologist: the nucleotide sequence is the blueprint of the protein, which is the workhorse of the cell.  The RT enzyme is responsible for copying the HIV-1 genome within the cell. As the HIV-1 genome is translated it is in one long string of amino acids; the PR protein cuts this string into the numerous functional units - required by the HIV life-cycle. These are the proteins that are targeted by most HIV-1 drugs since they are mostly unique to the HIV-1 life-cycle.  

Along with the HIV-1 viral sequences I have provided the two common clinical indicators used to determine the "general health" of an HIV-1 infected individual: Viral Load and CD4+ cell counts.  The CD4+ cell count is an estimate of the number of white-blood-cells in 1 mL of blood while the viral load is the number of viral particles in that same mL.  In this dataset the viral load is represented in a log-10 scale.  The higher the number the more "active" the immune system. Paradoxically higher CD4 counts imply both a healthier individual but also a higher amount of viral reproduction (the virus primarily replicates in CD4 cells).

If you're interested in learning more about the HIV lifecycle and HIV treatments, here are some extra resources:
http://en.wikipedia.org/wiki/HIV
http://www.youtube.com/watch?v=RO8MP3wMvqg&feature=related
http://www.hiv.lanl.gov/content/sequence/HIV/HIVTools.html
http://en.wikipedia.org/wiki/HIV_therapy#Treatment



According to the World Health Organization, HIV has caused 25 millions deaths worldwide since it was first recognized in 1981. In recent years, the infection has been managed with a collection of therapies. However, the virus will likely evolve around these drugs, making it crucially important that we get a better understanding of the virus itself. 

An important step in understanding the virus, is to get a handle on its genetic blueprint. This competition aims to do this by having contestants find markers in the HIV sequence which predict a change in the severity of the infection (as measured by viral load and CD4 counts).

Models can be trained using the records of 1,000 patients. To predict an improvement in a patient's viral load, competitors will be provided with data on the nucleotide sequences of their Reverse Transcriptase (RT) their Protease (PR) and their viral load and CD4 count at the beginning of therapy. There is a brief discussion of the science of these variables in the Background section, but no knowledge of biology is necessary to succeed in this competition. Competitors' predictions will be tested on a dataset containing 692 patients.        

The competition is being run by http://www.ucl.ac.uk/complex/.



The evaluation method is the misclassification error rate, which calculates the number of incorrect predictions as a proportion of the total number of predictions. This means that a contestant is punished equally for a false positive and a false negative prediction.

The score quoted on the leaderboard is 1 less the misclassification rate - so the higher the score the better. Also note that the public leaderboard is calculated based on 30 per cent of the submission to prevent contestants from overfitting their models. The full leaderboard will be revealed after the competition deadline passes.  

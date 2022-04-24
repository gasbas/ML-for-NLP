# News Article Summarization 
### Ecole Nationale de la Statistique et l'Administration Economique (ENSAE)

--- 
This repository contains our report and notebook for the course Machine Learning for Natural Language Processing given at ENSAE.
We evaluated three methods for automatic summarization on the CNN/Daily Mail dataset: 
- A baseline method called *lead-3* that extract the first three sentences of an article to produce a summary
- A sequence2Sequence model based on Transformers trained from scratch
- A pre trained BART model, fine tuned for summarization on this dataset. 

Evaluation was made using the gold standard ROUGE-1, ROUGE-2 and ROUGE-L. 

The baseline performs really great but is still outperformed by the BART model. Our Seq2Seq model has shown really poor performances that can be partly explained by underfitting. 

# Example of a summary 

    Reference article

        The build-up for the blockbuster fight between Floyd Mayweather and Manny Pacquiao in Las Vegas on May 2 steps up a gear on 
        Tuesday night when the American holds an open workout for the media. The session will be streamed live across the world and you 
        can watch it here from 12am UK (7pm EDT).

     Reference Summary 

        Floyd Mayweather holds an open media workout from 12am UK (7pm EDT). The American takes on Manny Pacquiao in Las Vegas on May 2. 
        Mayweather's training is being streamed live across the world.

     Lead-3

        The build-up for the blockbuster fight between Floyd Mayweather and Manny Pacquiao in Las Vegas on May 2 steps up a gear on 
        Tuesday night when the American holds an open workout for the media. The session will be streamed live across the world and you 
        can watch it here from 12am UK (7pm EDT).

    Seq2Seq 

        Floyd Mayweather will be open to the fight on Tuesday night. The fight will be open in Las Vegas. Mayweather will be open to 
        the fight Floyd Mayweather and Manny Pacquiao.

     BART 

        Floyd Mayweather will hold an open workout for the media on Tuesday night. The session will be streamed live across the world 
        and you can watch it here from 12am UK (7pm EDT). Mayweather and Manny Pacquiao will fight in Las Vegas on May 2.

# Authors

- Dounia CHEKEMBOU, ENSAE, MS Data Science.
- Gaspard MICHEL, ENSAE, 3A.
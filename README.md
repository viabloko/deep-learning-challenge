# deep-learning-challenge
Module 21
Overview of the analysis:
The goal is to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

Results: 
  Data Preprocessing
    What variable(s) are the target(s) for your model?
         Binary success rate (Yes or No)
    What variable(s) are the features for your model?
         List of application type, classification type, income, special considerations (Y, N)
    What variable(s) should be removed from the input data because they are neither targets nor features?
         In this exercise, we removed the Name and EIN (probably, the code ID for each organization).  However, I would still keep the Name for better classification
  Compiling, Training, and Evaluating the Model
    How many neurons, layers, and activation functions did you select for your neural network model, and why?
        I finally stopped at two layers and eight neurons each. I did not find useful to increase more (no improvement in the accuracy) which will consume more power. I also cut the epoc number as could not notice the difference betwwen 50 and 100 counts. 
    Were you able to achieve the target model performance?
        Unfortunately, no.  Optimizing the model did not improve the accuracy of ~73%
    What steps did you take in your attempts to increase model performance?
        I played with the cutoff value for classificatioan (appliation_type and classification bins), activation function (relu and tahn), number of hidden layers (incerased to three but no effect). No improvement in the accuracy was noted.
        
Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
        In total, 804 parameters were created, 0.55 fraction loss and the accurace of 0.726 were recorded. I could not improve the accuracy by adjusting the knobs, such as # of layers and neurons, cut-off classifier values. 
        I wonder if we should still keep the NAME for better binary classifier.
        The model was saved as AlphabetSoupCharity.h5 file.

# EEG-based BCI using Emotiv Epoc X and Visual Imagery


In this project, I explored the feasibility of using Emotiv EPoc X to record a potential BCI control strategy based on the emergent Visual Imagery (VI) paradigm.
The working of a BCI system is commonly composed of three basic components: signal acquisition, signal processing and control device, as shown below:

 
 <img src="https://github.com/Ilesal/BCI_Analysis/blob/main/images/BCI_flow.png?raw=true" width="600px" height="auto">
 


In this experiment, the subject performs two visual imagery tasks. The first one, denoted as Relax, requires the participant to imagine a blue sky. In the second one, called Push condition, the subject imagines pushing a box along a corridor. We collected a total of 30 sessions, where each session is composed of 5 trials:


 <img src="https://github.com/Ilesal/BCI_Analysis/blob/main/images/design.png?raw=true" width="400px" height="auto">


Once the EEG data have been collected with Emotiv, they have been pre-processed using the following pipeline:


 <img src="https://github.com/Ilesal/BCI_Analysis/blob/main/images/preproc.png?raw=true" width="600px" height="auto">

 
 
Then, I explored how this pipeline might affect the final decoding performance. I compared the performance of different decoders when applied to preprocessed and non-preprocessed data. Similarly, the accuracy classification was compared when also different features were taken into account. 
The best performance was achieved by SVM when applied to occipital alpha power features extracted with Morlet Wavelet Transform, reporting a 70% accuracy: 

 <img src="https://github.com/Ilesal/BCI_Analysis/blob/main/images/first_res.png?raw=true" width="350px" height="auto">


and by LDA, with a 72% accuracy, when applied to spatial features extracted through Common Spatial Pattern: 

 <img src="https://github.com/Ilesal/BCI_Analysis/blob/main/images/second_res.png?raw=true" width="600px" height="auto">




 









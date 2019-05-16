# Language-Identification-using-CRNN
Building a CRNN to classify audio into one of 5 languages - English, German, Catalan, French, Italian

## Summary
Language Identiﬁcation(LID) systems are used to classify the spoken language from a given audio sample and are typically the ﬁrst step for many spoken language processing tasks, such as Automatic Speech Recognition (ASR) systems. Without automatic language detection, speech utterances cannot be parsed correctly and grammar rules cannot be applied, causing subsequent speech recognition steps to fail.We have implemented CRNN architecture used in the previous research with a few modiﬁcations of our own to explore the architecture through various experiments. We checked the performance with 3 different spectrogram representation techniques. Robustness of model was also tested with 10 different noises and 2 different loudness levels. 

## Highlights
* Extracted data from https://voice.mozilla.org/en/datasets for five languages - English, German, Catalan, French, Italian
* Data contained audio clips recorded by people, hence were very diverse, i.e. contained different accents, voice from people with different gaes and gender etc.
* Data were not clean, i.e. included clips which had too much noise or even periods of silence
* Created a spectrogram by extracting features in 3 scales: STFT, Mel Scale, MFCC 
* Trained a Convolution Recurrent Neural Network i.e. CNN followed by LSTM to build a classification model to obtain a CV accuracy of ~91%
* Checked the robustness of the model using data with 2 different intensities of noise, obtained accuracy of ~87% on data with softer noise and ~83% on data with louder noise

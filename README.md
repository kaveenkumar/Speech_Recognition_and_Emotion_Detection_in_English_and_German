## Transcribing audio clips
```
The Command and GUI tools perform transcription on long wav files.
They take in a wav file of any duration, use the WebRTC Voice Activity Detector (VAD)
to split it into smaller chunks and finally save a consolidated transcript.
```
### 0. Prerequisites
```
Setup your environment


$ sudo apt install virtualenv
$ cd ~/vad_transcriber
$ virtualenv -p python3 venv
$ source venv/bin/activate
(venv)$ pip3 install -r requirements.txt
```


### 1. Download Models and audio files


[click here](https:)



### 2. Staring the GUI

The GUI tool does the same job as the CLI tool.
The output is displayed in the transcription window and saved into the directory as the input
audio file as well.
```
$ python3 audioTranscript_gui.py
```

Then browse the Model folder that contains model, trie and LM 
After that browse the audio file that needs to be 16000kz.

Then you are ready to transcribe!


#### References

Our report can be obtained from Research Gate -
https://www.researchgate.net/project/Speech-Recognition-and-Emotion-Detection-in-English-and-German

We primarily utilized Mozilla DeepSpeech -
https://github.com/mozilla/DeepSpeech

English sentiment analysis -
https://www.liip.ch/en/blog/sentiment-detection-with-keras-word-embeddings-and-lstm-deep-learning-networks

German sentiment analysis -
https://textblob-de.readthedocs.io/

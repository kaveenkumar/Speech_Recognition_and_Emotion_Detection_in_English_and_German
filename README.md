## English and German Audio Transcriber
```
A Linux based application that can transcribe audio file of English or German to text.
Consecutively it can also detect the sentiment in the text.
```
### 0. Prerequisites
```
Setup your environment

If virtual environment is not installed on your Linux machine -
$ sudo apt install virtualenv

Navigate to your Transcriber directory (or create one)
Clone this git content

Initiate and activate a venv -
$ virtualenv -p python3 venv
$ source venv/bin/activate

Install the prerequisites -
(venv)$ pip3 install -r requirements.txt
```
### 1. Download Models and Sample Audio files

[click here](https://drive.google.com/open?id=1wuhkZ3b5jKfoNIDfaEzrdg-KZVagk-lS)

### 2. Transcribing / GUI working

```
$ python3 audioTranscript_gui.py
```
Steps -
1) Choose input: Microphone recording or file upload
2) Choose the language: English or German
3) Browse for the wav file if file upload chosen
4) Browse for the model and supporting files directory: Models/english or Models/german from
5) Click on 'Start speaking' for microphone or 'Transcrive wav' for file upload

The GUI tool performs transcription on long wav files.
It takes in a wav file of sample rate 16KHz of any duration, then uses the WebRTC Voice Activity Detector (VAD) to split it into smaller chunks and finally save a consolidated transcript in the source audio directory.

The output of text and sentiment is displayed on the transcription window.

Enjoy! :')

## References

Our report can be obtained from Research Gate -
https://www.researchgate.net/project/Speech-Recognition-and-Emotion-Detection-in-English-and-German

We primarily utilized Mozilla DeepSpeech -
https://github.com/mozilla/DeepSpeech

English sentiment analysis -
https://www.liip.ch/en/blog/sentiment-detection-with-keras-word-embeddings-and-lstm-deep-learning-networks

German sentiment analysis -
https://textblob-de.readthedocs.io

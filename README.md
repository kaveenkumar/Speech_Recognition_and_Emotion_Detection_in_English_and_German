# English and German Audio Transcriber + Emotion detector 
## Speech-to-Text + Sentiment Analysis
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
$ mkdir transcriber
$ cd transcriber

Clone this git content
$ git clone https://github.com/kaveenkumar/Speech_Recognition_and_Emotion_Detection_in_English_and_German.git
$ cd Speech_Recognition_and_Emotion_Detection_in_English_and_German

Initiate and activate a venv -
$ virtualenv -p python3 venv
$ source venv/bin/activate

Install the prerequisites -
(venv)$ pip3 install -r requirements/requirements.txt

For sentiment analysis we user the corpora from textblob
run the following command to download it
$ python -m textblob.download_corpora
```
### 1. Download Models and Sample Audio files

[click here](https://drive.google.com/open?id=1wuhkZ3b5jKfoNIDfaEzrdg-KZVagk-lS)

### 2. Transcribing / Working with GUI
Simply run the below command to launch the GUI
```
$ python3 transcriber_gui.py
```
Steps -
1) Choose the language: English or German
2) Choose input: Microphone or file upload
2.1) Browse for the wav file if file upload chosen
3) Click on 'Start speaking' for microphone or 'Transcribe wav' for file upload

The GUI tool performs transcription on long wav files.
It takes in a wav file of sample rate 16KHz of any duration, then uses the WebRTC Voice Activity Detector (VAD) to split it into smaller chunks and finally save a consolidated transcript in the source audio directory.

The output of text and sentiment is displayed on the transcription window.

Enjoy! :')

**Note**: if you notice the GUI crashing, please remember to follow this procedure:
Everytime you want to change between 'mic' and 'file upload', always remember to follow this sequence - 'click on language' -> 'click on mic / file' -> 'click on start speaking / transcribe wav'. If you want to change from file_upload to mic (or mic to file), always click on language first and then mic and then start speaking.

## References

Our report can be obtained from Research Gate -
https://www.researchgate.net/project/Speech-Recognition-and-Emotion-Detection-in-English-and-German

We primarily utilized Mozilla DeepSpeech -
https://github.com/mozilla/DeepSpeech

English sentiment analysis -
https://www.liip.ch/en/blog/sentiment-detection-with-keras-word-embeddings-and-lstm-deep-learning-networks

German sentiment analysis -
https://textblob-de.readthedocs.io

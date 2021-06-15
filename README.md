# English and German Audio Transcriber + Emotion Detector 
## Offline Speech-to-Text + Sentiment Analysis
```
A Linux based application that can transcribe audio file of English or German to text.
Consecutively it can also detect the sentiment in the text.
Works completely offline!
```
Based on our published paper - [German Speech Recognition System using DeepSpeech](https://dl.acm.org/doi/abs/10.1145/3443279.3443313)

![image](https://user-images.githubusercontent.com/38073885/122025881-07083b80-cdca-11eb-9826-0fa2f9082fc4.png)

![image](https://user-images.githubusercontent.com/38073885/122027470-6f0b5180-cdcb-11eb-9bef-26e801ea5ce4.png)

### 0. Prerequisites

Setup your environment

If virtual environment is not installed on your Linux machine -
```
sudo apt install virtualenv
```

Navigate to your Transcriber directory (or create one)
```
mkdir transcriber
cd transcriber
```

Clone this git content
```
git clone https://github.com/kaveenkumar/Speech_Recognition_and_Emotion_Detection_in_English_and_German.git
cd Speech_Recognition_and_Emotion_Detection_in_English_and_German
```

Initiate and activate a venv
```
virtualenv -p python3 transcriber
source transcriber/bin/activate
```
or 
```
mkvirtualenv transcriber
```

Install the prerequisites inside venv
```
(transcriber) pip3 install -r requirements/requirements.txt
```

For sentiment analysis we use the corpora from textblob.

run the following command to download it
```
python -m textblob.download_corpora
```

### 1. Download Models and Sample Audio files
The model files are too large to be uploaded on GitHub. Hence, download them from [here](https://drive.google.com/drive/folders/1wuhkZ3b5jKfoNIDfaEzrdg-KZVagk-lS?usp=sharing)

Once the model files are downloaded, move them to the proper storage structure such that the main file can read them.
Directory structure to follow:

```
~(home/user/)
 |----Speech_Recognition_and_Emotion_Detection_in_English_and_German
     |----audio
          |----english
             |----audio_file_sample.wav
          |----german
             |----audio_file_sample.wav
     |----models
          |----english
             |----alphabet.txt
             |----lm.binary
             |----output_graph.pb
             |----trie
          |----german
             |----alphabet.txt
             |----lm.binary
             |----output_graph.pb
             |----trie
     |----requirements
          |----requirements.txt
     |----tools
          |----wavSplit.py
          |----wavTranscriber.py
     |----transcriber_gui.py 
```

### 2. Transcribing / Working with GUI
Simply run the below command to launch the GUI
```
python3 transcriber_gui.py
```
Steps to use the GUI-
1) Choose the language: English or German
2) Choose input: Microphone or file upload
3) Browse for the wav file if file upload chosen
4) Click on 'Start speaking' for microphone or 'Transcribe wav' for file upload

The output of text and sentiment is displayed on the transcription window.

Enjoy! :')

**Note**: if you notice the GUI crashing, please remember to follow this procedure:
Everytime you want to change between 'mic' and 'file upload', always remember to follow this sequence - 'click on language' -> 'click on mic / file' -> 'click on start speaking / transcribe wav'. If you want to change from file_upload to mic (or mic to file), always click on language first, then mic and then start speaking.

## References

Our report can be obtained from Research Gate -
https://www.researchgate.net/project/Speech-Recognition-and-Emotion-Detection-in-English-and-German

We primarily utilized Mozilla DeepSpeech -
https://github.com/mozilla/DeepSpeech

English sentiment analysis -
https://www.liip.ch/en/blog/sentiment-detection-with-keras-word-embeddings-and-lstm-deep-learning-networks

German sentiment analysis -
https://textblob-de.readthedocs.io

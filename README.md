# Classical Piano Composer

This project leverages a Long Short-Term Memory (LSTM) neural network to generate music. It begins with parsing MIDI files to extract notes and chords, which are then converted into sequences of integers. These sequences are used to train an LSTM-based neural network designed to predict the next note in a sequence, effectively learning the musical patterns and structures from the training data. Once the model is trained, it generates new music by predicting a sequence of notes based on a random starting sequence. These generated notes are then converted back into a MIDI file format, resulting in a playable piece of music. By utilizing deep learning techniques, this project explores the creative domain of music composition, showcasing the potential for AI-driven music generation

## Requirements

* Python 3.x
* Installing the following packages using pip:
	* Music21
	* Keras
	* Tensorflow
	* h5py

## Training

To train the network you run **lstm.py**.

```
python lstm.py
```

The network will use every midi file in ./midi_songs to train the network. The midi files should only contain a single instrument to get the most out of the training.

**NOTE**: You can stop the process at any point in time and the weights from the latest completed epoch will be available for text generation purposes.

## Generating music

Once you have trained the network you can generate music using **predict.py**



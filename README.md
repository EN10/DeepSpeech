# Deep Speech

Based on [Mozilla DeepSpeech](https://github.com/mozilla/DeepSpeech) v0.1.1  
Tested on CS50.io

## Install DeepSpeech:

    sudo pip install -U pip
    sudo pip install deepspeech

## Install 7z & Extract Graph

    sudo apt update
    sudo apt install p7zip-full
    7z e output_graph.7z.001 
    
## Run DeepSpeech
speech-to-text inference on WAVE file:

    deepspeech output_graph.pb man1_wb.wav alphabet.txt
    
## Free Space
Delete 7z files:

    rm output_graph.7z.00*

Recover deleted 7z files:  

    git checkout output_graph.7z.00*

## Update output_graph.pb

Download [latest release](https://github.com/mozilla/DeepSpeech/releases) model:

    wget https://github.com/mozilla/DeepSpeech/releases/download/v0.1.1/deepspeech-0.1.1-models.tar.gz
    
Extract then Create 50MB volumes

    7z a -mx9 -v50m output_graph.7z output_graph.pb
    
codenvy faster than cs50.io
 
## Error

`tensorflow/core/platform/cpu_feature_guard.cc:35] The TensorFlow library was compiled to use AVX2 instructions, but these aren't available on your machine.
Aborted`

requires AVX2 see `less /proc/cpuinfo`
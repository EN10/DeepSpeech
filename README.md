# Deep Speech

Based on [Mozilla DeepSpeech](https://github.com/mozilla/DeepSpeech)  
Tested on CS50.io

## Install DeepSpeech:

    sudo pip install -U pip
    sudo pip install deepspeech

## Install 7z

    sudo apt update
    sudo apt install p7zip-full
    7z e output_graph.7z.001 
    
## Run

    deepspeech output_graph.pb man1_wb.wav alphabet.txt
    
## Error

`tensorflow/core/platform/cpu_feature_guard.cc:35] The TensorFlow library was compiled to use AVX2 instructions, but these aren't available on your machine.
Aborted`

requires AVX2 see `less /proc/cpuinfo`

## Free Space
Recover deleted 7z files:  

    git checkout output_graph.7z.00*
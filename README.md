# Stupid Speaker (WIP)

Stupid Speaker is a minimalist voice recognition system designed to only recognize a predefined set of commands. Unlike feature-rich smart speakers, Stupid Speaker focuses on a single goal: precise recognition of a limited dictionary of commands. It doesn't aim to provide general-purpose voice assistance, nor does it offer a wide range of features. If no commands are defined, Stupid Speaker will simply do nothing.

This project is an experiment to explore whether limiting the scope of recognized commands can improve accuracy. Stupid Speaker serves a purpose when only a few specific actions are needed, and nothing more.

## Key Features

- Pattern Match: Prioritizes accuracy over versatility by limiting its dictionary.
- Plugin Architecture: User can define own action as plugin.

## Pseudocode

*Voice*: Binary, *Prompt*: String, *Command*: *Target* &times; *Action*, *Target*: String, *Action*: String, *Script*: String

*SpeechToText*: *Voice* &rarr; *Prompt*  
*AnalyzeSemantics*: *Prompt* &rarr; *Command*  
*ExecuteCommand*: *Command* &rarr; *Script*  
*TextToSpeech*: *Script* &rarr; *Voice*

*Answer* = *TextToSpeech* &compfn; *ExecuteCommand* &compfn; *AnalyzeSemantics* &compfn; *SpeechToText*  
*Answer*: *Voice* &rarr; *Voice*

- SpeechToText: Julius
- TVController: Nature Remo &or; Infrared Signal
- Cast: Chromecast
- TextToSpeech: VoiceVox

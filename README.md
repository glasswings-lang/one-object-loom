# one-object-loom
## A single-branch auto-itterating text generator using phi3:mini and ollama
Inspired by [slimepriestess](https://nitter.net/slimepriestess) telling us about [Command Loom Interface](https://github.com/socketteer/clooi), this project implements a single-branch auto-itterative text generator in Python3.
## Requirements:
* [Ollama](https://ollama.com/) installed
* Optional: [UV package manager for python](https://docs.astral.sh/uv/)
* The python bindings for ollama (`pip3 install ollama`) installed.


## Usage
     Clone this repository and  then do
```
cd one-object-loom
#Create a virtual environment to isolate packages from the system python.
python -m venv .venv
# Or if using UV:
uv venv
.venv\scripts\activate
#Replace backslashes with slashes if on a Unixlike OS
python -m pip install ollama
#Or the UV equivalent:
uv pip install ollama
ollama pull <modelname> (whatever model you want so long as it runs and is a valid modelname for ollama) 
# optional, if you don't already have a  model downloaded
python ool.py
```
This will install ollama, download a model of your choosing, then start the loom.
You will be prompted to set several parameters before the process starts, including system prompt, user message, continuation phrase, model name, and session name. .

When finished, run the following command to deactivate the virtual environment:
```
deactivate`
```

Whenever running ool.py, be sure to run `.venv\scripts\activate` first!

## Credits go to:
* Slimepriestess - for the initial idea of looms, as well as the song lyrics that comprise the initial user message
* Rozaya (CommunityBelonging) for contributions regarding the "continuation phrase" feature, as well as for code contributions to a feature to attempt to avert looping.
* Garrett Klein/[@garrettk18](https://github.com/garrettk18/) for tie virtual environment instruction and UV info.
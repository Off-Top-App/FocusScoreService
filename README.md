### Stanford CoreNLP/Stanza:
Python Flask server that checks for input from a text file containing the results from MozillaDeepSpeech and performs the following Natural Language Processing operatiopns using the StanfordNLP library, currently known as Stanza:
- TokenizeProcessor.
- POSProcessor.
- LemmaProcessor.
- NERProcessor.

**Pre-Reqs:**
- Need to have Python3 installed and `pip3`.

- Need to set up a virtual environment in Python skip to 'Activate' if you already have one set up.
  - Use the following command to install virtual-env: 
   (Linux) `sudo apt install python3-venv`
   (Windows) `pip3 install virtualenv`
  - Create a virtual directory which has the required scripts using: `python3 -m venv my-venv`
  - Activate the virtual env using the following command: `source my-venv/bin/activate`
   
- Need to have flask package installed using:
   (Linux) `sudo apt-get install flask`
   (Windows)`pip3 install flask`
   (Mac) `pip3 install flask`

- Need to have flask_apscheduler package installed using:
   (Windows)`pip3 install flask_apscheduler`
   (Mac) `pip3 install flask_apscheduler`

- Need to have datetime package installed using:
   (Windows)`pip3 install datetime`
   (Mac) `pip3 install datetime`

- Need to have stanza package installed using:
   (Linux) `sudo apt-get install stanza`
   (Windows)`pip3 install stanza`
   (Mac) `pip3 install stanza`

- Need to download the pre-trained English model and extract it using:
	Launch the Python interactive interpreter and first, run `import stanza` then, `stanza.download('en', '~/stanza_resources')`
	*By default, Stanza stores its models in a folder in your home directory. The English model should be downloaded to `off-top-python/stanfordnlp`.
	*Make sure to specify your own directory (the second argument in the download command.
	*Make sure the name of the model folder is "stanza_resources".

**Description:**
- Inside this branch navigate into stanfordnlp. You will see a script called `stanza-nlp.py` which is a Flask server.
`stanza-nlp.py` - The Flask server runs through a task scheduler, checks for input from a text file, and displays the processed results (Tokens, POS', NER tags) on the terminal every 10 seconds.

**How to use:**
Locate the directory of `stanza-nlp.py` inside stanfordnlp and then run `python3 stanza-nlp.py`. This will automatically run the processes and generate the results on the terminal.
*Make sure you have the input .txt file in the same directory which is the same file that Mozilla DeepSpeech generated with the results.

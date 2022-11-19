# secretsanta
A secret santa generator. Supports excluding particular matches from the final draw, and can email each participant their match if supplied with a SMTP server and email account.

Internally contains a Santa class. He makes the list, checks it twice, and is capable of determining who is naughty and who is nice. Disseminating Santa's information is done by his Elves class.

The information is provided to [``secretsanta.py``](secretsanta.py) in the [``secretsanta.yml``](secretsanta.yml) YAML file, including a list of names and contacts (typically email addressess), and a list of excluded pairings. The a toggle determines whether specified exclusions go both ways or are unidirectional. A seed for the random number generation can be provided. This file is also where the email is set up, specifying the SMTP server, message subject, and message body. The login details are entered securely within the terminal or notebook.

### Usage:
Run ``python secretsanta.py`` in the terminal, which automatically imports data from [``secretsanta.yml``](secretsanta.yml). For examples of using this within a jupyter notebook, have a look at [``docs/secretsanta_example.ipynb``](docs/secretsanta_example.ipynb) or [``docs/secretsanta_yaml_example.ipynb``](docs/secretsanta_yaml_example.ipynb) for using information from a YAML file.

If you're sending the emails from a Gmail account you will need to [generate a one-time-use app password](https://support.google.com/accounts/answer/185833) or the script will not be able to log in.

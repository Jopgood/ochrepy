# **Ochrepy**

##### Ochrepy is a Python library. Its primary purpose is to interface with the Ochre API from Python. This can act as a very helpful package for ETL/ELT for Python developers working for music (and music-related) companies.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Quick Start](#quick-start)
  - [Example with client authentication](#example-with-client-authentication)
- [Reporting Issues](#reporting-issues)
- [Contributing](#contributing)

## Features

Ochrepy supports all features of the web API available at the [Ochre API Documentation](https://ochreapi.docs.apiary.io).

## Installation

```bash
pip install ochrepy
```

alternatively, for Windows users 

```bash
py -m pip install ochrepy
```

or upgrade

```bash
pip install ochrepy --upgrade
```

## Quick Start

Comprehensive documentation will be provided soon, explaining all available methods and abilities of this package. For the meantime, examples can be found in the examples directory.

To use this package, you will need a client ID and a client secret, which you can obtain through your account manager at Ochre.

### Example with client authentication

#### .env
```
OCHRE_CLIENT_ID=
OCHRE_CLIENT_SECRET=
OCHRE_CLIENT_USERNAME=
```

#### code
```python
import ochrepy
from ochrepy.auth import OchreClientCredentials

op = ochrepy.Ochre(client_credentials_manager=OchreClientCredentials())

results = op.music_tracks.list()
for track in response['results']:
            pprint(track['title'] + ' - ' + track['artist']['name'])
```
Expected result will be the list of tracks found in your account.
```
'Track 1 - Artist 1'
'Track 2 - Artist 2'
'Track 3 - Artist 3'
'Track 4 - Artist 4'
'Track 5 - Artist 5'
'Track 6 - Artist 6'
'Track 7 - Artist 7'
'Track 8 - Artist 8'
'Track 9 - Artist 9'
'Track 10 - Artist 10'
```


## Reporting Issues

If you have suggestions, bugs or other issues specific to this library,
file them [here](https://github.com/Jopgood/ochrepy/issues). Or just send a pull request.

## Contributing

If you are a developer with Python experience, and you would like to contribute to Ochrepy, please be sure to follow the guidelines listed on documentation page.
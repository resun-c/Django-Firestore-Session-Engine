# <p align="center" style="margin: 2rem auto; width: -moz-fit-content; width: fit-content; font: 2.5rem 'JetBrains Mono'">Django-Firestore-Session-Engine</p>


This is a simple [`Django Session Engine`](https://docs.djangoproject.com/en/dev/topics/http/sessions) that uses `Firestore` as the database to store session data.


## How to use


Import the collection reference for storing session data from your Firestore initialization file as `__SESSION_COL__`

#### Change [line 13](firestore_session_engine.py#13) of the [firestore_session_engine.py](firestore_session_engine.py) file


```

from firestore_init import FIRESTORE_SESSION_COL as __SESSION_COL__

```

Replace `firestore_init` with the file name where you have initialized `Firestore` and `FIRESTORE_SESSION_COL` with the variable name you used to initialize the collection where you want to store session data.


## Tips

Do not 'initialize' or 'import initialized' Firestore in more than one file while using it with Djnago. A good practice is to initialize firestore in the `settings` file and import it from there.


## Acknowledgements

This Engine was made based on what is described in the Djnago documentation on [`How to use sessions`](https://docs.djangoproject.com/en/dev/topics/http/sessions/) and after some reverse-engineering of the existing session engines, especially the `'django.contrib.sessions.backends.db'` and `'django.contrib.sessions.backends.file'` engines.

Please send any  comments  and  criticisms  to the author here saif.resun@outlook.com
<p  align="center">
  <img  align="center" src="https://resun-c.github.io/resources/happy_coding.svg?t=1686599284" height="64px">
</p>

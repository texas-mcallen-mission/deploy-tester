# deploy-tester
Demo repository for our CLASP deployment pipeline that shows exactly what you need to get started.

### [Link to Dev Branch of Demo](https://script.google.com/d/1ENdDRwHHCkaZhoE8mMbjWNmvy5fmFVa5hNBKaIMAbOR3zfpdAkrf2iKo/edit?usp=sharing)

## Things To Setup

Everything you need to hit an MVP deployable app.

Things to do:

1. Set up repo secrets.

### Actions Secrets

- *to access- go to your repository's Settings / Security / Secrets / Actions.*

#### ``CLASPRC_JSON``

- The contents of ``clasprc.json``.  You get this by setting up and logging into [clasp](https://github.com/google/clasp) on a local machine.  (You will need to install node.js on your machine for this to work, BTW.)  It generally winds up in your home directory.

``REPO_ACCESS_TOKEN``

- [Personal access token](https://github.com/settings/tokens) with ``repo`` access.

#### ``SCRIPT_ID``

The script id- the alphanumeric string after ``projects/``: in this demo's case, the string for this:

[https://script.google.com/u/1/home/projects/1ENdDRwHHCkaZhoE8mMbjWNmvy5fmFVa5hNBKaIMAbOR3zfpdAkrf2iKo/edit](https://script.google.com/u/1/home/projects/1ENdDRwHHCkaZhoE8mMbjWNmvy5fmFVa5hNBKaIMAbOR3zfpdAkrf2iKo/edit)

is ``1ENdDRwHHCkaZhoE8mMbjWNmvy5fmFVa5hNBKaIMAbOR3zfpdAkrf2iKo``

#### ``CONFIG_DATA`` - optional, but recommended

If you want to pass through data (in JSON format) to your project, here's where to send it in.  We use this to store document ID's and stuff that we don't want to publish.  For this demo, we're passing in some fake config data that looks like this:

```js
    config1: {
        key1:"WORDS", // Comment
        key2:"WORDSSS",
        key3:"MOAR WORD" /*inline comment*/
    },
    config2: "WOO",
    config3: ["A","B","C","D"]
```

*This data gets stored inside a JS object.  Anything that legally fits inside of one of those is okay.*

#### ``PARENT_ID`` - optional

If you have a containing document, put the ID for it here.

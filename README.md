# CREATOR Remote lab
<!-- TODO: Explain what this is -->


## Setup
In order to send the results via email, you must set your Google Mail address in
the `EMAIL` environment variable and your
[app pasword](https://support.google.com/mail/answer/185833?hl=en) in the
`PASSW` environment variable.

The configuration of the target boards must be placed in
`config/deployment.json`.
<!-- TODO: Explain config -->

More information in the [CREATOR documentation](https://creatorsim.github.io/creator-wiki/teaching-resources/remote-lab.html).


## Executing

### With Docker Compose
```
docker compose up --build
```

### With Python
This project uses [uv](https://astral.sh/uv). Install it and run with:
```
uv run flask --app src/app.py run
```


## Development
This project uses [uv](https://astral.sh/uv) as a package manager.

In order to set up the virtual environment (`.venv/`), run:
```
uv sync
```

And activate it accordingly:
- Linux/MacOS (bash/zsh): `source .venv/bin/bash`
- Windows (powershell): `& .venv\Scripts\activate.ps1`

Now you can just run:
```
flask --app src/app.py run --dev
```
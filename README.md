# Hearth and Kin

## Libraries and APIs Used

- FastAPI: A modern, fast (high-performance), web framework for building APIs with Python 3.6+ based on standard Python type hints.
- SQLModel: SQL databases in Python, designed for simplicity, compatibility, and robustness.
- OpenAI: An API for accessing OpenAI's artificial intelligence models.
- nVIdia NIM: API endpoints for working with a large number of models, that we can choose from
- ElevenLabs: A text-to-audio generative model with very convincing voices and tone
- Uvicorn: A lightning-fast ASGI server implementation, using uvloop and httptools.

## Key Features

- Real-time communication: This application uses FastAPI to provide real-time communication.
- Database: This application uses SQLModel to manage a SQLite database.
- AI Integration: This application uses OpenAI's API to integrate AI capabilities.
- Environment Variables: This application uses dotenv to manage environment variables.

## Code Structure

The main application is created as a FastAPI object. The application is configured to use a SQLite database located at 'db/test.db'.

Several models are defined with SQLModel for:
- Users
- Stories
- Characters
- Sessions

## Environment Variables

The application uses the following environment variables:
- OPENAI_API_KEY: The API key for OpenAI.
- ELEVENLABS_API_KEY: The API key for ElevenLabs.
- ELEVENLABS_VOICE_ID: The voice ID for ElevenLabs.
- NVIDIA_API_KEY: API Key for LLMs.

## Development

Install [pyenv](https://github.com/pyenv/pyenv). When you enter the directory, it will recognize which python version should be used (`.python-version file`) and use it automatically.


```bash
cd hearth_and_kin
pyenv install $(cat .python-version)
```

Connect poetry to the proper version of python

```bash
poetry env use $(which python)
```

Install dependencies locally. You can use docker!

```bash
make install
```

Run tests (pytest)

```bash
make test
```

Build app

```bash
make build
```

Run app

```bash
make run
```
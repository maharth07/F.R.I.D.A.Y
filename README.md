# F.R.I.D.A.Y — Voice Assistant

This README documents the `Friday.py` voice assistant found in this repository. It explains what the script does, required dependencies, how to run it, example voice commands, and troubleshooting tips.

## What it does
- Listens to microphone input and attempts to recognize spoken commands using Google's Speech Recognition API.
- Responds using the system text-to-speech engine via `pyttsx3`.
- Performs actions: play YouTube videos, search the web, tell time/date (IST), open Notepad/Calculator (Windows), fetch short Wikipedia summaries, and tell jokes.

## Important files
- `Friday.py` — main voice assistant script (microphone input + TTS + command handling).

## Dependencies
- Python 3.8 or newer is recommended.
- Required Python packages (install with pip):

```Terminal
python -m pip install SpeechRecognition pyttsx3 pywhatkit wikipedia pyjokes pytz
pip install pipwin
pipwin install pyaudio
```

Notes on individual packages:
- `SpeechRecognition`: provides microphone input wrappers and speech-to-text. Using `recognize_google` sends audio to Google's Web Speech API (internet required).
- `pyttsx3`: offline TTS engine; uses system voices (on Windows this uses SAPI).
- `pywhatkit`: used to open/play YouTube and perform web searches.
- `wikipedia`: fetches summaries for "who is" queries.
- `pyjokes`: returns short programming jokes.
- `pytz`: used for timezone-aware time (IST) display.

## Run (console)

Run the assistant:

```Terminal
python Friday.py
```

The script runs a continuous loop listening for commands. Use Ctrl+C in the terminal to stop it.

## Common voice commands
- "Play <song or video name>" — plays the specified title on YouTube.
- "Time" or "What is the time" — replies with the current time in India (IST).
- "Date" or "What is the date" — replies with today's date.
- "Open notepad" — launches Notepad (Windows).
- "Open calculator" — launches Calculator (Windows).
- "Tell me a joke" or "Joke" — tells a joke using `pyjokes`.

## Privacy and network notes
- Speech recognition with `recognize_google` sends audio to Google servers for transcription; do not use with sensitive audio.
- `pywhatkit` and `wikipedia` open network connections for search and lookup.

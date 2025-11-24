# Project Statement — F.R.I.D.A.Y. Voice Assistant

Purpose
- F.R.I.D.A.Y. is a small hobby voice assistant implemented in `Friday.py`. Its goal is to demonstrate a lightweight, local orchestration of speech recognition and text-to-speech to perform common tasks (play media, fetch quick facts, open apps, tell jokes, report time/date).

Scope
- The project focuses on clarity and simplicity rather than production readiness. It uses readily available Python libraries to provide a functional assistant that runs on a personal machine.
- The assistant is intended for experimentation, learning, and small automations rather than handling sensitive or critical tasks.

Design Choices
- Uses `SpeechRecognition` with Google Web Speech for reliable transcription; this requires an internet connection.
- Uses `pyttsx3` for TTS to avoid relying on external cloud speech services for output.
- Commands are implemented as straightforward string matches for readability and easy modification.

Dependencies
- See `README_FridayOnly.md` for installation instructions. Key packages include: `SpeechRecognition`, `pyttsx3`, `pywhatkit`, `wikipedia`, `pyjokes`, and `pytz`.

Privacy & Safety
- Audio sent to Google's Web Speech API is transmitted over the internet; do not use the assistant with private or sensitive audio.
- The code executes system commands (e.g., `start notepad`, `calc`) — run only on trusted machines and review code before executing.

Limitations
- No explicit authentication, sandboxing, or permission system — be cautious about enabling it on multi-user machines.
- Simple command parsing may produce false positives; consider adding a wake word or stricter parsing for production use.

Recommended Next Steps
- Add a configuration file to control voice selection, speech rate, and timezone.
- Implement a wake-word detector or short push-to-talk button to reduce accidental activations.
- Add logging and opt-in telemetry for debugging (store logs locally by default).

Acknowledgements
- Built using several open-source Python libraries; see their respective licenses for details.


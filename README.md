# PicoLang

Simple, fast dictionary-based language detector for short texts.

## Installation

```bash
pip install picolang
```

## Usage

```python
from picolang.detector import detect

print(detect("bonjour")) # ('fr', 0.45)
print(detect("学中文")) # ('zh', 0.45)
print(detect("ciao mondo")) # ('it', 0.9)
print(detect("El gato doméstico")) # ('es', 0.45)

# Optionally, specify a subset of languages to consider
print(detect("ciao", languages=["de", "ro"])) # ('de', 0.45)
```

`detect(text, languages=[])` -> tuple (`IETF BCP 47 language tag`, `confidence`)

## Supported Languages

 * Afrikaans
 * Albanian
 * Arabic
 * Armenian
 * Basque
 * Bengali
 * Bulgarian
 * Catalan
 * Chinese
 * Czech
 * Danish
 * Dutch
 * English
 * Esperanto
 * Estonian
 * Finnish
 * French
 * German
 * Greek
 * Hebrew
 * Hindi
 * Hungarian
 * Indonesian
 * Italian
 * Japanese
 * Kabyle
 * Kazakh
 * Korean
 * Latvian
 * Lithuanian
 * Macedonian
 * Norwegian
 * Occitan
 * Polish
 * Portuguese
 * Romanian
 * Russian
 * Serbian
 * Slovak
 * Slovenian
 * Spanish
 * Swedish
 * Thai
 * Turkish
 * Ukrainian
 * Vietnamese
 * Farsi

## Limitations

This detector was designed for handling small texts (< 150 characters). It will probably not work reliably for longer text sequences. As it relies on dictionaries, if a word is missing or misspelled, the detection will fail.

## Contributing

If you want to add a new language, or improve an existing one, add more words to the respective dictionary in the `dictionaries` folder.


## Funding on the AI capabilities

[AIPITCH](https://www.linkedin.com/company/aipitch)(AI-Powered Innovative Toolkit for Cybersecurity Hubs) is a co-funded EU project supported by the European Cybersecurity Competence Centre (ECCC) under the DIGITAL-ECCC-2024-DEPLOY-CYBER-06-ENABLINGTECH program and [CIRCL](https://www.circl.lu).

The project brings together an international consortium to develop AI-based tools that enhance the capabilities of operational cybersecurity teams. These tools are designed to support critical services, with a focus on national security teams, while also being applicable to internal security teams in companies and institutions.


## License

AGPLv3

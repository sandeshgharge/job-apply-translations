# Job Apply Translations

This repository is a supporting translation project for the main application. It centralizes localization data so the main project does not need to manage language files directly.

## Purpose

- Store application translations in a dedicated project.
- Keep the main application simpler by removing the need to add new languages there.
- Make supported languages configurable through `manifest.json`.

## How it works

- `manifest.json` defines the supported languages.
- Each language has a corresponding JSON translation file named with its language code, such as `en.json` or `de.json`.
- The main application can read `manifest.json` and load translations from this project.

## Adding a new language

1. Add a new language entry to `manifest.json`.
   Example:
   ```json
   {
     "code": "fr",
     "name": "Français"
   }
   ```
2. Create a matching translation file named `fr.json` in this repository.
3. Populate `fr.json` with the translated strings used by the application.

## File structure

- `manifest.json`: configuration for supported languages.
- `en.json`: English translations.
- `de.json`: German translations.

## Notes

- The number of supported languages is determined by the entries in `manifest.json`.
- Do not add language support directly in the main application; use this translations project instead.
- Keep translation files synchronized with the application's expected keys.

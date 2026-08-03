# GPT Instructions and Skills Repository Design

## Goal

Create an independent Git repository for reusable GPT instructions and future skill packages while keeping `C:\GitRepo` as a non-repository container for other repositories.

## Structure

- `C:\GitRepo\README.md` inventories repositories stored in the container.
- The `gpt-instructions-and-skills` subdirectory is the Git repository.
- Its root README catalogs individual instructions and skills.
- `instructions/` contains standalone Markdown prompts.
- `skills/` contains future skill packages and its own catalog.

## Initial content

The first instruction is named `pure-css-rotating-glow-border.md`. Its descriptive title and catalog entry make its purpose discoverable without opening every file.

## Publishing

Initialize the subdirectory on the `main` branch, commit only files within that subdirectory, create a new public repository under the authenticated GitHub account, and push `main`. The container-level README remains outside Git and is not published with the subrepository.

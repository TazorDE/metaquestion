# Contributing to meta-question

Contributions are welcome!

The main way you can contibute is by translating the page to new languages.
The process of adding a new language is as follows:

- fork the repository
- clone the forked repository to your local machine
- install the dependencies by running `pnpm install`
- create a new branch for your changes
- open `./project.inlang/settings.json`
- add the desired new 2-letter language code to the `languageTags` array. The code must be a BCP-47 compliant language tag
- create a new file in `./messages` named `<language-code>.json`
- run `pnpm build` to compile the new language file
- use either the [Sherlock VSCode Extension]() or the newly created `.json` file to add the translations
- add your new translation and your name to the appropriate section in [README.md](./README.md)
- submit a pull request with the new translations

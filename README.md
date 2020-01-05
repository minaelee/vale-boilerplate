# vale-boilerplate

This is an repository showcases the basic components of Vale's configuration: a `StylesPath` (`/styles`), a configuration file (`/.vale.ini`), and markup content (this file).

Try it out by running `vale README.md` from your command line.

## Markup

Vale is capable of "understanding" markup, allowing it to intelligently lint prose without generators hundreds of markup-related false positives.

For example, consider the following [`write-good`](https://github.com/btford/write-good) style violations:

> This sentence is extremely good.

When using the `write-good` style, this sentence will generate a warning by default (`'extremely' is a weasel word!`). However, if we format `extremely` as inline code, we will no longer receive a warning:

> This sentence is `extremely` good.

You can also use inline comments to control Vale's behavior:

<!-- vale off -->

This also works for code blocks and you can even write rules that only activate in certain sections of markup (e.g., headings or block quotes). See the [documentation](https://errata-ai.gitbook.io/vale/markup) for more information.

<!-- vale on -->

This is is another sentence with an error.

## Configuration

Vale's configuration file (`.vale.ini`) needs to define a `StylesPath` directory that contains any styles that you'd like to use:

```text
styles/
.gitignore
.vale.ini
```

See the [documentation](https://errata-ai.gitbook.io/vale/configuration) for more information.

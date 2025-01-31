# Advanced Usage

### Using CLI with Proxy Server

Crowdin CLI provides the possibility to work with a proxy server. Each time you run a command, Crowdin CLI checks whether the operating system has the configured environment variables.

Supported environment variables:

- `HTTP_PROXY_HOST` - the name or the IP address of the host at which the proxy server is located
- `HTTP_PROXY_PORT` - the port used by the proxy server for listening
- `HTTP_PROXY_USER` - the username used for authentication on a proxy server
- `HTTP_PROXY_PASSWORD` - the password used for authentication on a proxy server

### Attach labels to the uploaded strings

There are a few ways to attach labels to the uploaded strings using the Crowdin CLI:

1. Specify labels for each file-group in the `crowdin.yml` configuration file:

    ```yml title="crowdin.yml" {5-8}
    files: [
        {
            'source': '...',
            'translation': '...',
            'labels': [
                'main-menu',
                'application'
            ]
        }
    ]
    ```

2. Specify Labels as the [crowdin upload sources](/commands/crowdin-upload-sources) command options:

    ```bash
    crowdin upload sources -s "..." -t "..." --label "main-menu" -- label "application"
    ```

### Excluding target languages for uploaded sources

By default, the source files are available for translation into all target languages of the project. There is a possibility to specify the languages your file shouldn't be translated into:

```yml title="crowdin.yml"
'files': [
    {
        'source': '...',
        'translation': '...',
        // highlight-next-line
        'excluded_target_languages': ['uk', 'fr']
    }
]
```

Or using command options:

```bash
crowdin upload sources --excluded-language uk fr
```

### Download Pseudo-localization

You can configure and download pseudo-localized translation files.

To download an archive with pseudo-localized translation files:

```bash
crowdin download --pseudo
```

Add the `pseudo_localization` section to your `crowdin.yml` configuration file with the following structure:

```yml title="crowdin.yml"
pseudo_localization: {
  length_correction: 25,
  prefix: "",
  suffix: "",
  character_transformation: "cyrillic"
}
```

Visit the [KB article](https://developer.crowdin.com/pseudolocalization/) to read more about Pseudo-Localiation.

### Configure export options for each file group

There is a way to specify export options for each file-group in the `crowdin.yml` configuration file:

```yml title="crowdin.yml"
files: [
     {
         'source': '...',
         'translation': '...',
         // highlight-next-line
         'skip_untranslated_strings': true # Skip untranslated strings
     },
     {
         'source': '...',
         'translation': '...',
         // highlight-next-line
         'skip_untranslated_files': true # Skip untranslated files
     },
     {
         'source': '...',
         'translation': '...',
         // highlight-next-line
         'export_only_approved': true # Export only approved
     },
     { # Only for Crowdin Enterprise
         'source': '...',
         'translation': '...',
         // highlight-next-line
         'export_string_that_passed_workflow': true # Export only strings that passed workflow
     },
]
```

### Ignore hidden files during upload sources

To ignore hidden files during sources upload, add the following to your configuration file:

```yml title="crowdin.yml"
settings: {
    "ignore_hidden_files": false
}
```

Default value - `true`.

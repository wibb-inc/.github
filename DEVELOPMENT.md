# Development

All changes happen through pull requests. Pull requests are the best way to propose changes. Please note that some conventions here might be different than what you are used to. Reading this document will help you save time and work effectively with the developers at Wibb.

## Project Management
We use GitHub Projects for all software related tasks.

Before you make your pull request, it's recommended to start a discussion (Feature Request) topic on Wibb Discussion on GitHub.

## Pull Requests ("PR")
We actively welcome your pull requests. Pretty much in any repository the process is as follow:

1. Fork the repo and create your branch from `staging` (usually named `patch-%the number of PRs you've already made%`)
2. If you've added code that should be tested, add some test examples.
3. If you've changed APIs, update the documentation.
4. Ensure the test suite passes.
5. Make sure your code lints.
6. Finally, ensure to describe your pull request.

## Commiting
All projects are using the [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/) standard. Please follow these steps to ensure your commit messages are standarized:

1. Make sure your shell path is in the root directory of the project you're working on.
2. Install [Commitizen / cz-cli](https://github.com/commitizen/cz-cli) in your local machine if you don't already have it.
3. Run `cz`. This will start an interactive prompt that generates your commit message:
    1. Select the type of change.
    2. Type the scope. This is either `global` for project-wide changes or one of the packages's name (e.g. "web", "mobile", "api", "typescript", etc).
    3. Write a short, imperative tense description of the change (e.g. "add|create|update|remove button" instead of "added|created|updated|removed button").
    4. If the above was not sufficient, you may now write a longer description of your change (otherwise press enter to leave blank).
    5. 'y' or 'n' for whether there are any breaking changes (e.g. changing the props of a component, changing the JSON structure of an API response).
    6. 'y' or 'n' for whether this change affects an open issue, if positive you will be prompted to enter the issue number.

    Your commit should something like this:

    ```
    <type>[optional scope]: <description>
    [optional body]
    [optional footer(s)]
    ```
4. our commit message has now been created, you may push to your fork and open a pull request (read above for "PR" instructions).
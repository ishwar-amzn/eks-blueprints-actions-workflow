# Contributing Guidelines

Thank you for your interest in contributing to our project. Whether it's a bug report, new feature, correction, or additional
documentation, we greatly value feedback and contributions from our community.

Please read through this document before submitting any issues or pull requests to ensure we have all the necessary
information to effectively respond to your bug report or contribution.

## Requirements

The following tools need to be installed on your local machine:

### Mandatory

* [pre-commit](https://pre-commit.com/)
* [tfenv](https://github.com/tfutils/tfenv)
* [tflint](https://github.com/terraform-linters/tflint)
* [tfsec](https://github.com/aquasecurity/tfsec)
* [terraform-docs](https://github.com/terraform-docs/terraform-docs)
* [checkov](https://github.com/bridgecrewio/checkov)

### Recommended

* [oh-my-zsh](https://ohmyz.sh/)
* [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
* [spaceship-prompt](https://github.com/spaceship-prompt/spaceship-prompt)

## Local Development Setup

Run these steps before making changes to the code. They will help automate the commands to lint the code or run tests. These steps help to ensure high code quality and reduce the likelihood that the changes inadvertently break something.

### Install Visual Studio Code recommended extensions

Install Visual Studio Code [recommended extensions](https://code.visualstudio.com/docs/editor/extension-marketplace#_recommended-extensions) defined in [.vscode/extensions.json](.vscode/extensions.json) to improve you productivity and increase code quality.

### Install latest terraform version

```shell
tfenv install latest
tfenv use latest
```

### Install pre-commit hooks

> This will ensure that the commands we want to execute before each commit are executed automatically.

```shell
pre-commit autoupdate
pre-commit install
```

### Execute pre-commit hooks manually on all files

```shell
# All hooks
pre-commit run --all-files

# Checkov
pre-commit run checkov --all-files

# Terraform docs
pre-commit run terraform_docs --all-files
```

## Reporting Bugs/Feature Requests

We welcome you to use the GitHub issue tracker to report bugs or suggest features.

When filing an issue, please check existing open, or recently closed, issues to make sure somebody else hasn't already
reported the issue. Please try to include as much information as you can. Details like these are incredibly useful:

* A reproducible test case or series of steps
* The version of our code being used
* Any modifications you've made relevant to the bug
* Anything unusual about your environment or deployment

## Contributing via Pull Requests

Contributions via pull requests are much appreciated. Before sending us a pull request, please ensure that:

1. You are working against the latest source on the *main* branch.
2. You check existing open, and recently merged, pull requests to make sure someone else hasn't addressed the problem already.
3. You open an issue to discuss any significant work - we would hate for your time to be wasted.

To send us a pull request, please:

1. Fork the repository.
2. Modify the source; please focus on the specific change you are contributing. If you also reformat all the code, it will be hard for us to focus on your change.
3. Ensure local tests pass.
4. Commit to your fork using clear commit messages.
5. Send us a pull request, answering any default questions in the pull request interface.
6. Pay attention to any automated CI failures reported in the pull request, and stay involved in the conversation.

GitHub provides additional document on [forking a repository](https://help.github.com/articles/fork-a-repo/) and
[creating a pull request](https://help.github.com/articles/creating-a-pull-request/).

## Finding contributions to work on

Looking at the existing issues is a great way to find something to contribute on. As our projects, by default, use the default GitHub issue labels (enhancement/bug/duplicate/help wanted/invalid/question/wontfix), looking at any 'help wanted' issues is a great place to start.

## Code of Conduct

This project has adopted the [Amazon Open Source Code of Conduct](https://aws.github.io/code-of-conduct).
For more information see the [Code of Conduct FAQ](https://aws.github.io/code-of-conduct-faq) or contact
opensource-codeofconduct@amazon.com with any additional questions or comments.

## Security issue notifications

If you discover a potential security issue in this project we ask that you notify AWS/Amazon Security via our [vulnerability reporting page](http://aws.amazon.com/security/vulnerability-reporting/). Please do **not** create a public github issue.

## Licensing

See the [LICENSE](LICENSE) file for our project's licensing. We will ask you to confirm the licensing of your contribution.

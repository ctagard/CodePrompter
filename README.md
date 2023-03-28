# Project Prompt Generator

The Project Prompt Generator is a command-line interface (CLI) tool that generates a prompt file for Rust, Go, and JavaScript projects. The generated prompt file contains the contents of the source code files in the project, along with a question provided by the user.

## Features

Automatically finds and processes files based on the specified project type (Rust, Go, or JavaScript)
Respects .gptignore files for ignoring specified files or directories
Allows users to choose between ChatGPT3.5 and ChatGPT4.0 models and warns if the total word count exceeds the model's limit

## Installation

To install the Project Prompt Generator, follow the instructions in the Homebrew section or build it from source.

### Install with Homebrew
```sh
$ brew tap your-github-username/tap-name
$ brew install your-cli-name
```

### Build from source
Clone the repository:
```sh
$ git clone https://github.com/your-github-username/your-cli-repo.git
```
Change to the repository directory:
```sh
$ cd your-cli-repo
```
Build and install the CLI:
```sh
$ cargo build --release
$ cp target/release/your-cli-binary /usr/local/bin/
```

## Usage

USAGE:
    your-cli-binary [OPTIONS]

OPTIONS:
    -t, --type <TYPE>       Sets the project type (rust, go, or js)
    -m, --model <MODEL>     Sets the model type (ChatGPT3.5 or ChatGPT4.0)
    -h, --help              Prints help information
    -V, --version           Prints version information

## EXAMPLES:

Generate a prompt file for a Rust project with ChatGPT4.0:
    $ your-cli-binary -t rust -m ChatGPT4.0

Generate a prompt file for a Go project with ChatGPT3.5:
    $ your-cli-binary -t go -m ChatGPT3.5

Generate a prompt file for a JavaScript project with ChatGPT4.0:
    $ your-cli-binary -t js -m ChatGPT4.0
Replace your-cli-binary with the appropriate value for your CLI.

## .gptignore files
You can create a .gptignore file in your project directory to specify files or directories that the Project Prompt Generator should ignore. The syntax is similar to .gitignore files. For example:

### Ignore all files in the "node_modules" directory
```
#projectdir/.gptignore
node_modules/
```

### Ignore all ".log" files
*.log
License

This project is licensed under the MIT License. See the LICENSE file for details.
Here’s a step-by-step guide to installing `pyenv` on macOS:

### 1. Install Homebrew
If you haven't already, you'll need to install Homebrew, which is a package manager for macOS. Open the Terminal and run the following command:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

### 2. Install pyenv
Once Homebrew is installed, you can install `pyenv` using Homebrew with the following command:

```sh
brew install pyenv
```

### 3. Configure your shell
After installing `pyenv`, you need to configure your shell to use it. If you're using bash, add the following lines to your `~/.bash_profile` or `~/.profile`. If you're using Zsh, add them to your `~/.zshrc` file:

```sh
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv virtualenv-init -)"
```

After adding these lines, restart your terminal or source your profile file with `source ~/.bash_profile`, `source ~/.profile`, or `source ~/.zshrc` depending on your shell.

### 4. Verify Installation
To verify that `pyenv` is installed correctly, run:

```sh
pyenv --version
```

If the installation was successful, you should see the version of `pyenv` printed to the terminal.

### 5. Install Python Versions
Now, you can install different versions of Python. For example, to install Python 3.9.1, you would use:

```sh
pyenv install 3.12.0
```

To switch to a different Python version globally, use:

```sh
pyenv global 3.12.0
```

Or, for a local project-specific version, navigate to your project directory and run:

```sh
pyenv local 3.12.0
```

This will create a `.python-version` file in your project directory that specifies the Python version for `pyenv` to use when you’re working in that directory.

Remember, after installing new versions of Python or changing the global/local Python version, you may need to restart your terminal or re-source your shell configuration file to apply the changes.
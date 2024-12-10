# Manage Ruby 

## Install Ruby

### 1. Install rbenv using one of the following approaches

#### Homebrew
On macOS or Linux, we recommend installing rbenv with Homebrew.
```
brew install rbenv
```

#### Debian, Ubuntu, and their derivatives
```
sudo apt install rbenv
```

### 2. Set up your shell to load rbenv.
```
rbenv init
```
### 3. Close your Terminal window and open a new one so your changes take effect.

## Basic Git Checkout
```
git clone https://github.com/sstephenson/rbenv.git ~/.rbenv
git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build
```
- Add to ~/.bash_profile or ~/.zshrc

```
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile(.zshrc)
echo 'eval "$(rbenv init -)"' >> ~/.bash_profile(.zshrc)
```
- Verify installation
```
type rbenv   # → "rbenv is a function"
```
These are generic instructions; there may be rbenv packages available for your OS.
See: [Installation](https://github.com/rbenv/rbenv#installation)

## Managing versions
| CMD | DES |
|-------|-------|
| rbenv install -l | List all available versions | 
| rbenv install 2.2.1 | Install Ruby 2.2.1 |
| rbenv uninstall 2.2.1 | Uninstall Ruby 2.2.1 |
| rbenv versions | See installed versions |
| rbenv version | See current version |
| rbenv which <NAME> | Display path to executable |
| rbenv rehash | Re-write binstubs |

## Using versions

### Locally
| CMD | DES |
|-------|-------|
| rbenv local 2.2.2 | Use Ruby 2.2.2 in project | 
| rbenv local --unset | Undo above |

> Application-specific version numbers are stored in .ruby-version.

### Globally
| CMD | DES |
|-------|-------|
| rbenv global 2.2.2 | Use Ruby 2.2.2 globally | 
| rbenv global --unset | Undo above |

> Global version numbers are stored in ~/.rbenv/version.

### Shell
| CMD | DES |
|-------|-------|
| rbenv shell 2.2.2 | Use Ruby 2.2.2 in shell | 
| rbenv shell --unset | Undo above |

> Shell-local version numbers are stored as environment variables.

# Add Gemfile && Bundle. How to use bundle?

-- Install Bundle
```
gem install bundler
```
-- Add Gemfile to your project flutter
```
cd ios && bundle init && bundle install
```
-- Add package to gem 
```
bundle add <package_name>
```

-- Use bundle
old: `pod install`
new: `bundle exec pod install`





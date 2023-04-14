# Setting up linters

Add the contents of `settings.json` to the repository `.vscode/settings.json` file (or copy it if it does not exist).

## Client (TypeScript React)

```bash
npm install vite
curl https://bitbucket.prodyna.com/users/ple/repos/react-typescript-guide/raw/.gitignore -o .gitignore
npm create vite app -- --template react-ts
cd app
npm install eslint --save-dev
npx eslint --init
```

Select the following options:

- **ESLint usage:** To check syntax, find problems, and enforce code style
- **Module type:** JavaScript modules (import/export)
- **Framework:** React
- **TypeScript?** Yes
- **Environment:** Browser
- **Style definition:** Use a popular style guide
- **Style guide:** Standard
- **Format:** JSON
- **Install?** Yes
- **Package manager:** npm

## Server (Ruby on Rails)

```bash
rails new server --api
cd server
rm -rf .git
echo "group :development, :test do
  gem 'rubocop', require: false
  gem 'rubocop-rails', require: false
end" >> Gemfile
bundle install
echo "require:
  - rubocop-rails" >> .rubocop.yml
```

## AI Model (Python Flask)

```bash
python3 -m venv pyenv
./pyenv/bin/activate
pip install black flask
```

Install the Python extension for Visual Studio Code if not installed yet:

```bash
# Press Ctrl/Cmd + P and enter
ext install ms-python.python
```

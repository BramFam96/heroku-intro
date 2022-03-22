- [Heroku configuration](#heroku-configuration)
  - [Homebrew install](#homebrew-install)
  - [Heroku install](#heroku-install)
  - [Gunicorn install](#gunicorn-install)
  - [Adding a Procfile](#adding-a-procfile)
  - [Adding runtime.exe](#adding-runtimeexe)

---

# Heroku configuration

---

## Homebrew install

---

```sql
echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"'
eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
sudo apt-get install build-essential
brew install gcc
```

---

## Heroku install

---

```sql
curl https://cli-assets.heroku.com/install.sh | sh
```

heroku -v -> heroku/7.59.4 linux-x64 node-v12.21.0

---

## Gunicorn install

---

Gunicorn will create a production ready server environment

```sql
pip install gunicorn
```

---

## Adding a Procfile

---

```py
echo "web: gunicorn app:app" > Procfile
```

We put this in the root of our app

---

## Adding runtime.exe

---

```sql
echo "python-3.8.10" > runtime.txt
```

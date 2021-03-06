# mastodon-bot-template
A bot template for Mastodon API compatible servers

## Installation
You'll need [Python 3](https://www.python.org/downloads/), along with pip (which should come with python 3). If you're on a Linux system, try installing `python3 python3-pip` or `python python-pip`. If you're on Windows, make sure you check the "Add Python to PATH" box in the installer, if present.

Next you'll need to download mastodon-bot-template. If you have git:
`git clone https://github.com/Lynnesbian/mastodon-bot-template`
Otherwise, download the zip file from [here](https://github.com/Lynnesbian/mastodon-bot-template/archive/master.zip), and extract it somewhere.

After installing Python, you'll need to install mastodon-bot-template's requirements. You can do this by opening a terminal in the directory you put the files in, and running
```
python3 -m venv venv
source venv/bin/activate #if you're on windows, run venv\Scripts\activate.bat instead
python3 -m pip install -r requirements.txt
```

You're now ready to start editing the bot template.

## Configuration
You'll want to edit `meta.json` to set your bot's name, source code page, and administrator. You'll also want to take a look at `login.py`, which defines which instance your bot logs in to, `reply.py`, which handles replying to mentions, and `post.py`, which handles one-off posts. Note that it's mandatory to provide a link to the source code, as this code is licensed under the GNU Affero General Public License v3. You'll also need to link back to [this repository](https://github.com/Lynnesbian/mastodon-bot-template).

Finally, run `login.py` by typing `python3 login.py`, and answer the questions given. You're ready to go! Try running `python3 post.py` to create your first post.

When you upload your source code, **make sure you don't upload the `config.json` file**. This file contains your bot credentials, and if you upload them, someone else can use them to post from your bot's account!!

## Listening for Replies
If you're using systemd, you can fill in the provided `systemd-example.service` and move it into an appropriate direcoty (e.g. `/etc/systemd/system`) to manage replies with systemd. You can do the same with SysVInit, initrc, launchd, etc., but no template is ([currently](https://github.com/Lynnesbian/mastodon-bot-template/pulls)) provided.

You can also listen for replies manually. This is done by running `python3 reply.py`.

## About
mastodon-bot-template is created and managed by [Lynnesbian](https://fedi.lynnesbian.space/@Lynnear_Software). Some code used was originally from [mstdn-ebooks](https://github.com/Lynnesbian/mstdn-ebooks), and many of my other Fediverse bots (e.g. [OCRbot](https://github.com/Lynnesbian/OCRbot)) use similar code.

### Donations
You can donate once with [PayPal](https://paypal.me/lynnesbian) or [Ko-fi](https://ko-fi.com/lynnesbian), or you can set up a monthly donation (with perks!) at [Patreon](https://patreon.com/lynnesbian).

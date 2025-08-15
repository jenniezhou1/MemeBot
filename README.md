<h1>Memebot - Discord Meme Responder</h1>

<h2>Description</h2>
MemeBot is a simple Python Discord bot that listens for the command $meme and replies with a random meme. It connects to the Discord API, read messages, make an HTTP request, and send a response back to a channel.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python 3.10+</b> 
- <b>discord.py</b>
- <b>requests</b>
- <b>python-dotenv</b> (loads tokens from <code>.env</code>)
- <b>Meme API</b>

<h2>Environments Used </h2>

- <b>macOS</b>

<h2>Program walk-through:</h2>

<b>1) Open the project folder</b>
<br />
Open a terminal in the repository root:
<pre><code>cd MemeBot
</code></pre>

<b>2) Create <code>.env</code> with your bot token</b>
<pre><code>DISCORD_TOKEN=your_discord_bot_token_here
</code></pre>

<b>3) Install dependencies</b>
<pre><code>python3 -m pip install -U discord.py requests python-dotenv
</code></pre>

<b>4) (One-time) Invite the bot to your server</b>
<br />
Use the Discord Developer Portal (OAuth2 → URL Generator) with scope <code>bot</code> and permission <code>Send Messages</code>, then open the generated URL to add the bot.

<b>5) Run the bot</b>
<pre><code>python3 bot.py
</code></pre>
Expected terminal output:
<pre><code>Logged on as MemeBot#xxxx!
</code></pre>

<b>6) Use in Discord</b>
<pre><code>$meme
</code></pre>
The bot replies with a meme URL (Discord auto-embeds the image).

<h2>Notes / Troubleshooting</h2>

- <b>Keep secrets out of git:</b> store the token in <code>.env</code> and add <code>.env</code> to <code>.gitignore</code>.
- <b>Message Content Intent:</b> must be enabled in the Developer Portal for <code>$meme</code> to be detected.
- <b>Multiple replies:</b> ensure only one process is running (stop extra terminals with <code>Ctrl+C</code>).
- <b>macOS SSL error (system Python):</b>
<pre><code>/Applications/Python\ 3.10/Install\ Certificates.command
</code></pre>

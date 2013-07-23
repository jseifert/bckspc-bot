# bckspc-bot

## Description

bckspc-bot is an IRC bot for [backspace][1]'s channel on freenode (#backspace).
It provides various features to interact with space infrastructure and other
handy things.

## Commands

<dl>
  <dt>!inspace</dt>
  <dd>List the members currently present.</dd>

  <dt>!pizza NUM{s,m,h}</dt>
  <dd>Alert you in NUM seconds/minutes/hours. Default is 15 minutes.</dd>

  <dt>NICK +1</dt>
  <dd>Give NICK one karma point.</dd>

  <dt>!karma [NICKS]</dt>
  <dd>List each NICK's karma score.
      If no NICK is supplied, list the issuer's score.</dd>

  <dt>!karmatop NUM</dt>
  <dd>List the top NUM karma scorers. Default is 3.</dd>

  <dt>!alarm MSG</dt>
  <dd>Broadcasts MSG in the local network.
      Other services may display MSG on the LED-board or similar.<\dd>

  <dt>!echo [ARGS]</dt>
  <dd>Echo the arguments.</dd>
</dl>

## Other features

* Append "open"/"close" to the topic, depending on whether someone is currently
  present.

* Voice members who are currently in the space.

## Configuration

bckspc-bot requires a JSON configuration file that is passed as first argument.
The following fields are accepted:

<dl>
  <dt>statusUrl</dt>
  <dd>URL of the JSON space status information</dd>

  <dt>karmaFile</dt>
  <dd>Path to the file in which karma scores are saved.
      The file must exist.</dd>

  <dt>channel</dt>
  <dd>The channel the bot should join.</dd>
</dl>

See [the provided example file](cfg.json).


[1]: http://www.hackerspace-bamberg.de/Hauptseite

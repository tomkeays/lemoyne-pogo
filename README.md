# Le Moyne PoGo Map

We're using the PokeNav bot in Discord to create a [map showing raid progress and research tasks](https://pgmap.org/map.html?center=43.048631,-76.090419&zoom=17&s2level=0&s2n=2&map=OpenStreetMap&show=1111) on the the Le Moyne College campus.

Le Moyne PoGo Map Discord invite: https://discord.gg/4u8Zjp

Here's what the base map looks like now. 

![pogo-map-unpopulated](https://user-images.githubusercontent.com/171037/56751665-9f5b8600-6754-11e9-8a48-51f1eed00cd9.png)

Note: the "Le Moyne Clock" location appears twice. This is because PokeNav verified the location at one point when the GPS coordinates were off. Those coordinates were fixed in the game, but PokeNav still has the old information. In the meantime, we set the POI alias using the correct GPS coordinates, so it appears twice. PokeNav doesn't yet have a mechanism for the community to report these sorts of errors.

## POI Aliases

Here are POI aliases for the Gyms and Pokestops on-campus and near campus. These save some typing for reporting Raids and Research.

* bell = "Le Moyne College Bell Tower"
* chapel = "Panasci Family Chapel"
* clock = "Le Moyne Clock"
* devotion = "Devotion"
* dolphy = "Eric Dolphy Jr. Statue"
* grewen = "Grewen Hall Of Presidents"
* iron = "Iron Sculpture"
* library = "Falcone Library"
* lynch = "Shane Lynch Memorial"
* pac = "W. Carroll Coyne Center for the Performing Arts"
* soule = "Soule Branch Library"
* cemetery = "Salt Springs Cemetery"

## Reporting Raids

Report in the `#announce-raids-here` channel in Discord. Reporting a raid will create a new channel in Discord that lasts for the duration of the raid.

After reporting a raid, it will be listed in the `#active-raids` channel. More importantly, it will create a channel on the fly just for that raid, where members of the Discord server can indicate if they will participate.

Full documentation: https://docs.pokenavbot.com/raids.html

### Reporting Raid Bosses

Command takes this form: "`$raid latios chapel 37`", where:

* `$raid` is the command
* `latios` is the name of the Pokemon (case insensitive)
* `chapel` is the name of the POI; can use alias or full name
* `37` is the number of minutes until despawn

![raid-report](https://user-images.githubusercontent.com/171037/56749522-e3985780-674f-11e9-90e0-0c9031bb40e2.png)

### Reporting Unhatched Raid Bosses

If egg still hasn't hatched, instead use the `$egg` command. 

E.G., "`$egg giratina dolphy 51`" or "`$egg T5 dolphy 51`", where:

* `$egg` is the command
* `giratina` is the name of the Pokemon, if known; else use the tier, e.g., `T5`
* `dolphy` is the name of the POI; can use alias or full name
* `51` is the number of minutes until hatch

![egg-report](https://user-images.githubusercontent.com/171037/56749499-d713ff00-674f-11e9-8669-9934df1faf49.png)

Note: You will need to go into the the new raid channel after hatch and report the name of the Raid boss that hatched from the egg. E.G.,  `$boss giratina`

### Uploading Gym Screenshots

You can also upload a screenshot of the raid gym, showing the name of the gym and the time to hatch or despawn. E.G., here's an egg report.

![egg-screenshot](https://user-images.githubusercontent.com/171037/56749880-9799e280-6750-11e9-84af-5826e2893c2c.png)

![egg-screenshot-report](https://user-images.githubusercontent.com/171037/56750541-ff9cf880-6751-11e9-9c7f-d6a4b4bc871a.png)

Note: there's a limit of 20 screenshot uploads per month per person. You can check where you are at by typing "`$quote`" in the `#general` channel.

### Raid Counters

If the raid boss was set, simply use `$counters` to get the list of counters for that boss. You can also provide current weather conditions, `$counters rain`.

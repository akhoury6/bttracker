# Battle Trophy Tracker

This is a tool to help keep track of Battle Trophies in Star Ocean 3! It also uses [Aerius's Battle Trophy Guide](battle_trophy_guide) on [GameFAQs](gamefaqs) to provide details and hints on how to get the trophies. All credit for the actual content goes to Aerius and the other contributors to that guide - I'm only making it easier to use.

It can be run side-by-sde with an emulator too, to view and keep track of your battle trophy data while you play the game.

![Screenshot](./screenshots/screenshot01.png)

## Install & run

`Ruby >= 3.3` is the only preqrequisite required to run. It can optionally use the gem `colorize` to display colored output, which is highly recommended.

The file `trophies.zlib` contains the data from the FAQ, as well as the record of which trophies have been completed.

```shell
git clone --depth=1 https://github.com/akhoury6/bttracker.git
cd bttracker; rm -rf .git
chmod u+w trophies.zdata; chmod u+x bt
./bt
```

## How to use

Running the tool like above shows a list of commands that it accepts. The most commonly used are `list`, `find`, `mark`, and `unmark`.

Completed trophies will get an asterisk (*) net to their number and will be displayed in green. Incomplete trophies will be displayed in red.

### List

```shell
./bt list                  # List incomplete trophies
./bt list all              # List all trophies
./bt list 12 13 14 15 ...  # List the status of specified battle trophies
```

### Find

```shell
./bt find term1 term2 ...  # Find all trophies which contain "term1" and "term2", and display their guides
```

### Mark / Unmark

```shell
./bt mark 147 148 ...      # Mark all specified trophies as completed
./bt unmark 147 148 ...    # Mark all specified trophies as incomplete
```

### Rewards

```shell
./bt rewards               # Display all reward tiers, which are obtained, and how many are left until the next one
```

### FAQ

```shell
./bt faq                   # Display the FAQ
./bt faq 1                 # Display FAQ section 1 only (1, 2 or 3)
```

[gamefaqs]: https://gamefaqs.gamespot.com
[battle_trophy_guide]: https://gamefaqs.gamespot.com/ps2/536705-star-ocean-till-the-end-of-time/faqs/38855

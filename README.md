```sh
brew tap roar/aged-upgrade
brew install jq

brew aged-upgrade --days 10
```

`brew aged-upgrade` upgrades outdated formulae and casks to the newest version
whose tap file is older than the configured age cutoff. If the latest tap file
commit is newer than the cutoff, the command temporarily checks out the most
recent older revision of that formula/cask file, runs `brew upgrade`, and then
restores the tap file. Upgrades run with Homebrew auto-update and API installs
disabled so the selected local tap revision is used.

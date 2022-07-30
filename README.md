RSS -> IMAP Bridge
==================

Modified version of RSS -> IMAP bridge ([https://github.com/tbrownaw/rss-imap](https://github.com/tbrownaw/rss-imap)) which uses a SQLite database to store loaded feed URLs and a yaml file for the feed config, instead of looking up in the RSS folder (plus a few other minor modifications to suit my needs)

Create the database (RSS.db) with the following SQL:

```sql
CREATE TABLE feeds (feed_folder text, guid text, loaded_datetime text, primary key (feed_folder, guid));
```

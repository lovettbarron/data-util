# data-util
Personal data utilities. Parsing, scraping, scheduling, automating.

## Sack Patrol
*Requires .env file and a twillio account*

Made because there was a stupid thing I wanted to cop. Basically, it repeatedly polls a big cartel site's endpoint to see when soemthing switches from Sold Out to anything else. Catches errors if the item itself is removed from the list or similar, and can continue the polling. Would have cost the price of the item to do this via another mode, and was a fun little project. Plays the sound file in the `/sound` folder. 

# Download recommended episodes from Overcast

95% of this script was written by [Alex Chan](https://git.alexwlchan.net/?p=overcast-downloader;a=summary)
I've just added a flag to by default download only the episodes that you've started.

Big thanks to Alex for writing this script!

## Instructions

You need:

- **An Overcast account with an email and password.**
  You can create this in the Overcast iOS app.
  If you haven't done this before, or you've forgotten your email/password, read [my instructions](add_email_password) for doing so.

- **A working Python 3 installation.**
  This script only works with Python 3.6 or later.

Steps:

1.  **Get your Overcast OPML file.**

    Log in to the Overcast website at <https://overcast.fm/login> using your email address and password.

    Once you're logged in, navigate to <https://overcast.fm/account>.
    Under "Export Your Data", click "All data".
    This will download an OPML file, which includes a list of every podcast episode you've ever played.

2.  **Download the Python script.**

    Download the script [`download_overcast_podcasts.py`](download_overcast_podcasts.py), and save it somewhere on your disk.

3.  **Run the script, passing the path to your OPML file as the first argument.**
    For example, if the OPML file is in the same directory as the python file `./overcast.opml` and you want to create the podcast folders in the same, run:

    ```console
    $ python overcast-download.py overcast.opml --download_dir . --recommended
    ```

    To download all the files (basically Alex's original script, run):

    ```console
    $ python overcast-download.py overcast.opml --download_dir . --recommended 0
    ```

The initial download will be very slow, depending on how many podcasts you've listened to, and it uses a lot of disk space.
(At time of writing, I have ~1200 episodes in my export, which take up 61 GB.)
On subsequent runs, the script should only download files that it hasn't saved before, so it should be a lot faster.

## License

MIT

```

```

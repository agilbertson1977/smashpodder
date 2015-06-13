smashpodder

podcatching client based on MashPodder, and eaerlier, BashPodder

This is Andrew Gilbertson fork of Chess Griffin's podcast downloading client,
MashPodder. Many of the updates are simply refactoring to make the code
easier to deal with; however, see the end of this README for details about
what's changed. 

Smashpodder allows the user to download podcast episodes. The user can choose
to save these episodes in a named directory (i.e. separate directory per feed)
or in a date-based directory, so the most recent episodes are in one folder.
Or, the user can combine this by having some podcasts in a named directory and
others in the date-based directory. The user can choose to download all, none,
or a set number of episodes per feed. The user can also choose to mark the
episodes as downloaded (without actually downloading them) which can be used
to 'catch up' to a podcast.

Three files are needed: mashpodder.sh, mp.conf, and parse-enclosure.xsl. All
three of these files are available here in the mashpodder repository. You can
also browse through the source tree and download the files directly. There is
also a sample cron wrapper script that folks can use and modify. I will
occasionally package up a simple tarball of these files to make it easier for
folks to download.

Note, you also need wget, curl, and xsltproc installed. They are usually
included in most default distro installs or you can get them from your
distro's repositories.

Finally, about the Git repo: this is a tiny project so there will only be
one branch, which is 'master' and that will contain the latest code and
patches and testing bits.  It may or may not work at any given time.
However, when it seems that the code is stable, I'll tag a release.  So,
basically, if you want something stable, use the latest release.  If you
want the latest-and-greatest or want to help test, use the master branch.

Enjoy!

Here's the bit about Andrew's updates:
1. The ability to choose whether or not to "fix" the filename that is
   provided by the RSS feed.  The fact that Scientific American was providing
   filenames that were "podcast.mp3?fileID=$UUID" was causing the MashPodder
   to always see these as just "podcast.mp3" and not download it as that name
   was already in the log as having been previously downloaded.
2. Prepending a source name to name of the downloaded file. This isn't
   at all useful to getting podcasts to download, but it does allow the user
   to figure out what's the source of a file with a funny-looking filename is.



# bc-librarian
Unzip albums from bandcamp, put them in the right place, updates a playlist & stores the original zipfile in an archive.

## ziptodir
This script runs on a Synology NAS. It:

 1. finds zipfiles downloaded from bandcamp (manually, currently)
 2. unzips those files into the appropriate directory
 3. moves the zipfile to an archive outside of where the NAS stores music
 4. TODO: updates a playlist with recent tracks from bandcamp
 5. TODO: moves the album directories into the main locations
 
The script should run on a cron via:

```
find . -type f -a -name \*.zip -exec ./ziptodir {} \;
```

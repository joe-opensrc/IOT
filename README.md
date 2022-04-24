## README

In Our Time Podcast CLI Script Suite (v0.2)

A script suite to parse / download / play episodes from the public InOurTime Podcast Website.

Files:
  - IOTFetch: 
      - Fetch files (or url placeholders) 
      - update iot.db 
  - IOTPlay:
      - Simple selection of downloaded files or placeholders:
          - uses vlc for mp3s
          - uses firefox for urls / pholds
  - README.md:
      - this file :)
  - iot.db:
      - db of episodes and assocciated metadata


Observations:
  - The BBC Website has changed:
      - filenames no longer in the meta-header via curl
      - later episodes are not currently available as mp3 downloads:
          - we create a placeholder file which contains the episode url
  - This is a significant re-write of v0.1, should probably be v1.0 ;)
          

Dependencies: 
 - fzf (https://github.com/junegunn/fzf)
 - fmt
 - vlc 
 - curl 
 - wget 

#### Fetch an episode
```bash
user@host> IOTFetch 
```
#### Fetch an episode and include episode description in fzf list (helps with searching) 
```bash
user@host> IOTFetch -d
```
#### Incremental update of iot.db 
```bash
user@host> IOTFetch -u 
```
#### Full update of iot.db (should be used sparingly) (NOT WORKING)
```bash
user@host> IOTFetch -u 0
```

#### Play an episode with vlc
```bash
user@host> IOTPLay
```

TODO:
  - make vlc -> xdg-open 
  - perhaps consolidate wget into curl to reduce dependencies
  - maybe remove fzf dependency...

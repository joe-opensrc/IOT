## README

In Our Time Podcast CLI Script Suite.
 
A script suite to parse / download / play episodes from the public InOurTime Podcast Website.

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
#### Full update of iot.db (should be used sparingly)
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

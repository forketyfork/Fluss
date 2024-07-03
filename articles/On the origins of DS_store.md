from:: [On the origins of DS\_store | Lobsters](https://lobste.rs/s/q7rxib/on_origins_ds_store)
url:: [On the origins of DS\_store](https://www.arno.org/on-the-origins-of-ds-store)
on:: 2024-07-03 15:34

An old article from 2006. The former tech lead of Mac OS X Finder tells the story of the `.DS_Store`files, how they came to be, and why they're named that way. DS means Desktop Services, a backend part of Finder that was extracted (during the heavy rewrite in 1999) to be used by other applications and eventually to be published as an API. Dot at the beginning is for invisibility. There was also a long standing bug back then: this file was created every time the user visited the folder (instead of only when some view settings for this folder are changed). 

Indeed, I remember the time those files were created all over the place, but I'm pretty sure this issue is fixed already.
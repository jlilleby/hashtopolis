## BETA State: Important

Hashtopussy currently is in BETA state. This means there may be still some bugs or things not working. You are free to test anything and helping us with reporting detected bugs or problems. 

You NEED to use the very new hashcat version, if it's older than 2nd of March, it will not work. 

These features are not working / not ready yet:

- WPA cracking (we still need some times on this as we will support hccapx)
- Binary hash handling is not complete
- Currently only the C# client is completely working, others are just partially implemented

There are parts of the documentation/wiki which are not up-to-date. If you detect anything or have questions on understanding descriptions, feel free to ask us.

To report a bug, please create an issue and try to describe the problem as accurately as possible. This helps us to identify the bug and see if it is reproducable.

---

# Hashtopussy 

<img src="https://github.com/s3inlc/hashtopussy/blob/master/src/static/logo.png" alt='Hashtopussy' width="100">

Hashtopussy is a multi platform client-server tool to distribute Hashcat tasks between multiple computers and is strongly based on Hashtopus. 
Like Hashtopus The main goals for its development were portability, robustness, Multi-user support, and to bring Hashtopus to the next level. 
The application has two parts:

- **Agent** Multiple clients (C#, Python, PHP) easily customizable to suite any need. 
- **Server** several PHP/CSS files operating on two endpoints: Admin Gui and Agent Connection Point

Aiming for high usability even on restricted networks, Hashtopussy communicates over HTTP(S) using own proprietary JSON protocol so its easy to understand and text-readable. 

The server part runs on PHP using MySQL as database back end. It is vital that your MySQL server is configured as well as possible performance wise. 

Some of the queries can be very expensive and proper configuration makes the difference between few milliseconds of waiting and	disaster multi-second lags. 

The database schema heavily profits from indexing. Therefore, if you see a hint about pre-sorting your hashlist, please do so. 
The web admin is therefore the single point of access once your agents were deployed on the cracking machines. 

New agent deployment requires one-time password generated in the new agent tab, which protects your server from hashes/files leaking to rogue or fake agents.

## Features

- Easy and comfortable to use
- Accessible from anywhere via Web
- Server part highly compatible with common web hosting set-ups
- Agent part completely unattended
- File management for word lists, rules, ...
- Self-updating of both Hashtopussy and Hashcat
- Cracking multiple hashlists of the same type as one
- Running the same binary on Windows and Linux (OSX untested)
- Files/hashes marked as "secret" only distributed to agents marked as "trusted"
- Many options to import/export data
- A lot of statistic info about tasks/hashes
- Visual representation of chunk distribution
- Event-driven cracking mode
- Multi-User Support
- User Permission levels

## Hashtopus or Hashtopussy?

Hashtopus is a great program but lacking in some areas major differences between the two are: 

- Drastically Improved Security
- Multi User support
- Improved look and layout
- Super Tasks (hcmask support)
- --hex-salt support

Please visit the [wiki](https://github.com/s3inlc/hashtopussy/wiki) to get more information on setup and upgrade.

Some screenshots of Hashtopussy (by winxp5421): [Imgur](http://imgur.com/gallery/Fj0s0)

## Thanks

* winxp for testing, writing help texts and a lot of input ideas
* blazer for modifying the agent to get it working with hashcat v3
* CynoSure Prime for testing
* atom for [Hashcat](https://github.com/hashcat/hashcat)
* curlyboi for the original Hashtopus code

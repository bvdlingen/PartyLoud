# Changelog

## 0.0.10 juli 2019 

### :forked: forked
### :autoinstall_dependency: install dependency's for debian and alike

## [0.0.9] - 2019-05-06
### :new: Added
- DNS randomization flag
- No-Wait (between tow requests) option added

### :white_check_mark: Changed
- Switched Internet connectivity check from PING to TCP Handshake 
- Moved all functions in ./src directory
- Minor fixes

## [0.0.8] - 2019-04-17
### :new: Added
- HTTP/HTTPS proxy option (Thx to [acbekoac](https://github.com/acbekoac "acbekoac"))
- Added flags for separate URL-list and blocklist file specification
- Added disclaimer as suggested by [Samuel First](https://gitlab.com/samuelfirst "Samuel First")

### :white_check_mark: Changed
- Minor code fixes (Thx to [Samuel First](https://gitlab.com/samuelfirst "Samuel First"))
- Minur UI improvements

## [0.0.7] - 2019-04-15
### :new: Added
- HTTP requests are now atomic
- *You can now stop partyloud via CTRL-C*
- On startup is executed a software check, if something is missing user get notified
- On startup is executed a connection check, if partyloud will exit if unable to  connect to network

### :white_check_mark: Changed
- Added compression option to cURL requests
- Added max-time (aka timeout) option to cURL requests
- Changed Header options in cURL requests to filter everything but text
- Changes in UI:
  - Everything fits in 80 cols
  - Every request made will be dispalyed
- Changed error recovery mechanism
- Changed html parsing mechanism
- Changed badwords wordlist
- Changed url list
- Changed url list location (partyloud.conf)

### :no_entry: Removed
- Removed process number option

## [0.0.6] - 2019-03-26
### :new: Added
- Re-added User defined # of threads
    - upper bound = 24
    - lower bound = 1
- Now UserAgent is generated using generateUserAgent function.
- OS List
    - Windows 10
    - Windows 8.1
    - Windows 8
    - Windows 7
    - MacOS Mojave
    - MacOS High Sierra
    - MacOS Sierra
    - MacOs El Capitan
    - Linux (generic)
- Browser List
    - Mozilla Firefox 50 - 66
    - Google Chrome 56 - 73

### :white_check_mark: Changed
- Added Help screen
- Fixed a bug that caused a division by 0 to computed during Engine execution
- Fixed a bug that caused a file named "1" to be generated
- Minor changes in UI

## [0.0.5] - 2019-03-21
### :new: Added
- Now each partyloud engine wait a pseudo-randomic amount of time before
making a new request to prevent anti-DDoS mechanism triggering (Thx to
[Ale Sala](https://www.instagram.com/ale.sala.97/ "Ale Sala"))
- The wait time is calculted using this formula **Wait time** =
(**Guessed #Word** * **Reading Speed [second/word]**)

### :white_check_mark: Changed
- Added User Agents to cURL requests in order to improve traffic
randomness
- Changed error recovery mechanism (now if an HTTP request fail a
backup URL is used)
- Fixed bash 3.2 bug in the URL selection mechanism
- Fixed wc -l related bug
- Minor changes in UI

## [0.0.3] - 2019-03-20
### :new: Added
- Internal Engine is now complete and operative
- cURL is now used to generate pseudo-random requests
- HTML response is now parsed using grep
- Bad URLs are now filtered using a wordlist mechanism
(wordlist is located in a file named badwords)

### :white_check_mark: Changed
- Fixed number of sub-processes to 7

### :no_entry: Removed
- noisy.py and python are now no more required to run the script
- disabled user-defined number of processes

## [0.0.2] - 2019-03-18
### :white_check_mark: Changed
- Started migration from noisy.py to internel Egnine
- Major UI Improvemnts

## [0.0.1] - 2019-03-17
### :new: Added
- Initilal Alpha
- Added a while loop to start a used defined number of noisy.py process
- Added a minimal UI

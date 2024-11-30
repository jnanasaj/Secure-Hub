
# Secure Hub

Secure Hub is a tool developed with the task of aiding SOC analysts with automating part of their workflow. One of the goals of Secure Hub is to perform as much of the routines checks as possible, allowing the analyst more time to spend on deeper analysis within the same time-frame. 


## Contents
 - [Current Features](#Securehub-can-currently)
 - [Requirements](#requirements)
 - [Development](#development)
 - [Changelog](#changelog)
 - [Roadmap](#roadmap)
 - [Contributors](#contributors)
 
<!-- The SOC Analysts all-in-one CLI tool to automate and speed up workflow. -->

![](readmeimages/repcheck.gif)


## Secure Hub can Currently:
  - Sanitise URL's to be safe to send in emails
  - Perform reverse DNS and DNS lookups
  - Perform reputation checks from:
    - [VirusTotal](https://www.virustotal.com)
    - [BadIP's](https://www.badips.com/)
    - [Abuse IPDB](https://www.abuseipdb.com/)
  - Check if an IP address is a TOR exit node
  - Decode Proofpoint URL's, UTF-8 encoded URLS, Office SafeLink URL's and Base64 Strings
  - Get file hashes and compare them against [VirusTotal](https://www.virustotal.com) (see requirements)
  - Perform WhoIs Lookups
  - Check Usernames and Emails against [HaveIBeenPwned](https://haveibeenpwned.com) to see if a breach has occurred. (see requirements)
  - Simple analysis of emails to retrieve URL's, emails and header information.
  - Extract IP addresses from emails.
  - Unshorten URL's that have been shortened by external services. (Limited to 10 requests per hour)
  - Query [URLScan.io](https://urlscan.io) for reputation reports.
  - Analyze email addresses for known malicious activity and report on domain reputation utilising [EmailRep.io](https://emailrep.io)
  - Create dynamic email templates that can be used as a base for phsing triage response.

![](readmeimages/email_analysis.gif)

## Requirements
 - [Python 3.x](https://www.python.org/)
 - Install all dependencies from the requirements.txt file. `pip install -r requirements.txt`
 - To use the Hash comparison with VirusTotal requires an [API key](https://developers.virustotal.com/reference), replace the key `VT_API_KEY` in the code with your own key. The tool will still function without this key, however this feature will not work.
 - To use the Reputation Checker with AbuseIPDB requires an [API Key](https://www.abuseipdb.com/api), replace the key `AB_API_KEY` in the code with your own key. The tool will still function without this key, however this feature will not work.
 - To use the URLScan.io checker function with URLScan requires an [API Key](https://urlscan.io/about-api/), replace the key `URLSCAN_IO_KEY` in the code with your own key. The tool will still function without this key, however this feature will not work. 
 - Use of the HaveIBeenPwned functionality requires an [API Key](https://haveibeenpwned.com/API/Key), replace the key `HIBP_API_KEY` in the code with your own key. The tool will still function without this key, however this feature will not work.
 
## Development

Want to contribute? Great!

  #### Code Contributions
  - New features / requests should start by opening an issue. This helps track new features and prevent crossover.
  - If you wish to work on a feature, leave a comment on the issue page and I will assign you to it.
  - All code modifications, enhancements or additions must be done through a pull request. 
  - Once reviewed and merged, contibutors will be added to the ReadMe

Found a Bug? Show Me!

 #### Bugs and Issues
 - If an issue / bug is found please open a ticket in the issue tracker. State the issue first, and how to recreate it if necessary.
 - I will assign myself / another commenter to that case and work on fixing it asap.

## Changelog

#### Version 1.3 - The Templating Update
 - Added first iteration of dynamic email templates that generate based on Secure Hub's analysis.

![](readmeimages/templateGen.PNG)

#### Version 1.2 - The Phishing Update
 - Added first iteration of the Phishing tool.
 - Able to analyze an email (outlook / .msg only tested at the moment) and retrieve emails, urls (Proofpoint decode if necessary) and extract info from headers. 
 - Extract IP's from body of email.
 - Reputation check on sender of email, and provide enriched information.

#### Version 1.1 - The Reputation Update
 - Improved Rep Checker
 - Added HaveIBeenPwned Functionality
 - Added DNS Tools and WhoIs Functionality
 - Added Hash and VirusTotal Checkers
 - Added Abuse IPDB, Tor Exit Node, BadIP's to Reputation Checker
 
#### Version 1.0
 - Initial Release
 - URL and ProofPoint Decoder
 - Initial implementation of Reputation Checker
 - Sanitize links to be safe for email



## RoadMap
  This is an outline of what features *will* be coming in future versions.
  
#### Version 1.2 - The Phishing Update
  - Scan email attachments for malicious content, macros, files, scan hashes, etc.

#### Version 1.3 - The Templating Update
 - ~~Add dynamic email templates that generate based on Secure Hub's analysis.~~ Edit: Added

#### Version 1.4 - The PCAP Analysis Update
- Add ability to analze .pcap files and provide concise, enriched information.

#### Version 1.x - The Case Update
  - Add a 'New Case' Feature, allowing output of the tool to be output to a txt file.

### MAIL ME FOR THE GUI VERSION OF THE REPO (jsagar@duck.com)

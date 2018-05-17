# Project 7 - WordPress Pentesting

Time spent: **8** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. WordPress  4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [ ] Summary: Puts a Youtube Url with XSS at the end to create an alert popup.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version:  4.7.3
  - [ ] GIF Walkthrough: ![](https://github.com/jmondragon123/IST590/blob/master/XSS.gif)
  - [ ] Steps to recreate:
    1. Log in to an account that has editor privileges.
    2. Add the below comment to any page.
      ```
      https://youtube.com/embed/12345<svg onload=alert(1)>
      ```
     3. Refresh the page and you will get an alert.
  - [ ] Affected source code:
    - [Link 1](https://blog.sucuri.net/2017/03/stored-xss-in-wordpress-core.html)
2. Wordpress Readme.html Version number
  - [ ] Summary: Able to navigate to the readme.html and find the version number of WP running.
    - Vulnerability types: Fingerprinting
    - Tested in version:4.2
    - Fixed in version: 
  - [ ] GIF Walkthrough: ![](https://github.com/jmondragon123/IST590/blob/master/Fingerprint1.gif)
  - [ ] Steps to recreate: 
    1. Navigate to the url below:
     ```
     http://wpdistillery.vm/readme.html
     ```
     2. Website will show what version WP is running
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
3. (Required) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types: Privilege Escalation
    - Tested in version: 4.2
    - Fixed in version: 
  - [ ] GIF Walkthrough: ![](https://github.com/jmondragon123/IST590/blob/master/Privilege%20Escalation.gif)
  - [ ] Steps to recreate: 
    1. Post a comment on a page using a subscriber user.
    2. Approve the comment using an Admin account.
    3. Any new comments created by the Subscriber on that page will be able to post withouth admin approval.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)


## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)
- [Stored XSS in WordPress Core](https://blog.sucuri.net/2017/03/stored-xss-in-wordpress-core.html)


GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Difficult looking through the wpscan output and finding exploits to attempt.

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

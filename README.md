# Project 7 - WordPress Pentesting

Time spent: **8** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. WordPress  4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [ ] Summary: 
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
  - [ ] Summary: 
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
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
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

Describe any challenges encountered while doing the work

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

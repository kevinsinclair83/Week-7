# Week-7
# Project 7 - WordPress Pentesting

Time spent: **X** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) User Enumeration
  - [ ] Summary: 
    - Vulnerability types: User Enumeration
    - Tested in version: 4.2
    - Fixed in version: 4.7.2
  - GIF Walkthrough: ![User Enumeration](https://github.com/kevinsinclair83/Week-7/blob/master/userenumeration.gif)
  - [ ] Steps to recreate: 
  
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Required) 
  - ![XSS Vulverability ] Summary: 
  - Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.0
    - Fixed in version: 4.6
  - ![XSS](https://github.com/kevinsinclair83/Week-7/blob/master/xssvulnerability.gif)GIF Walkthrough: 
  - [ ] Steps to recreate: 
  
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
 3. Persistent XSS exploit commenting as an unauthenticated user (CVE-2015-3440)
  - Summary: 
    - Vulnerability types: Persistent XSS
    - Tested in version: 4.0
    - Fixed in version: 4.2.1
  - GIF Walkthrough: ![Persistent XSS](https://github.com/kevinsinclair83/Week-7/blob/master/xss%202.gif)
  - [ ] Steps to recreate: I searched wordpress 4.2 vulnerabilities in exploit-db.com leading me to Klikki's url outlining a proof of concept stored XSS vulnerability. Using this code as comment text ` <a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>` with 65536 bytes of information to pad the comments, I was able to replicate this vulnerability.   
  
    - [Klikki's link](https://klikki.fi/adv/wordpress2.html)


## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

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

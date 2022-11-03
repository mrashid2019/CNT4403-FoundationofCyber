# Project 7 - WordPress Pen Testing

Time spent: **8** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pen Testing Report

### 1. Large File Upload Error XSS (ID: CVE-2017-9061)
- [ ] Summary: There was a Cross-Site Scripting (XSS) vulnerability which existed when attempting to upload very large files, becuase the error messgae does not properly restrict presentation of the filename. 
  - Vulnerability types: XSS
  - Tested in version: 4.2
  - Fixed in version: 4.7.5
- [ ] GIF Walkthrough: 
- [ ] Steps to recreate: [This link](https://hackerone.com/reports/203515) provides a walkthrough of how to view the "file to large" error which ends up interpolating the file name and appending it into DOM unsanitized leading to XSS. 
- [ ] Affected source code:
  - [Link 1](https://github.com/WordPress/WordPress/commit/8c7ea71edbbffca5d9766b7bea7c7f3722ffafa6)
  
### 2. Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds (ID: CVE-2017-6817)

- [ ] Summary: There is authenticated Cross-Site Scripting (XSS) in YouTube URL Embeds.
  - Vulnerability types: XSS
  - Tested in version: 4.2
  - Fixed in version: 4.7.3
- [ ] GIF Walkthrough: 
- [ ] Steps to recreate: The shortcode provided in [this link](https://blog.sucuri.net/2017/03/stored-xss-in-wordpress-core.html) shows how to get a working stored XSS exploit
- [ ] Affected source code:
  - [Link 1](https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8)

### 3. Authenticated Stored Cross-Site Scripting (XSS) (ID: CVE-2015-5622)

- [ ] Summary: The stored XSS vulnerability in WordPress allows users to inject web scripts or HTML by leveraging the Author or Contributor role to place a shortcode inside an HTML element.
  - Vulnerability types: Cross-Site Scripting (XSS)
  - Tested in version: 4.2
  - Fixed in version: 4.2.3 
- [ ] GIF Walkthrough: 
- [ ] Steps to recreate: The code provided in [this link](https://klikki.fi/wordpress-core-stored-xss/) demonstrates the vulnerability. It should be entered in a page or posting using the HTML edit mode (instead of of the default WYSIWYG).
- [ ] Affected source code:
  - [Link 1](https://core.trac.wordpress.org/changeset/33359)



## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with  ...
<!-- Recommended GIF Tools:
[Kap](https://getkap.co/) for macOS
[ScreenToGif](https://www.screentogif.com/) for Windows
[peek](https://github.com/phw/peek) for Linux. -->

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2022] [Mahdia Rashid]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

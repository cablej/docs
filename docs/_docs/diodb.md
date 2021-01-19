---
layout: doc
title: diodb - Open-source vulnerability disclosure and bug bounty program database
categories: [Core projects]
tags: 
---
Repo:
Status:
Maintainer/s: 
To do/s:

---
A community-powered, vendor agnostic directory of all known VDP and BBPs, contact details, policy location, preferred languages, and the status of:

- Safeharbor
- Availability rewards, hall of fame, swag
- Disclosure policy

### Why does diodb exist?

diodb exists to drive the adoption of Safe Harbor for hackers and promote the cybersecurity posture of early adopters, simplify the process of finding the right contacts and channel at an organization, and help both finders and vendors align around the expectations of engagement. It also provides a simple, vendor-agnostic point of engagement for program operators, potential program operators, and the security community to maintain updates to their program. 

## How to contribute

### Getting started

If you have new VDP or bug bounty program information to add, update, or delete in the [#diodb open-source vulnerability disclosure and bug bounty program list](https://github.com/disclose/diodb/blob/master/program-list.json), we'd love you to contribute by issuing a Pull Request.

If you're new to Github, [this article](https://help.github.com/articles/creating-a-pull-request-from-a-fork/) is a good primer on how PRs work. If you'd like to help us create tooling to allow updates without the use of Git and PRs, get in touch at hello@disclose.io.

### Adding a new program?

Programs on the bug-bounty-list need to satisfy the definition of a public bug bounty or vulnerability disclosure program, which means they need two key components:

1. "policy_url" - A publicly accessible vulnerability disclosure policy, sometimes called a program brief or bounty brief, and
2. "contact_url" - A publicly accessible intake channel for vulnerability submissions. This intake channel must be explicitly mentioned in the vulnerability disclosure policy.

If you work with an organization like this, encourage them to launch a formal and public program and point them to disclose.io for helpful tools to assist them along the way!

### Other tips

* Launch date can be tricky to find on some programs e.g., it's buried in a press release or blog post and not on the program page. If you think you've found a launch date, please include a reference to where you found it in the PR so the maintainers can check.
* Some companies will offer these things on an ad-hoc or case-by-case basis, but this doesn't mean they're committing to do it for everyone. Be careful with the "bounty_offered", "swag_offered", and "hall_of_fame" options. As always, read the program page.

### Some examples of suggestions that won't be accepted:

Remember, the goal of The disclose.io Project is to drive the adoption of VDP with best practices, so we'll only accept entries that satisfy the Policy and Intake requirement above.  

Sometimes, organizations have informal vulnerability reporting setups. While these organizations provide lucky or persistent folks with the option to report issues, this arrangement does NOT constitute a formally established and fully endorsed public VDP.

Some examples of this include:

1. Private programs
2. Invitation-only programs
3. Updates where the intake channel is unlisted or informal in the policy
4. Programs that you heard about from a friend but aren't listed publicly
5. Programs without a public policy or a nominated channel for communication
6. security.txt entries without a valid "policy_url"

## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">disclose</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://disclose.io" property="cc:attributionName" rel="cc:attributionURL">disclose.io</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

# disclose.io/program-list

> The community-powered index of ALL known public bug bounty and vulnerability disclosure programs, including their safe harbor status.  

## How to contribute  
If you've found a new program, new information on an existing program, or think a program should be deleted, you can contribute to the bug-bounty-list by issuing a pull request (PR) to the repo. If you're new to Github, [this article](https://help.github.com/articles/creating-a-pull-request-from-a-fork/) is a good primer on how PRs work. 

## Before you go hunting for new programs to add...

Programs on the bug-bounty-list need to satisfy the definition of a public bug bounty or vulnerability disclosure program, which means they need two key components:
  1. A publicly accessible vulnerability disclosure policy, sometimes called a program brief or bounty brief, and 
  2. A publicly accessible channel for vulnerability submission **which is explicitly mentioned in the vulnerability disclosure policy**.  
  
Some examples of suggestions that won't be accepted:
  1. Private programs  
  2. Invitation-only programs  
  3. Programs that you heard about from a friend but aren't listed publicly  
  4. Programs without a public policy or a nominated channel for communication  
  5. Programs 

## Definition of fields 

- **program_name (optional):** What is the name of the company or product team responsible for the program?  
- **policy_url (required):** Where can the policy which defines the program be found? (Usually a webpage e.g. /security, a URL on a vulnerability management platform, or in a robots.txt or security.txt file).  
- **contact_url (required):** Where does policy say vulnerability submissions should be sent? (Usually a web form, a URL on a vulnerability management platform, or an email address. Emails can be added as URLs using 'mailto:').  
- **launch_date (optional):** When does the program say it was launched?  
- **bug_bounty (optional):** Does the program commit to rewarding vulnerabilities?  
- **swag (optional):** Does the program commit to sending swag out for vulnerabilities?  
- **hall_of_fame (optional):** Does the program have a Thanks page, Hall of Fame, or other page acknowledging vulnerability reporters?
- **safe_harbor (required):** Does the program support full or partial safe-harbor?  

~~~~
  {
    "program_name": "Tesla",
    "policy_url": "https://bugcrowd.com/tesla",
    "contact_url": "https://bugcrowd.com/tesla/report",
    "launch_date": "2013-11-26",
    "bug_bounty": true,
    "swag": false,
    "hall_of_fame": true,
    "safe_harbor": "full"
  },
~~~~

*Example: Tesla*

## How to fill out the safe harbor field

The list supports three safe harbor states: Full, Partial, and None. The flow below will help you determine which applies to the policy as you contribute to the list:  

1. Does the policy mention anything about legal protections for good-faith hackers? If it does, go to Step 2. If not, then you should choose **"None"**. 
2. Does the policy talk about authorization of testing and/or an exemption from pre-existing legal terms? In addition, does the policy clearly define the scope of testing, the compensation for valid findings, the official communication channels, and a disclosure policy? If so, you should choose **"Full"**. If not got to Step 3.
3. Does the policy talk about "not legally pursuing researchers" or use similar language, but does not explicitly grant authorization and/or exemption for security testing? Are any of the key parameters described above ambiguously defined or missing completely? If so, you should choose **"Partial"**. 

## Other tips  

* Launch date can be tricky to find on some programs e.g. it's buried in a press release or blog post and not on the program page. If you think you've found a launch date, please include a reference to where you found it in the PR so the maintainers can check.
* Some companies will offer these things on an ad-hoc or case-by-case basis, but this doesn't mean they're committing to do it for everyone. Be careful with the bug_bounty, swag, and hall_of_fame options. As always, read the program page.
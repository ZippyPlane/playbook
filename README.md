# Acme Playbook
**⚠️ NOTICE**: This is still very much a work in progress.

This is the Acme playbook. In it, you'll find nearly all of the company's operational knowledge. There are some types of information that doesn't live in here, though.

lthough we're pretty small at the moment, we believe very strongly that **good process and tooling** is an easy win. Establishing our policies & processes and setting up our tooling properly is not a lot of effort and is much easier to do **now** than in a few years, once we've started to scale. That's why this document exists. If you want to read a bit more about this, [Process Street wrote a good ebook](http://c.danny.is/ce063d70893a/The-Complete-Guide-to-Business-Process-Management.pdf).

This playbook is fairly extensive. Keeping it relevant is an **important part of everyone's job**. We have a playbook because:

* Reading is much faster than listening.
* Reading is async. You don't have to interrupt someone or wait for them to become available to get an answer to your question.
* Onboarding new hires is easier if you can find all the relevant information.
* Teamwork is easier if you know how other parts of the company work.
* Discussing changes is easier if you can see what the current process is.
* Everyone can contribute to it.

Documenting things in this playbook takes time and requires **thinking**. But it saves time in the long-run and is **essential to scale and adapt our company**. It is like writing tests for your software: it avoids chaos and technical debt in the long-term.

#### Contributing

Process evolves. Tools change. That's a good thing. It's **everyone's responsibility to keep this playbook up-to-date**. Just open a PR and have someone review it. In general:

1. Only include practices, processes and tools that are established in the company or have been agreed as a convention.
2. Imagine you are a new employee joining Acme. **Write for them**.
3. Link to external tools and documentation when you mention them.


## Contents

* Values
* [Tooling](#tooling)
* [Security](#security)
* Engineering
* Product
* Operations

***

## Tooling

We think everyone should be free to use whatever tools work best for them, so we don't prescribe hardware or software. Use whatever you need to get the job done. That said, **collaboration is mega-important**, so we do insist on a standard toolset for sharing and storing work.

### Hardware

Everyone is free to use whatever hardware they choose, providing it meets our security requirements. Remote workers are expected to have a decent microphone and camera (the MacBook camera is good enough, but a decent headset or [external](https://www.bluedesigns.com/products/yeti/) mic is a must).

### Google Apps

We use GSuite for email, calendars, document storung and the like. We enforce 2FA and strong passwords. By convention, we issue usernames as firstname@zippyplane.com. There is also a single group **All Staff** (all@zippyplane.com).

* [GSuite Admin](http://admin.google.com)
* [Email](http://mail.google.com)
* [Calendar](http://calendar.google.com)
* [Drive (file storage)](http://drive.google.com)
* [Documents](http://docs.google.com)
* [Slides](http://slides.google.com)
* [Sheets](http://sheets.google.com)

#### Google Drive

We try to keep **all out stuff** on google drive, unless there is a better tool suited to the job. You should avoid storing information locally in Word, Excell or powerpoint files, instead creating Google docs, sheets and slides. 

Feel free to keep notes, working documents etc in your own GDrive, but *make sure you move any long-lived documents to the Team Drive!*

The team drive contains some top-level folders. Every document you create should go in one of them:

* **Business** - Operations, business and HR related stuff. Some sub-folders are only available to founders, for obvious reasons.
* **Design** - Branding and design assets, sketch files etc.
* **Engineering** - Engineering-related documents
* **Finance** - Financial records (read-only for most people).
* **Marketing** - MArketing-related documents
* **Process** - Process documents. This includes compliance documents, process maps and records of process-improvement activites like retrospectives.
* **INBOX** - A dumping ground for anything that doesn;t have an obvious home.

Just like this document, it's **everyone's responsibility** to keep the GDrive neat, tidy and *useful*. Having said that, we don't want you spending ages agonising over where to put a file.

**Put it in the "INBOX" 📥 if you can't think where it should go** (or if you're really busy). Periodically, someone will go through the inbox and file everything properly, but we'll still be able to find it in the meantime thanks to GDrive's search.

When creating/uploading files:

* **Prefer native Google formats**. If you can easily convert an Excel sheet to a Google Sheet, do so. It will make eveyone else's life easier in the future.
* **Name your files well**. Consider someone looking for it in 12 months. What would they search for?
* **Avoid versions: use dates instead**. Don't add things like `v1` or `final` to your filenames. If a document is likeley to have many versions use dates (eg. `2018-01-01-SomeDocument`), and remember that Google [has version history](https://support.google.com/docs/answer/190843). 
* **Follow existing conventions**. If you're adding something and all similar files seem to be named according to a convention, stick to it.

### Slack

Because we're a distributed team, we make heavy use of [Slack](https://zippyplane.slack.com) to collaborate. Everyone should have a profile picture and a username cossisponding to the first part of their email address. Here are the rules:

* Always create public channels, unless you have a *really good reason* to create a private channel, and always set the channel purpose.
* Prefer talking in public channels over DM - it lets everyone know what's goign on.
* Use threads and responses liberally - they help keep the channels clean.

We have a few noteworthy channels:

* **articles** - A place to share interesting articles.
* **builds** - A feed of notifications from our CI pipeline. All discussions in here should be in threads.
* **general** - Everyone is in here.
* **random** - Anything goes.

Right now, we have very few conventions in slack. We'll add them here as they develop.


##### Reaction Conventions

You can use emoji reactions however you want, except for the following which have special meanings:

| Response | Meaning |
| -------- | ------- |
| 🏁 | I've resolved this request/action. |
| 👀 | I'm looking into this request/question. | 

### Airtable

In order to avoid "tool creep", we try to use [Airtable](https://airtable.com/) in place of other tools where we can. We currently use it for:

* [CRM](https://airtable.com/tblukruMzX2nA1JkS) - Managing our contacts and leads, as well as arranging customer interviews and user research sessions.
* [Asset Register](https://airtable.com/tblmdl7S9oWn0JExX) - Register of physical and virtual assets. This helps us comply with GDPR and paves the way for various security and data protection certifications.

Airtable is incredibly powerful, and has the added advantage that it can connect to Zapier and expose its data over an API.If you find yourself looking at a new piece of software, ask yeself wether you could replicate its functionality in Airtable.

#### Airtable vs Google Sheets

Use **AirTable** for structured, long-lived or connected data that is likeley to change or be added to. Eg:

* Scheduled/past retrospectives
* Social Media content management
* Expenses Records
* Product Roadmaps
* Bugs / Defects

Use **Google Sheets** for short-lived, messy data, or data that is unlikely to change. Eg:

* Schedule for a meeting or hack-day
* One-off analysis of specific data
* Financial projections

Often, data will start in a Google Sheet and move to an Airtable as the optimal structure becomes clearer.

### Zapier

We don't currently use Zapier but expect to use it heavily as we grow, to automate numerous business and operational tasks.

### MailChimp

We don't currently use Mailchimp, but expect to manage our mailing list and drip campaigns with it in the future.

### Trello

We use Trello extensively to manage our work. We tend to use it as a freeform tool, with very few rules and conventions. When we need more structure, we reach for Airtable.

* [Acme Trello](https://trello.com/acme/home)

### 1Password

We don't currently use [1Password for Teams](https://1password.com/teams/), but will as soon as we need to share login details between more than a few people.

We **strongly suggest** that you use it (with a personal vault) to manage your own passwords.

### GitHub

Most of our code is hosted on BitBucket, but we also use GitHub for open source projects and for this playbook.

* [Github Organization](https://github.com/Acme)

There is one [Contributors](https://github.com/orgs/ZippyPlane/teams/contributors) team, which has push access to all repos. Note that you must enable 2FA in order to join the Acme organisation.

### BitBucket

Most of our closed-source code is hosted on BitBucket. 

* [Bitbucket Team](https://bitbucket.org/zippyplane/)

There are two User Groups:

* **Administrators** - Admin access to all repos.
* **Developers** - Push access to all repos.

### Zoom (and Slack Calls)

As a distributed team, we rely heavily on videoconferencing software to communicate and pair. For quick voice calls we prefer slack.

For longer calls, screensharing or calls with many participants, we prefer [Zoom.us](https://zoom.us/). It tends to be more reliable than Slack.

> **📝 NOTE**: For remote pairing, we reccomend either Slack (once we start paying for it), or [VSCode LiveShare](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare) alongside a Zoom call.

### DigitalOcean

TBA

### Gallery.io

[Gallery](https://gallery.io/#my-projects) is a tool from Google for collaborating on designs, mochups and images. We use it as a place to store inspiration, screenshots and mockups.

### DNS

TBA

### Software to Download

You should consider installing the following software on your devices:

#### Desktop (Mac)

* Slack for Desktop
* Airtable for Desktop
* Trello for Desktop
* 1Password
* Zoom
* Odrive or Google Drive File Stream

#### Mobile

* Slack
* Airtable
* Google Drive
* Google Docs
* Google Sheets
* Google Slides
* Trello
* 1Password
* [Gallery.io](https://gallery.io/apps)

## Security

Security is really important to us. While we care about the security of our business data, we're more concerned with the security of our **customers personal data**. Having stong, well-documented security policies and practices protects us from potential litigation, and also makes it far easier for us to attain accreditation in the future.

> **📝 NOTE**: Engineering has its own set of practices relating to security and data protection. They're not detailed here.

#### Geenral Principles

1. **Just be sensible.** Don't leave a USB stick on the train. Don't read sensitive documents where someone might snap a photo them.
2. **It's on you.** Security is everyone's responsibility. "It's not a dirty word, Blackadder".


#### Online Software

By using web apps like GSuite and Airtable to manage most of our information, we shift much of the responsibility to them – so long as we follow a few simple rules:

1. Use a long, strong password for your 1Password master key.
2. Always use strong, long passwords – generated by 1Password.
3. Never reuse passwords.
4. Always enable 2FA where available, prefering app-based auth over SMS-based auth.
5. Avoid storing information (particularly customer data) on your devices.
6. Periodically [check your Google account for third-party apps you no longer use](https://myaccount.google.com/u/3/permissions?pageId=none) and remove them.

#### Asset Register

All software and hardware used for work must be recorded in the [Asset Register](https://airtable.com/tblmdl7S9oWn0JExX). Any software that has access to customer data will be audited in accordance with our security policy.

#### Laptops

If you are using a mac, take steps to secure your machine:

* Set a strong login password.
* Set your laptop to lock automatically after a few minutes.
* Turn on Touch ID if you have it.
* Switch FileVault On.
* Turn the Firewall on and enable Stealth Mode.
* Keep software up-to-date.
* Install [AntiVirus software](https://www.avira.com/en/free-antivirus-mac).
* Install an AdBlocker for your browser.

#### Mobile Devices

We don't currently enforce security rules on mobile devices but if you use them for work, you should:

* Install [AntiVirus software](https://www.avira.com/en/free-antivirus-ios).
* Set a long passcode.
* Turn on Touch ID if you have it.
* Keep software up-to-date.
* Set your phone to lock after a few minutes.

#### Physical Security

* Don't write sensitive data on whiteboards or notepads.
* Avoid printing whenever you can.
* Avoid USB sticks (and other removable media) whenever you can.
* Shred all printed material when no longer needed – don't just throw it in the bin!
* Keep your desk/working area clean and tidy, and have a lockable cabinet for storing notebooks and bits of paper.

#### Incident Reporting

Any security or data protection incidents should be immediatly reported to danny@rootpath.io.com. This includes near misses and potential vulnerabilities.

<img src=https://github.com/i5ik/ViewFinder/raw/boss/.github/26881_DOSY_PP-01.png width=100%>

<div align=center>
<a href="https://www.producthunt.com/posts/come-browse-with-me?utm_source=badge-featured&utm_medium=badge&utm_souce=badge-come-browse-with-me" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=294970&theme=dark" alt="Come browse with me - Invite others to browse with you | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a><a href="https://www.producthunt.com/posts/viewfinder-pro?utm_source=badge-featured&utm_medium=badge&utm_souce=badge-viewfinder-pro" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=311208&theme=dark" alt="ViewFinder Pro - Virtual browsers you embed in your web app | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a><a href="https://www.producthunt.com/posts/iso-1?utm_source=badge-featured&utm_medium=badge&utm_souce=badge-iso-1" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=242265&theme=dark" alt="ISO - Isolate dangerous sites and docs in your browser | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a><a href="https://www.producthunt.com/posts/viewfinderjs?utm_source=badge-featured&utm_medium=badge&utm_souce=badge-viewfinderjs" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=284819&theme=dark" alt="ViewFinderJS - A secure browser you embed in your webapp | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a>
</div>


<div align=center>
  <a href="https://hub.docker.com/r/dosyago/browsergapce" target="_blank"><img src="https://img.shields.io/docker/pulls/dosyago/browsergapce" alt="Come browse with me - Invite others to browse with you | Product Hunt" style="width: auto; height: 40px;" height="40" /></a><a href="https://www.npmjs.com/package/remoteview" target="_blank"><img src="https://img.shields.io/npm/v/remoteview" alt="ViewFinder Pro - Virtual browsers you embed in your web app | Product Hunt" style="width: auto; height: 40px;" height="40" /></a><a href="https://www.npmjs.com/package/remoteview" target="_blank"><img src="https://img.shields.io/npm/dt/remoteview" alt="ISO - Isolate dangerous sites and docs in your browser | Product Hunt" style="width: auto; height: 40px;" height="40" /></a><a href="https://hits.seeyoufarm.com" target="_blank"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fc9fe%2FViewFinder&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=%28today%2Ftotal%29%20visitors%20since%20Oct%2027%202020&edge_flat=false" alt="ViewFinderJS - A secure browser you embed in your webapp | Product Hunt" style="width: auto; height: 40px;" height="40" /></a>
</div>

# [:camera: ViewFinder](https://github.com/i5ik/Viewfinder) 

Viewfinder is a virtualized browser, running in your browser! Run it on our cloud, or bring your own.

**Main advantages over other RBI, using VNC/Remote Desktop, Browserless debug console, or custom inspection solutions:**

- Source-available and readily demo-able by cloning this repo, unlike other RBI solutions
- Faster and more adaptive to bandwidth degradation that VNC and remote desktop, so delivers you responsivness that VNC cannot and reduces lag relative to Remote Desktop in tight bandwidth conditions.
- More extensive than Browserless debug console (VF includes remote debugging UI (the standard Chrome DevTools frontend you get with a regular browser), but also includes things that Browserless does not support such as multiple tabs, file uploads and downloads, sound, advanced adaptive streaming, and other "regular browser" features not supported by the more limited interactivity available with Browserless browser viewport inspection.
- Custom inspection solutions must encounter many issues that are already solved in this software, and expend time and effort developing their own solutions and keeping them up to date, there's no need to duplicate that expertise if you can purchase it.

-----------------------------------

This means VF is clientless browser isolation (a.k.a an embeddable BrowserView). You can also think of it as secure Chrome-as-a-service. This source-available version is free for personal use (see [the Polyform Strict License](LICENSE.md)). The Pro version (not source-available) has advanced features, like variable-rate adaptive streaming to minimize lag, remote DevTools, built-in instant messaging as well as co-browsing. 

VF is like S2, WebGap, Bromium, Authentic8, Menlo Security and Broadcom remote cloud browser offerings, but free for personal use and source-available. Plus, the Pro version has many advanced features not offered by those competitors. 

In addition, integrated secure document viewing with content-disarm and reconstruction (CDR) is available from [p2.](https://github.com/dosyago/p2%2e) for either version. [Contact me](mailto:cris@dosycorp.com?subject=ViewFinder%20License) for more information, or see the [license options](#license) below. 

## Offerings

While many customizations are availalbe, VF is available in 3 distinct flavors:

- VF CE, ViewFinder "Community Edition", which is this repository
- VF Pro, a closed-source edition based on VF CE, with more advanced features including elastic scalability and adaptive streaming
- VF Personal, your own fully managed VF Pro instance for personal use. [Read more about that here](https://personal.dosyago.com) or see the [Personal](#personal) section below.

The rest of this README covers VF CE and VF Pro, including how the licenses available for each.

**NOTE: if you'd like to get a hold of a release of Community Edition for personal use, I am currently revamping the release flavors and right now the best way is to either clone this repo, or get a Docker image (listed below). The latest NPM release is untested and binary releases are not available right now, so best to clone the repo or pull the Docker image. Thanks!**

## What is browser virtualization?

Also known as remote browser isolation, or "cloud browsers", this technology was originally a security layer implementing the isolation model to isolate web-based threats from your network and device by running all web content on a remote, lightweight server: the browser isolation server. But the technology behind virtualizing just browsers (not entire Desktops) enables so much more than just security--it creates a whole set of applications where browsers can be embedded in regular web apps. The ViewFinder application implements a feature-complete, clientless (meaning you don't need to download anything, as it is entirely served as a web app) remote browser isolation. 

Some ways to you might like to think about what ViewFinder is. ViewFinder is:

- a web UI for for headless Chrome (also can work with other browsers that support the DevTools protocol)
- a browser interface that runs in client-side JavaScript and HTML and connects to a browser running locally or on a server
- a platform to build enhanced browsing atop of, including capabilities like: co-browsing, secure document viewing, no-code automation
- a free and source-available implementation of remote browser isolation
- a way to view automations you're running with puppeteer, playwright or using the DevTools protocol natively. 
- a double web proxy or reverse proxy system for the whole web.

This repository is the source-available version of ViewFinder, otherwise known as ViewFinder Community Edition. It is feature complete but contains less features and less advanced capabilities compared to the closed-source ViewFinder Pro version, otherwise known as VF Pro.

**What's the Pro version?**

Pro version is an updated version of this free, and source-available "community edition" version, that includes many enhancments including:

- co-browsing support for any number of clients
- advanced "adaptive variable rate"  streaming for optimal quality over a wide range of bandwidth conditions
- chat panel for co-browsing participants
- open DevTools to inspect remote pages
- run puppeteer scripts in a secure sandbox
- scale up to run multiple browsers on a single server
- control CPU, memory and bandwidth resource usage
- additional security and performance enhancements

You can license the Pro version for your product, or license the source-available version with a license upgrade to avoid the  PolyForm Strict License 1.0.0
[Contact Dosycorp about a license](mailto:cris@dosycorp.com?subject=ViewFinderJS%20License&body=Hello%20Cris)

[Have a little look at the latest features to land on Product Hunt](https://www.producthunt.com/posts/puppeteer-console)

[Product Hunted x 3](https://www.producthunt.com/posts/viewfinderjs/maker-invite?code=wMxcDN) https://www.producthunt.com/posts/viewfinder-pro

If you use or like this, don't forget to show your appreciation by [starring this repo](https://github.com/i5ik/ViewFinderJS/stargazers), or [following me](https://github.com/i5ik) 😹 (*or upvoting the below PHs)



**What is this, in a (admittedly quite large) nutshell?**

**ViewFinder** is a programmable virtualized browser for web apps. You can run it to serve your own remote browser isolation, integrate it as an embeddable BrowserView to permit cross-site process coordination, or build it into your tooling to give you greater visibility into your browser automation jobs, and keep a human-in-the-loop to intervene if a job gets stuck or requires manual input. The source available version offered here is a scaled down, simplified version of the more advanced, and full featured Pro version, which includes variable bandwidth streaming for optimal user experience as well as and co-browsing to enable use cases like real-time interactive support and training using a shared browser. 

As it enables RBI and CBII, ViewFinder is like CloudFlare Cloud Browsers, S2, WebGap, Bromium, Authentic8, Menlo Security and Broadcom RBI, but the difference is ViewFinderJS is free and source-available. ViewFinderJS also lives in another space, because it's a fully programmable browser that you can connect to your existing browser workloads, powered by Puppeteer or your own custom automation logic. In this way it's similar to [Browserless](https://browserless.io), but different in that it's also serving a niche that needs a more complete browser experience with multiple tabs and same-as-native-browser UI and UX. Where Browserless focuses almost entirely on automation, ViewFinderJS is a platform for building many tools and apps on top of, from automation, internal tooling, to RBI and live support and training. 

Similarly to Browserless, ViewFinder source code is publicly inspectable, and if you need it with a less restrictive license, you can purchase an upgrade via links in this README, or [via email](mailto:cris@dosycorp.com?subject=ViewFinder%20License&body=Hello%20Cris), where you can also upgrade to the Pro version to access the more advanced features and a range of flexible licenses, maintenance contracts, deployment, delivery and custom development options to power your business. 

Both source-available and Pro versions support secure document viewing with CDR from https://github.com/dosyago/p2%2e but you'll need to set that up yourself for the source-available version, while the Pro version includes this. 

# Personal

VFPersonal is a range of bespoke 
remote browsers, for personal use.

VFPersonal lets you browse the web
safely and securely without exposing
your device to malware, ransomware,
or 0-day exploits.

## Features of VFPersonal

  - Adaptive streaming optimizes 
    latency
  - DevTools panel for remote
    access to browser DevTools 
  - Use from mobile or
    destkop with any modern browser
  - Built-in secure document viewier
  - Built-in live co-browsing and chat
    for collaboration
  - Fully-encrypted 'pixels-only',
    clientless RBI 
    
## Try it out

Sign up now and we'll get you set up in a couple of days (or hours, depending on how busy we are) with your very own instance running the Pro teir that you can use yourself. [Try VFPersonal for USD15 a month](https://buy.stripe.com/dR615g7hL0Mjeek5kx)
    
## Where is it hosted? 

VFPersonal is currently hosted on Vultr. Vultr provides great cloud services at an affordable price. I switched to them after being a loyal customer of other large cloud computing platforms. If you have a need for cloud infrastrucutre, you should definitely check them out with one of my referral links. The below links are my referral links. 

- [Check out Vultr](https://vultr.grsm.io/iyiikd389y9k)
- [Try Vultr with a USD100 free-credit (limited time only)](https://www.vultr.com/?ref=8967641-8H)
- <a href="https://www.vultr.com/?ref=8967639"><img src="https://www.vultr.com/media/banners/banner_300x250.png" width="300" height="250"></a>


----------------------

- [Overview](#camera-viewfinder----)
  * [Get started](#very-very-quick-install)
  * [License](#license)
  * [About](#about)
  * [Contributing](#contributing)
  * [Releases](#releases)
  * [Managed API: `VF.openSecurely(url: URI)`](#managed-api-vfopensecurelyurl-uri)
  * [Try it out](#try-it-out)
  * [Normal Browser UI things that work](#normal-browser-ui-things-that-work)
  * [Normal Browser UI things not yet implemented](#normal-browser-ui-things-not-yet-implemented)
  * [Advanced things only BG does](#advanced-things-only-bg-does)
  * [Some ways people are using ViewFinder](#some-ways-people-are-using-viewfinder)
  * [Major bugs](#major-bugs)
  * [localhost:8002](#localhost-8002)
  * [Get and self-host](#get-and-self-host)
  * [Easy install trouble shooting](#easy-install-trouble-shooting)
    + [Windows systems (and Mingw and Cygwin)](#windows-systems-and-mingw-and-cygwin)
    + [Binaries](#binaries)
    + [Safari](#safari)
  * [Docker build](#docker-build)
  * [Headless Detection](#headless-detection)
  * [In depth](#in-depth)
  * [Managed Cloud Service (available now)](#managed-cloud-service-available-now)
  * [Secure Cloud Based Internet Isolation](#secure-cloud-based-internet-isolation)
    + [Set up using a blank machine (running Linux)](#set-up-using-a-blank-machine-running-linux)
    + [Docker](#docker)
  * [Awesome](#awesome)
  * [Opening DevTools](#opening-devtools)
  * [Connecting puppeteer](#connecting-puppeteer)
  * [Other Similar Projects](#other-similar-projects)

------------------------
## Very Very Quick Install

```shell
$ curl -o- https://raw.githubusercontent.com/i5ik/ViewFinderJS/6ddbc6b312d4795a557ea14aa9037ccc254be339/quick_script.sh | bash
```

## Very Quick Install

```shell
$ echo Update distro
$ sudo apt update && sudo apt -y upgrade
$ echo Install tools
$ sudo apt install -y curl wget git
$ echo Install node version manager
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
$ echo Load NVM
$ source $HOME/.profile
$ source $HOME/.nvm/nvm.sh
$ echo Install latest NodeJS
$ nvm install --lts
$ echo Install latest Node Package Manager
$ npm i -g npm
$ echo Setup ViewFinderJS
$ git clone https://github.com/i5ik/ViewFinderJS.git
$ cd ViewFinderJS
$ npm i
```

Follow the prompts. :)

# License

## CE Licenses

The code in this repo (VF CE, "Community Edition") is licensed under PolyForm Strict License 1.0.0 (no modification, no distribution, no commercial use). [Read the license here.](https://github.com/DOSYCORPS/polyform-licenses/blob/1.0.0/PolyForm-Strict-1.0.0.md). You can upgrade your perpetual CE license to the following license options via these purchase links:

- [Buy a Perpetual Non-commercial Use License of the current CE Version re-upped Monthly to the Latest CE Version, USD$2 per month](https://buy.stripe.com/4gw15g8lP1Qn9Y414u) [Read license](https://github.com/DOSYCORPS/polyform-licenses/blob/1.0.0/PolyForm-Noncommercial-1.0.0.md)
- [Buy a Perpetual Internal Use License of the current CE Version re-upped Yearly to the Latest CE Version, USD $3000 per year](https://buy.stripe.com/28odS26dHeD9b2814q) [Read license](https://github.com/DOSYCORPS/polyform-licenses/blob/1.0.0/PolyForm-Internal-Use-1.0.0.md)
- [Buy a Perpetual Shield License of the current CE Version re-upped Yearly to the Latest CE Version, USD $60500 per year](https://buy.stripe.com/bIY01c31v7aHfiobJ5) [Read license](https://github.com/DOSYCORPS/polyform-licenses/blob/1.0.0/PolyForm-Shield-1.0.0.md)

## Pro Licenses

VF Pro comes with better streaming and more advanced features including:

- Adaptive streaming to deliver reliable responsivness over a wider range of real-world bandwidth conditions
- Improved security and scalability to multiple machines or multiple browsers on a single machine, including resource and bandwidth controls
- Secure co-browsing to empower multiple collaborators to browse and chat about the same tabs at the same time
- Built-in remote secure DevTools access (developer tools) to allow secure remote access to the internal components of the viewed tabs
- More rapid update cycle than the source-available community edition version

**Purchase a Pro license**:

VF Pro is only commercially licensed through a variety of Polyform licenses, which you can purchase using the following purchase links. Each purchase includes free install (into your own infrastructure or cloud, but managed options are available), and 2 months of free support and deployment help (after which you can purchase various support tiers, and custom development).

- [Buy a Perpetual Internal Use License of the current CE & Pro Version re-upped Yearly to the Latest Versions, USD $12000 per year](https://buy.stripe.com/aEUeW659D66D6LS00o) [Read license](https://github.com/DOSYCORPS/polyform-licenses/blob/1.0.0/PolyForm-Internal-Use-1.0.0.md)
- [Buy a Perpetual Shield License of the current CE & Pro Version re-upped Yearly to the Latest Versions, USD $85000 per year](https://buy.stripe.com/8wM4hseKdeD9b28aEZ) [Read license](https://github.com/DOSYCORPS/polyform-licenses/blob/1.0.0/PolyForm-Shield-1.0.0.md)
- [Buy a Perpetual Perimeter License of the current CE & Pro Version re-upped Yearly to the Latest Versions, USD $110000 per year](https://buy.stripe.com/aEU01c8lPeD95HOeVe) [Read license](https://github.com/DOSYCORPS/polyform-licenses/blob/1.0.0/PolyForm-Perimeter-1.0.0.md)
- [Buy a Perpetual SMB License of the current CE & Pro Version re-upped Yearly to the Latest Versions, USD $185000 per year](https://buy.stripe.com/7sI9BM59D0Mj9Y4aEX) [Read license](https://github.com/DOSYCORPS/polyform-licenses/blob/1.0.0/PolyForm-Small-Business-1.0.0.md)

## About

The VF series of products are feature-complete, clientless, remote browser isolation products (RBI), including secure document viewing (CDR), built in HTML/JavaScript that runs right in your browser. Integrated with a secure document viewer (available on request), this can provide safe remote browser isolation at deployments of any size. It also saves you bandwidth (on the last hop, anyway).

With ViewFinder, in order to render the content of a web page, the only thing we send to your device from the remote page is pixels. So no HTML, CSS, JavaScript, etc from your browsing is ever executed on your device.

[What is RBI / CDR?](https://hackernoon.com/zero-trust-browsing-to-reduce-cybersecurity-job-fatigue-7ce72a633d4)

![Animated GIF of ViewFinder in action](https://j.gifs.com/E8yzLv.gif)

**You see that? :point_up: That's a browser running in your browser. All those tabs and UI, that's all ViewFinder. It's sending you pixels from a remote browser, running anywhere.**

You can use this repo to play with a browser running remotely in the cloud, rather than on your own device. Useful for security and automation. 

If you're a developer you can include a "BrowserView" in any other web application (for non-commercial use only).

If you're like to deploy this in your org, or for a for-profit project, write me: cris@dosycorp.com Or keep an eye out for the cloud service, coming soon. Official government use OK without purchase (also for university/public institution researchers, journalists and not-for-profits), as long as deployment is done in-house (or using Dosyago Corporation, not by other contractors, nor part of a paid deployment). If you're in government and you'd like to deploy this and want help, contact me for help or to discuss a deployment contract.

## Contributing

Hi there! :wave: :smiley: It's great that you'd want to contribute, but unfortunately I'd need you to sign a CLA which you might consider an issue :biohazard: I'm sorry, I'm sure you probably feel this is a stupid and inconvenient burden for you. If that is not impossible for you tho, and you're cool with that, then email me or please know that your PR will be closed unless you sign that. If you want to sign a CLA, have a read of it and if it's acceptable to you, sign it so you can contribute. In general terms, a CLA is a transfer of copyright and all rights (even moral rights) to your contributions to me and my company. The reason for this is to ensure there are no risks to me to license or sell this version to customers or others in future.

## Releases

[Get the latest binary release](https://github.com/cris691/ViewFinder/releases)

- Embed a browser in another web application to integrate user flows.
- Isolate your network from the risks of the public internet by running browsers in a remote machine.
- Protect your network from [Browser Zero-day exploits](https://www.radsix.com/dashboard1/)

[For more info at on fully managed versions, email me](mailto:cris@dosycorp.com?subject=ViewFinder%20Managed&body=Hello%20Cris)

## Managed API: `VF.openSecurely(url: URI)`

An API to open a link in a secure remote browser context. Calling the below in the browser will open a new tab.

```js
  import ViewFinder from './web_modules/@dosy/browsergapjs.js';
 
  const VF = ViewFinder('<my api key>');
  
  VF.openSecurely(url);
```

***News:*** VF.openSecurely was **featured** in ProductHunt.
OMG. Like Wow :rainbow: :joy_cat: I never got many likes on PH. And then suddenly it got SO MANY! :P :) xx (wow). And I didn't even check it until 2 months later I was going to PH for something else and I saw all these people voted. Yay. Here's..."The Badge":

If you want to see a demo of that in action, check out:  [schedule a demo](mailto:cris@dosycorp.com?subject=ViewFinderJS%20Demo&body=Hello%20Cris)

These APIs support the full package include secure document viewing. [Use the SDK](https://github.com/dosyago/browsergap.js)

## Normal Browser UI things that work

- Copy and paste (paste is as normal, but for copy you need to use the right-click context menu)
- File upload
- File download and CDR secure view (seamlessly integrated in licensed self-hosted, managed or per-session options)
- Modal dialogs
- New tabs
- History (invisible but you can navigate it with the forward and back buttons)
- Address bar search (defaults to Google but you can add your own)
- New incognito tabs 
- Clearing cache, history and session cookies
- Touch scrolling, track pad scrolling, mouse wheel and magic pad scrolling
- Desktop, tablet and mobile
- Form input (text, options, check boxes, etc)

## Normal Browser UI things not yet implemented

- Text selection
- Page zooming and pinch/spread zooming on mobile (implementation is buggy)
- Multi-touch on tablet and mobile
- Regular browser settings (language, default page scale, etc)
- Summary list of history entries
- WebGL (this is an open bug in Chrome headless)
- Multiple windows (you can sort of do this by opening the app in different tabs, and say opening all BG tabs in incognito mode, but it's not fluid)

## Advanced things only BG does

- Local and remote bandwidth indicator
- Secure browsing context (we only send you pixels from normal browsing, to protect you from exploits, malware and zero days)
- Fully functioning browser that you can embed in any other app on the open web (basically a `<browserview>` tag that works everywhere, and has the normal UI you expect from a browser)
- Control the resource usage of a pool of remote browsers, collectively and individually.
- Adaptively resamples images based on the bandwidth you have available on your connection, to maintain responsiveness and use the best image quality your bandwidth permits

## Some ways people are using ViewFinder

- To embed other applications in their own web app to unite separate user flows, and overcome iframe restrictions.
- As a browser proxy to enable secure browsing on locked down internal networks

## localhost:8002

By default (unless you provide command line arguments) it runs on port 8002.

## Get and self-host

Clone this repo

`git clone https://github.com/i5ik/ViewFinderJS.git`

Then run `npm i` in the repository directory, followed by `npm test` to start on the default port.

But you might like to `git fetch --all && git checkout nexe-build && git pull` to 
be on the branch that has all the latest additions just like in the Docker image, npm globals
and binaries.

or Install from npm 

`npm i -g remoteview@latest`

*Remember to follow the install prompt*

## Easy install trouble shooting

### Windows systems (and Mingw and Cygwin)

**Pre-requisites: Windows with Google Chrome already installed.**

If you're on Git Bash (or Cygwin, or Mingw) you might have trouble using `npm i -g remoteview@latest`.

Make sure you configure npm 

`npm config set script-shell "C:\\Program Files\\git\\bin\\bash.exe"`

Also, don't worry about running "setup_machine" at the prompt, because it uses `apt-get` which won't work on Windows anyway.

Normally, a Windows device with Chrome already installed won't need to run "setup_machine" anyway, which is a script to install things like fonts, graphics libraries and some utilities useful for running headless Chrome in linux.

### Binaries

**Pre-requisites: Windows, Mac OS or Linux with Chrome already installed.**

If you use a [binary](https://github.com/cris691/ViewFinder/releases/latest), make sure you have Google Chrome installed. You might also need to run the `setup_machine.sh` script, to make sure you have all dependencies of Google Chrome headless installed, but probably not if you have Windows.

### Safari

Safari requires TLS to use WebSockets with ViewFinderJS. In order to set that up you'll need to get yourself some TLS certificates, and copy them to the `/sslcert/master/` directory. Then run as usual using `npm test` or `npm start`.

## Docker build

[Get it on docker hub](https://hub.docker.com/r/dosyago/browsergapce), and see instructions below.

## Headless Detection

Even tho RV uses headless Chrome, it attempts to conceal that fact. Sometimes, a service knows (such as Google, Google always knows). But other times the service cannot tell. For some tests of headless, visit the following when using RV:

- [Detect headless](https://infosimples.github.io/detect-headless) :heavy_check_mark:
- [Are you headless?](https://arh.antoinevastel.com/bots/areyouheadless) :heavy_check_mark:

## In depth

ViewFinder is a platform for live streaming the browser, with full interactivity. It lets you plug in to a local or remote, even a headless browser, and fly it as if it's a normal browser. 

You can stream a remote browser with special customizations to your clients to side step the restrictions of regular browsers. You can use it to build rich experiences based on the browser that are not possible using Flash, Browser Extensions or regular Web Driver protocol. 

For business enquiries, please contact [Cris](mailto:cris@dosycorp.com?subject=ViewFinder)

[Watch the 16 second video](https://www.youtube.com/watch?v=SD0Fhl9v87k).

ViewFinder is a HTML/CSS/JavaScript "outer shell" for a browser. It also looks and works just like a browser, but it runs in your browser and controls another browser.

![browser in a browser](readme-files/tenor.gif)

## Managed Cloud Service (available now)

Login at https://dosyago.com and purchase a license. 

Try a session now for $3.81, first:

- https://comebrowsewithme.com

Contact [Cris](mailto:cris@dosycorp.com?subject=ViewFinder) for questions.

## Secure Cloud Based Internet Isolation

[Read more here](remote-browser-isolation.md)

### Set up using a blank machine (running Linux)

First set up the machine with git, and node (including nvm and npm) using the below:

If you want to speed up install and it hangs on `processing triggers for man-db` you can remove all your man pages (**WARNING**), with:
`sudo apt-get remove -y --purge man-db`

alternately, somebody reported they had luck with passing a `--force` to the apt command that seems to hang.

```shell
$ echo Update distro
$ sudo apt update && sudo apt -y upgrade
$ echo Install tools
$ sudo apt install -y curl wget git
$ echo Install node version manager
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
$ echo Load NVM
$ source $HOME/.profile
$ source $HOME/.nvm/nvm.sh
$ echo Install latest NodeJS
$ nvm install --lts
$ echo Install latest Node Package Manager
$ npm i -g npm
$ echo Setup ViewFinderJS
$ git clone https://github.com/i5ik/ViewFinderJS.git
$ cd ViewFinderJS
$ npm i
```

Then install and run VF from source:

```sh
git clone https://github.com/c9fe/ViewFinder
cd ViewFinder
npm i
npm test
```

If you'd like more control (over say the ports that Chrome and the web app run on, you can pass those
parameters to the `start.sh` script, which has the following signature:

```sh
./start.sh <chrome_port> <app_port> <cookie_name> <username> token2
```

*Note: the audio port is always 2 less than the app_port*


### Docker 

*Note: running from docker image means you have no sound*

You can pull an existing image from docker hub (already [![docker pulls](https://img.shields.io/docker/pulls/dosyago/browsergapce)](https://hub.docker.com/r/dosyago/browsergapce))

```sh
docker pull dosyago/browsergapce:2.6
```

And then run it 

```sh
curl -o chrome.json https://raw.githubusercontent.com/c9fe/ViewFinder/master/chrome.json
sudo su -c "echo 'kernel.unprivileged_userns_clone=1' > /etc/sysctl.d/00-local-userns.conf"
sudo su -c "echo 'net.ipv4.ip_forward=1' > /etc/sysctl.d/01-network-ipv4.conf"
sudo sysctl -p
sudo docker run -d -p 8002:8002 --security-opt seccomp=$(pwd)/chrome.json dosyago/browsergapce:2.6
```


You can also build a docker image from source yourself (you probably want to be on the nexe-build branch, tho).

Set up the machine (as above in the **Set up** section), then

use clone the repo and install docker (`build_docker.sh` will do that for you) and build yourself an image:

```sh
git clone https://github.com/i5ik/ViewFinder
cd ViewFinder
git fetch --all
git branch nexe-build
./build_docker.sh
./run_docker.sh 
```

And visit http://&lt;your ip&gt;:8002 to see it up.

## Awesome

Coming here from [Awesome Chrome DevTools](https://github.com/ChromeDevTools/awesome-chrome-devtools) or [awesome-puppeteer](https://github.com/transitive-bullshit/awesome-puppeteer)? 

Take a look at the [Zombie Lord connection](https://github.com/c9fe/ViewFinder/blob/master/zombie-lord/connection.js) and [Translate Voodoo CRDP](https://github.com/c9fe/ViewFinder/blob/master/public/translateVoodooCRDP.js).

## Opening DevTools

Just connect your browser to http://localhost:5002 from the machine you run it on.

## Connecting puppeteer

Just run PPTR on the same machine as this and connect to http://localhost:5002

## Other Similar Projects

- [Remote Browser](https://github.com/bepsvpt-me/remote-browser) - Use WebRTC to stream remote server puppeteer. Also, seems [that project was inspired by VF](https://learnku.com/nodejs/t/37088).

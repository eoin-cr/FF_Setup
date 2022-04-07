# FF_Setup
A file detailing my firefox privacy setup

I am a strong advocate for privacy against online tracking and
the like, and have a large amount of extensions and changes to
firefox settings.  Some extensions are for the benefit of privacy,
and some just improve the user experience.

As you increase user privacy, the convenience of some sites may reduce.
I will detail how much of an impact each extension and change makes so
you can choose for yourself.

## Contents
* Extensions
  * Extensions that I have enabled
    * Privacy
    * Bypassing Paywalls
    * Misc
  * Extensions I have disabled
* Firefox about:config changes
* Other privacy tips

---

# Extensions
NOTE: For all these extensions I will just be talking about extensions
that I have on Firefox.  Firefox is the best mainstream browser for 
privacy, and just overall IMO.  Chrome, Edge, Brave, etc, are all far
worse in terms of privacy, and I would recommend against using them.
## Extensions that I have enabled
### Privacy
#### ClearURLs
Many websites use tracking elements in the URL (hence why the urls on
Amazon are often so long).  This extension removes the tracking elements
contained in the URL and leaves just the base URL.

This is pretty good for privacy, and does not hamper convenience at all,
you will probably forget you even have it installed.  It will also make
copying links easier as they aren't so ridiculously long.

https://docs.clearurls.xyz

#### Consent-O-Matic
Rather than having to choose which cookies and the like you want on every
site you visit, this add on remembers your choices, and automatically inputs
them for you.

Good for privacy, and getting rid of all the annoying popups begging you to
agree to be tracked.  Doesn't hamper the user experience at all, another
extension you will forget you even have installed.

https://github.com/cavi-au/Consent-O-Matic

#### Decentraleyes
Many websites nowadays use 3rd party websites for content delivery,
which can be used for tracking.  This extension works to prevent this
from happening.

Good for privacy, and doesn't affect the convenience at all.

https://decentraleyes.org

#### Disconnect
Disconnect removes trackers, and claims to make pages load faster as
a result.

Never had any issues with it, seems good for privacy too.

https://disconnect.me/

#### Facebook Container
Opens facebook pages into container windows, so they are unable to
interact with or track anything outside the container.

Good for stopping facebook tracking, can be annoying to go back out of
a page by hitting the back icon I suppose but fine otherwise.

https://github.com/mozilla/contain-facebook

#### Firefox Relay
Creates email aliases that forward emails to your real inbox.  This
creates a degree of separation between all your accounts.  

Can be convenient but you can only create 5 aliases for free, you have
to pay for premium for unlimited ones.

https://relay.firefox.com/

#### HTTPS Everywhere
An extension that warns you if you are trying to access a HTTP site
(HTTP sites are far more insecure and send information such as passwords
in plaintext), and tries to automatically convert HTTP sites to HTTPS.

Not really needed anymore as basically every site uses HTTPS and most
browsers will warn you if you're trying to access a HTTP site anyway.

Slightly inconvenient if you're trying to access a HTTP site ig?  But
really you shouldn't be doing that so it's an extension you should have
if your browser doesn't have it already.

https://www.eff.org/https-everywhere

#### NoScript
JavaScript can reveal a huge amount of information about the computer
you're using to browse the web, making fingerprinting and tracking very
easy.  It is also used for tracking pixels and the like.  Overall, you
probably want to avoid JS when it's not necessary for a website.

This is probably one of the most inconvenient extensions.  Websites will
often not work without you enabling JS, and sometimes a certain functionality
you want will use some third party JS.  This can be very annoying if that site
uses a large amount of third party JS as you will have to go through the list
and figure out what you need to enable to fix the website.  Although
inconvenient, this is very privacy beneficial.

https://noscript.net

#### Privacy Badger
Automatically blocks invisible trackers based on their behaviour.

Good for privacy and does most of the stuff under the hood.

https://privacybadger.org/

#### Temporary Containers
Allows you to open sites in disposable containers.  Very convenient
for having multiple different accounts from one website open in one
browser, or just for keeping your work, shopping, etc, all separated
to avoid tracking.

https://github.com/stoically/temporary-containers

#### Terms of Service; Didn't Read
Displays a little icon in the URL bar which shows a grade for a website's
terms of service and privacy policy, as well as a quick and simple
breakdown when you click on the icon.

https://tosdr.org

#### uBlock Origin
The best content/ad blocker.  If you're currently using Adblock or Adblock
plus, get rid of it.  Not only is uBO better for privacy, and is more
lightweight, but it also blocks all ads.  Not everyone knows this, but
Adblock plus displays ads if the advertising company pays them.

uBlock Origin also has a huge amount of privacy and annoyancy lists,
as well as having JS blocking options built in (I personally use
NoScript to block JS, but you could do it all from uBO if you wanted).

My filter list settings on uBO are as follows
* Auto-update filter lists, Suspend network activity until all filter
lists are loaded, and parse and enforce cosmetic filters are all enabled.
* All 6 built-in filters are enabled
* EasyList is the only Ads filter I have enabled
* I have the AdGuard Tracking Protection, AdGuard URL Tracking Protection,
and EasyPrivacy filters enabled
* I have the Online Malicious URL Blocklist enabled
* I have Fanboy's Annoyance and Fanboy's Social enabled
* I have Peter Lowe's Ad and tracking server list enabled

Overall fantastic extension, great for privacy, blocking malicious
pages, and blocking ads!

https://github.com/gorhill/uBlock#ublock-origin

---

### Bypassing paywalls
#### Bypass Paywalls Clean
Just as the name implies, it bypasses paywalls.  There is a very large
amount of websites that are bypassed.  The only annoyance I've had with
this extension is that it updates rather often, which is handy as it
introduces bypasses for more sites, but can be a tad annoying to update
so often.

https://gitlab.com/magnolia1234/bypass-paywalls-firefox-clean

#### uBlock Origin
I'm putting uBlock Origin here as well because some of the filter lists
you can enable on uBO can bypass paywalls.  For example the "AdGuard Tracking
Protection" and "AdGuard URL Tracking Protection" will allow you to
bypass the New York Time's paywall.

https://github.com/gorhill/uBlock#ublock-origin

#### Unpaywall
Unpaywall legally gets you the full text of research papers.

https://unpaywall.org/products/extension

---

### Misc
#### Buster: Captcha solver for humans
This extension solves reCAPTCHA challenges automatically for you.  It
uses speech recognition on the audio challenges.  I find this extension
works about a third of the time, however, I don't use it hugely often.
I wouldn't recommend using it after you have entered a large amount of
information, as sometimes if it fails you may have to refresh the page,
causing the inputted info to be lost.  However, it can be handy for just
solving captchas on sites that aren't too important

https://github.com/dessant/buster

#### Cookie editor
As the name implies, it allows you to edit the cookies on webpages.  Handy
for testing stuff and the like.

https://cookie-editor.cgagnier.ca/

#### Dark Reader
Automatically makes pages dark mode, and allows you to change the brightness,
contrast, etc.  Very nice if you don't like getting blinded by light mode.

https://darkreader.org/

#### DuckDuckGo Hide Unwanted Results
I noticed that often in my search results, the same few annoying spam websites
would come up occasionally.  This extension allows you to remove certain sites
you don't want to see from your search results quickly and easily.

Here are the domains I have hidden in case you're interested
* solveforum.com - fake stackoverflow, very annoying in that it
says certain questions are answered when they aren't.  Just uses 
a fuck ton of SEO to get views.
* javaer101.com - same as previous
* pvillage.com - same as previous
* readallbooks.org - fake free pdf site
* geeksforgeeks.org - their stuff isn't great and I'm not a fan of how it
requires signing in just to view stuff now

https://github.com/pistom

#### Firefox color
Just allows you to customise how firefox looks more

https://color.firefox.com

#### Greyscale browsing
Changes colours to greyscale, good for reading, and can be nice on the eyes
sometimes.

https://mcarolan.net/

#### OneTab
If you're anything like me you probably have a huge amount of tabs open at
one time.  This extension will close all your tabs and create a page with
links to all the tabs you had open.  Very handy if you don't want to close
tabs, as there's stuff you want to come back to quickly later, but also
don't want so many tabs open.

http://www.one-tab.com

#### Popup Blocker (strict)
Makes all popups request to appear first.  Useful for when you click
something by accident that tries to redirect you to another page.

https://add0n.com/popup-blocker.html

#### Return YouTube Dislike
As the name implies, this extension returns the ability to see dislikes
on youtube.  Although the YouTube API has stopped sending the dislike
counts, this extension now uses the dislike data of the users, as well
as archived data from before the dislike API shut down, to fairly
accurately predict how many dislikes a video had.  Great way to combat
the very annoying removal of dislikes.  Linus Tech Tips made a video 
showing how accurate it is so you can check that out if you're interested.

https://www.returnyoutubedislike.com/

#### SoundFixer
Allows you to fix annoying sound problems on YouTube and some other websites.
I personally haven't used it that much but it seems like it could be handy
sometimes.

https://github.com/unrelentingtech/soundfixer

#### SponsorBlock for YouTube
Uses submissions from users of the extensions to automatically skip
over sponsor segments in videos.  This extension works surprisingly well
and is very convenient.

https://sponsor.ajay.app

#### Tabliss
Just a nice little customisable new tab page, with a pretty background which
changes each time, a clock, and more.

https://tabliss.io

#### Universal Bypass
Bypasses all sites that make you wait before redirecting (e.g. adf.ly)
or make you do something (e.g., show.co and sub2unlock.com) and 
even trackers (such as bit.ly and t.co).  It will also prevent IP grabbers
from being used against you.

https://universal-bypass.org/

---

## Extensions I have disabled
Bitwarden - I've heard this is a good cloud password manager, but I don't
use it personally, I just use the default firefox one, paired with KeePassXC

Chameleon - Allows you to spoof your browser profile.  Good for privacy, but
causes an irritating glitch with youtube where the bottom half of videos is
obscured by a colourful grid thing whilst the time scroll bar is visible.

Ecosia - I like that it plants trees for the searches you make, but I've heard
it's not great for privacy.

I don't care about cookies - I think Consent-O-Matic is probably slightly better
for privacy.

User-Agent Switcher - Same as Chameleon


---

# Firefox about:config changes
Will be added at a later stage

---

# Other privacy tips
Will be added at a later stage
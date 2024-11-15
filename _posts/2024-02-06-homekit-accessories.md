---
layout: post
title: "HomeKit and Accessories"
slug: homekit-accessories
categories: software home-automation
date: 2024-02-06T10:12:37.968Z
---

<!-- (modified 2024-06-27) -->

I’ve been through a few iterations of home automation systems… Google Nest, Home Assistant + NodeRed, POE cameras, etc… I’ve tried a LOT of products, a LOT of setups, and dealt with a LOT of headaches (namely, the HomeAssistant setup).

## My Requirements

After many, many, hours of installing/uninstalling/troubleshooting different products and services, I have solidified my needs and requirements for smart home devices. Changing out devices every 6-12 months isn’t ideal; sadly, I made an expensive hobby out of it! Most people, however, can’t and don’t want to change out devices and try new services. After all, nobody likes change for change-sake. That’s why coming up with a list of requirements and what you really want from a system is crucial to finding the products you need to buy.

Here are my requirements for how I chose Apple’s HomeKit as a centralized standard for my home:

- **Privacy matters** - ask yourself, do you want a company to use your data for machine-learning? Do you want your photos, data, or private footage in the hands of anybody else, including law-enforcement?
- **On-prem** - as much “on-premises” processing as possible. Do you really want to rely on a company’s “good-will” to keep a service going? Countless times companies have shut down services for products within a few years of selling that product. Imagine, you bought a smart-thermostat that requires connection to their servers, and they decide to shut off those services. Now you can’t use your thermostat from your phone, maybe you can’t use it at all! Not to mention: SPEED. I previously had a Belkien smart switch that required cloud access. It could take many seconds for the device to respond to a request, or sometimes it'd not respond at all!
- **Quick & easy access** - everything all in one place, always: the Apple Home app. Let’s avoid this: open the Eve app to access outdoor cameras, open the Tapo app to access SOME indoor cameras, open the Aqara app to access the OTHER indoor cameras, open the Yale app to unlock the front-door, access the Abode app to set the home-alarm system, etc. See how terrible of a user-experience this would be?
- **Quick setup** - nothing to maintain, nothing to update (if you don’t want to).

***A little note on HomeKit Secure Video***:

Recording video on HomeKit Secure Video requires a subscription to iCloud+. They have different tiers of iCloud+, which allow more cameras to be recorded. And yes, yes, I know, “on-prem”… you can find HomeKit cameras that have on-device recording, or even recording to a NAS (Network Assisted Storage) such as the EufyCam 2 (but again, they have a bad privacy track-record), and you can’t view the recordings in Apple Home app. But even without the subscription to iCloud+, you still get access to notification alerts from cameras, which is 80% of the battle. Even with iCloud+, the cameras provide end-to-end encryption. Even Apple cannot view the recordings.

In addition, I’m already signed up for [Apple One](https://www.apple.com/apple-one/) which gives you the needed iCloud+ storage anyway.

## The Products

HomeKit doesn’t have as many products available to it as Google, and that’s okay. Apple has more requirements to maintain privacy, security, and an ensuring their ecosystem plays well with itself.

Sadly, with the lack of products available to HomeKit, you need to be very careful on where you put your money. That’s why I’ve compiled a living list of good products (and also a list of bad products) to use with Apple’s HomeKit ecosystem.

Getting the obvious out of the way, Apple's HomeKit requires at least one "Home Hub". This could either be [Apple HomePod](https://www.apple.com/homepod/) or [Apple TV](https://www.apple.com/apple-tv/). I've seen the community swear by the Apple TV being the designated Home Hub (although, you can only force it by nightly turning off the HomePods using an outlet switch). But I haven't noticed a huge difference, nor have I cared too much, and I just let the Apple magic happen.

### The Good

#### Security System

[**Abode**](https://goabode.com) (⭐️⭐️⭐️⭐️✨ 4.5/5) - doesn't require a subscription (but they have one if you want monitoring). Great reliability, fair amount of accessories. The contact sensors are always reliable, and can be used natively in HomeKit's Automation!

#### Outdoor Camera

[**Eve Outdoor Camera**](https://www.evehome.com/en-us/eve-outdoor-cam) (⭐️⭐️⭐️ 3/5) - okay, I’ll be honest, I’m still on the fence about these. Generally, I’d avoid Eve’s cameras when possible, Eve’s indoor camera is mediocre at best for a premium price, and has disconnect issues.

*I'm only listing the Eve Outdoor Cameras because I'm forced to. There's not really any other **reasonably priced** options for outdoor homekit cameras!*

Field of view is great, picture quality is great, floodlight can be a little finicky, you cannot turn on the floodlight like a light switch, wifi connection has to be impeccable otherwise you'll have connection issues.

Spend some time in the reviews for the Eve Outdoor Camera, you’ll see: difficult to install. Spend some more time in the reviews about ANY Eve Camera, you’ll then see that they all have problems with disconnecting.
I only choose the Eve Outdoor camera because these problems can be mitigated by disabling the motion sensor (or just changing the settings, resetting the device to factory, or just power cycling). The biggest problem that people have misunderstood, is that their WiFi connection is most likely the issue, not the Eve Outdoor Camera. Unfortunately, WiFi settings may be to blame for random disconnects; Eve Indoor Cameras are just plagued with their own disconnect issues…

(Update: after owning two of these for more than 6 months, they're very good... IF they're close to your WiFi signal. I think that might be the deciding factor: if you can have it mounted fairly close to a WiFi access point, you're golden. Mine just so happen to be 10ft and 20ft away from access points, with NO DISCONNECTS! It's also possible that Apple HomeKit has done some good software updates to fix video disconnect issues.)

#### Indoor Camera

TP-Link’s [**Tapo C125**](https://www.tapo.com/us/product/smart-camera/tapo-c125/) (⭐️⭐️⭐️⭐️ 4/5)

I’ve tried a few indoor cameras (see the **Bad Indoor Camera** list below). TP-Link has incredible track record with local devices for a fair price, and easy of use. That’s why I was excited when they released their HomeKit indoor camera.
The only note I have about this camera, is that the quality can be just slightly lacking (but really, not a big deal), there can also be some heavy compression artifacts that you may see on occasion. I'll still recommend this camera for it's reliability and it's price.

#### Garage Door Opener

[**Meross Garage Door Opener**](https://www.meross.com/en-gc/smart-garage-door-opener/garage-door-opener-remote-control/29) (⭐️⭐️⭐️⭐️⭐️ 5/5) - I often forget about this device because it’s just simple, seamless, and reliable. Installation wasn’t exactly easy, since there’s a long cable from the motor to the door sensor. But it’s been there a few years now with minimal problems (the problems, were likely with Apple’s designated Home Hub), where there might be a disconnection. This happens once every 6-12 months (on average), where I’d come home and try to open the garage door through Apple CarPlay, and the device wouldn’t respond. Likely a WiFi connection issue. Software setup was only a little annoying, just because I think it required that I create an account with them.

#### Doorbell Camera

[**Logitech Circle View Doorbell Camera**](https://www.logitech.com/en-us/products/cameras/circle-view-video-doorbell.html) (⭐️⭐️⭐️✨ 3.5/5) - everything has been very good about this doorbell camera, and I've owned a few!
Again look into the reviews on this one, you'll see a pattern: turns off in "high heat", but everyone agrees that it is too sensitive and shuts off when the ambient temperature is around 100°F (exacerbated when the doorbell camera is facing the sun). There's only so much you can do to mitigate this, for example, I've 3d printed out a white cover to deflect some of the heat, which has helped a little bit. But it's still a problem. Otherwise, it's a good doorbell camera.

#### Deadbolt Lock

[**Yale Deadbolt Locks**](https://yalehome.com) (⭐️⭐️⭐️⭐️ 4/5) - Yale tends to update their product-line a little too quickly for my liking. This makes product support (user-manuals) and product information difficult to navigate. They're fine deadbolts and as soon as you get them set-up and integrated into your Home app, they're very reliable and long-lasting battery life.

The installation is fair; you can't really make it easier for installing a deadbolt. But sometimes the locking mechanism might be slightly difficult to line up with your door frame, but with a little tinkering and adjusting, it's worth it.

You'll need to read the specifications of which door lock you get, to make sure that it's got integration into HomeKit (you might have to buy what they call, "Smart Modules"); and you want to try to avoid having what Nest x Yale has, which is a dongle thingy that you have to plug into the wall to get the deadbolt to talk to the smart-home. I also haven't tried anything with Apple Home Key yet just because I've got automations set-up to unlock the door and disarm the security system.

While I might recommend Yale for these deadbolt locks, I'm not convinced that there aren't better ones.

Also: Their app sucks.

#### Thermostats

[**Ecobee3 lite**](https://www.ecobee.com/en-us/smart-thermostats/) (⭐️⭐️⭐️⭐️✨ 4.5/5) - Go read the reviews, you'll see why this is everyone's favorite thermostat. Although it's a little more costly than what I'd like, it's still a great thermostat for what you need. And you don't need to connect to any cloud services (looking at you, Google Nest!).
(I wish HomeKit had some sort of way to manage the thermostat scheduling, but that is unrelated to Ecobee's implementation of the HomeKit.)
I've got two of these (upstairs and downstairs), set-up was as normal as everything else, and they do exactly what they're supposed to. Their interface on the thermostats are good.

The web user-interface is teetering on "clunky", but I'll give it a pass since the functionality is there and it works.
The only strange thing is that I'll notice that if it's trying to reach a temperature, it doesn't keep the fan on too long (I don't know if this is their, "Smart Recovery" mode in action or not); it almost seems like it's trying to reach that temperature gradually. This hasn't been enough of an issue to warrant a customer service call.
Speaking of their customer service: great! I had an issue with set-up on one thermostat (it was giving me some system error). They were quick, helpful, friendly, and knowledgeable; would love to call again.


[**Meross Thermostats**] - I have not tried the Meross thermostats. However, I'd be interested in trying more things from Meross, considering how good their Garage Door Opener has been.

#### Light Switches & Dimmers

TP-Link's [**Kasa switches & dimmers**](https://kasasmart.com) (⭐️⭐️⭐️⭐️✨ 4.5/5)

This has a minor stipulation: I purchased these before TP-Link Kasa started making them available to HomeKit. So currently, I'm running a local server of [HomeBridge](http://homebridge.io/) to bridge the gap from TP-Link Kasa to my Apple HomeKit, it works wonderfully, almost flawlessly.
The products themselves have been nothing but reliable, simple, and easy to set-up. I've got 15 light switches and a few dimmers, never had problem with them. Even their app is good.
They probably could make the non-homekit light switches and dimmers HomeKit compatible with a software update, but they opted to release new "HomeKit compatible" products instead.

#### Outlet

TP-Link’s [**Kasa smart plugs**](https://kasasmart.com) (⭐️⭐️⭐️⭐️⭐️ 5/5) - simple, easy, reliable. These smart outlets do what they're designed to do, and don't require unnecessary setup (such as a cloud integration).

#### Temperature Sensors

[**Ecobee SmartSensor**](https://www.ecobee.com/en-ca/accessories/smart-temperature-occupancy-sensor/) - I haven't actually used this device, but this is actually something I'm interested in eventually trying out. I've heard nothing but decent/good reviews.

---

### The Bad

#### Temperature Sensor

[**Eve Weather**](https://www.evehome.com/en-us/eve-weather) (⭐️⭐️ 2/5) - while I'm still perturbed by Eve's indoor camera issues, if you need a sensor just to see what a room's temperature (or perform basic automations with), the Eve Weather works just fine. You'll need to keep in mind that the distance to the Home Hub cannot be too far, as the Eve Weather runs off of [Threads](https://en.wikipedia.org/wiki/Thread_(network_protocol)).
Also, I had a battery die within three months (it might just be a bad battery that was included), I'm now averaging 5%-10% loss in 6 months.
The temperature reading is fairly quick (you can't expect good battery life AND quick readings on the Home app).

(Update: I've seen some previous reviewers say that these end up dying after a year or two, for some reason I didn't believe them... I purchased two of these Eve Weather devices, and guess what happened? After a year, both of them died. I'm not purchasing these again if they're just going to die after a year. Otherwise, they worked okay...)

#### Indoor Cameras

**Logitech Circle View indoor camera** (✨ 0.5/5) - I tried everything to make this camera reliable. I even put it 5ft away from my WiFi router… still would have random times where it’d stop responding to the Home app. It’d work for a full week with no problems, and then randomly stop working for days. Too many people had the same issue with this camera for it to be a coincidence. Simply avoid.

**Eve Indoor camera** (⭐️⭐️ 2/5) - this wasn’t completely terrible of a camera, but still had similar issues as Logitech’s Circle View indoor camera, just not nearly as often. It’d work for weeks and weeks, and randomly stop responding for a few hours and come back online. Better reliability, but still not reliable enough for the premium price!

**ecobee Smart Doorbell Camera (wired)** - I haven't tried this Smart Doorbell, and I'm not gonna.
They're trying the usual, "Hey why don't we just offer our own cloud video hosting service and make money off of that?" thing.
And they're deceptive on their marketing materials too. On the website, it proudly states "Apple HomeKit" is supported! But hey, check out the disclaimer at the bottom: "HomeKit Secure video is not supported."
What does this mean? This means that the _Doorbell_ portion of the **ecobee Smart Doorbell Camera** is supported in Apple HomeKit, NOT the _Camera_ though.
When a person presses the doorbell on your **ecobee Smart Doorbell Camera**, your Apple HomePods will chime... your iPhone will notify you of a person ringing the doorbell...
but when you tap on that doorbell notification on your iPhone, guess what you see? Nothin'. Because they want you to purchase their video cloud subscription thing, and even if you do, the camera feed will not show in your Apple Home app; it'll only show in your ecobee app.
Simply not worth it.

#### Deadbolt Locks

Avoid **Kwikset**. I have one installed on a family member's home, and these locks are terribly loud, the user-experience is goofy, and integrating into a smart-home is clunky.

---

### The Ugly

Obviously, if the packaging or the product description doesn't explicitly say "HomeKit Compatible" then do NOT assume that it does.

Furthermore, DO NOT bank on the *promise* of future HomeKit integration. For example, SimpliSafe promised (back in 2018!!!) that they'd have Apple HomeKit support. I actually bought into this, and thought that it'd be supported. Never trust what a company says that they're *going* to do.

Go for native HomeKit integration over HomeBridge or HomeAssistant to bridge the gap! Having the least amount of dependencies is for the best, but sometimes you just don't want to replace 17 light switches & dimmers! Or sometimes, you want to do something that will never be Apple HomeKit supported, like my 2023 Chevrolet Bolt EUV!

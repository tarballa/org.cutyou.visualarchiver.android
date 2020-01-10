# org.cutyou.visualarchiver.android
TL;DR

It's occurred to me that with the death of a hard drive, my last non-work code sample became extinct.

I decided I'd put something together in its stead, using technologies I've never used before.  While this
may take longer, it brings me back to my favorite part of programming.  I'm not talking about the MVC  pattern,
which I'll be using with Spring Boot for the first time (I've used home-brewed legacy versions of this for a decade)
-- Trial and Error in Learning.

It's really nothing ground-breaking, but once completed, it should be a new trick for this old dog to learn, and a 
in part, the end of a solid decade of using JBoss/Wildfly as my application server.

This won't be a technological revolution.  I won't be reinventing the wheel.  The stack will include an Android app 
that collects telephony metadata (with 2FA and encryption!) and sends it to a http service;  
Incoming/Outgoing Calls, MMS, SMS and Geolocation pings.  Using this meta data, I'll offer a web view of previously
telephony-only statistics.  From Google Maps mashups to a living timeline, text messages can be shared to a public feed
or to social media.

Technologies I plan to use (Day 1 -- this should be an interesting diary note for agile folks).  I think I'll scope these out 
with the Fibanachi sequence, on a two week sprint with a 13-20 considered a full load.

Android APK: Minimal design.  Login/Password, Sign up. Once authenticated, Checkboxes for Call Events, SMS Event, MMS Event, 
and GPS ping at 5 minutes, 15 minutes, 30 minutes, 1 hour or 4 hours.  These figures were pulled right out of my ass. I have to 
imagine that GPS is a near constant heartbeat with the subscriber. 

Use Gson or Retrofit for REST calls, explore SQL lite text fields to take a look at autofill.  This may also work with REST, so 
it may be moot.

By the way, I'm using Android Studio on this.  Not only is it NOT ECLIPSE, but I'm using a Mac so my shortcutys are crazy honked off.
Yeah yeah, I'm sure you all are bad-asses who use Notepad.

Scope: 20.  It's not hard, but I'm out of practice oaan Android. That's including some leeway for playing with Gson/Retrofit, which is 
essentially tech debt, but I mean that in a positive way.

App Server: Tomcat with Spring Boot, Jersey, and JPA. A lot of people recommend Jersey instead of Spring's included REST API, so I'll examine
both.  Set up a Gradle build script in Eclipse (since Android Studio is totally in love with it).  It should be minimal with most of the initial
focus on the M and C of the MVC. I expecty the front-end taao be in React or Angular, so the work here is mostly in writing REST endpoints and test cases!!
Scope: 13, since the only technology I've used thus far is Jersey.  Regardless of the technology, I'll employ something like Swagger for documentation, but
that isn't included in this scope estimate.

Database :I've not used a NoSQL DB yet, so this might be the time.  MongoDB is highly recommended.  Should MMS media be stored in a blob?  Sir, this
is a Wendy's.  Why are you trying to store media in the damn DBa? I mean, it won't hurt my pride to at least Google that.

So Mongo or mySQL, schema design.
Scope: 7.

Add the DAO layer to the server app.  I'm sick of reading of data breaches, so I'm going to look into the cost of hardening my data.  Cost = effort, not money,
mom.
Scope 5.

Complete the REST transaction by phone alone.  All endpoints should exist now, the logic just neeeded to be wired in.  Add any missing tests.

Scope: 3.

Create a decent front end to display payloads.  It works in the mental image I have of it, but basically imagine a caroseul photo viewer that displays MMS content
in a text message recreator with mobile headers.  Display images and links with mini headless browsers (like http://m.fark.com) or Facebook link previews.
This one will take the longest because I've never been known as a front-end designer, but 

01/10/2020 @ 09:24 AM

I realized I left that full of typos and litterally in the middle of a sentence about something or another.  I'll try to do updates regularly.  I'm using GitHub's Jira knock off for sprint planning.  I'm only going through the trouble of having an actual sprint just so future readers will be able to get a handle on the type of person I am.  All is good for now, I'M NOT TYPING IN CAPS OR ANYTHING!!!111

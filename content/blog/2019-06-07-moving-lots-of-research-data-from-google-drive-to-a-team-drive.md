---
title: Moving lots of research data from Google Drive to a Team Drive
date: 2019-06-07T22:22:40.536Z
published: false
---
One of the places where I spend a great deal of my time is with the [USU Get Away Special](https://getawayspecial.usu.edu) team, and we recently ran into a problem: 

We currently use a shared Google Drive folder to house all our digital files. It's got papers, experiments, and team history that goes back all the way to the creation of our [team in 1976 (!)](https://en.wikipedia.org/wiki/Getaway_Special). After uploading some simulation data, one of our team members realized that the 60GB worth of data counted against his personal Google storage quota (luckily, he wasn't limited to just 15GB). That just wouldn't do!

In the past, our files had lived on just about every data medium you can think of. We've still got bookshelves full of binders and papers documenting purchases, manuals, and other details for the team's past payloads. We opted for Google Drive because it took the responsibility of keeping our data hosted somewhere we could all get to it away from us, and made using our own computers much easier. No longer did we need to rely on a small handful of old Dell Optiplexes hosting our data and passing around the external drive. 

We wanted to continue using Google Drive, and we had two options: 

1. Delete the data, and re-upload it from our school-provided google accounts, which have unlimited quotas for personal storage.
2. Move our data to a Team Drive. Google doesn't support moving entire folders unless you're a Super Admin, meaning we would have to move each file seperately.

Looking at our two options, we didn't have much hope. What were we going to do?

My first idea was to download a zip archive of the team resources, and then unzip it and upload it to the team drive. We started this process, but the zip creation took longer than 4 hours, and so we were back to square one, not sure what to do. Eventually, I remembered about `rclone`, a handy little tool that acts a lot like `rsync` except it's primarily for interacting with cloud data.

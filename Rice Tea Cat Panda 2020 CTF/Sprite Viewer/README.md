# Sprite Viewer

Category : Web

Points : 400

## Description

The developer of that work in progress game thinks there may have been a bug on his end, and has asked us to get the md5 hash of the goblin sprite image.

Here's the place where he got the images... but... they're stuck in a web player!!! How will you get the hash out of that?!

## Hint

[Challenge input](https://riceteacatpanda.wtf/spview)

Insert flag in MD5 format, without the rtcp{}:

e7ad2f601c93ea0dab82416581db2dfd

## Solving

Good question, how will we get the hash out of that ? Well first, let's look at the sprite viewer page and look in the network tab of
the developper tools and look for the file we're interested in that contains the assets, Builds.data.unityweb :

![image](https://user-images.githubusercontent.com/57148042/73198069-ba6b8400-4132-11ea-8d92-48249d687216.png)

We can then get the file, and look for a tool to open it. The tool we'll use here is AssetStudio :

![image](https://user-images.githubusercontent.com/57148042/73198240-00c0e300-4133-11ea-8f3b-be547586026b.png)

We then look for the goblin spritesheet in the "Asset list" tab :

![image](https://user-images.githubusercontent.com/57148042/73198330-20580b80-4133-11ea-9918-c21cc7f36c60.png)

Then right click on it to export it. Now we just need to get the md5 hash for it. Let's use some online tool to get our flag :

![image](https://user-images.githubusercontent.com/57148042/73198639-9e1c1700-4133-11ea-884f-a93b5da30936.png)

flag : rtcp{4698B70704C2C4DBD427DAFC1BBF5C89}

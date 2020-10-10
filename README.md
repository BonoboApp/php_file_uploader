# PHP FILE UPLOADER WITH PROGRESS BAR

![](https://camo.githubusercontent.com/6bbbfabbd62d20514245a59e4dadf52adf869014/68747470733a2f2f626f6e6f626f6170702e696f2f696d672f626f6e6f626f5f6c6f676f322e706e67)


![](https://drops.ricardoalcocer.com/drops/uploader_screenshot-cR1X1v8OvC.png)
Yeah, so this is the simplest reusable PHP File Uploader I could come up with.

# Background
This is the core of the uploader used by BONOBO.  The BONOBO implementation has a couple additional proprietary details that we've decided to strip out of this repo to make it as generic as possible.

# Why release this?
Although uploading files is well documented, sometimes is not trivial to setup.  

With this reusable implementation, simply drop the entire repo onto a folder.  Then browse to that folder, and the uploader launches - as simple as that.

# Installation
Drop it on a PHP-enabled folder and open index.php.  It should work right out of the box.

# How it works
- Index.php starts off the script and shows the upload form.  
- This docuemnt submits to itself, and next time around it checks if there are files 
- Although it's currently locked to uploading a single file, the script expects an array of files, so you could upload multiple by simply adding the `multiple` flag to the Input File tag.  I just don't have a need for it currently.  If you need muitple files, edit the tag like this:

`<input type="file" class="custom-file-input" id="file" multiple>`

# Can it upload large files? 

I've been able to succesfuly upload files up to around 250mb.  However, there seems to be an Apache restriction regarding how long a script can run, so it times out after running for around 10 minutes.

If anyone knows how to solve this, PULL REQUESTS are accepted and encouraged!

### Upload Folder

- It's specified on the header of `index.php`: 
   - `$uploadFolder = "files/";`

# Contributing
Yes, PLEASE.  If you use it and have something to contribute, please send a PULL REQUEST.

# Contributors

Ricardo Alcocer - https://alco.rocks

# License

MIT - alco.mit-license.org
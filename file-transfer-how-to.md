# Transferring Files to the Class Server

This term you will be submitting your work to be graded by uploading it to a server on the Internet. You can do this using any number of file transfer clients that support the SSH File Transfer Protocol. The one that I recommend and that is installed on the school’s computers is FileZilla. It’s free software and is available for Windows, Mac, and Linux from [filezilla-project.org](https://filezilla-project.org/index.php).

[![Imgur](http://i.imgur.com/oJ4Jdn0m.png)](http://i.imgur.com/oJ4Jdn0.png)

This tutorial below will walk you through uploading files to your site and doing basic file management.

## Downloading and Installing FileZilla

FileZilla is already installed on the computers here on campus. If you are using one of the college's computers you may skip ahead to **Logging Into the Class Server" below. If you want to download and install it on your personal computer follow the steps below.

1. Open a browser and navigate to [filezilla-project.org](https://filezilla-project.org/index.php).
1. Click the large button that reads "Download FileZilla Client."
1. You will be redirected to a page where you can download the software. The website will detect the operating system of the computer you are on and suggest the appropriate version of the program. If you want to download FileZilla for a different platform use the links on the page.
1. Download the version of the software you need and install it as you normally would. **Note:** As the page mentions there may be additional software bundled with FileZilla. Pay attention as you click through the install wizard to be sure you don't install any additional software you do not want.

## Logging Into the Class Server

You were given a slip of paper with, among other things, your username and password for the server. Log in by following the steps below.

Open FileZilla. Notice that the FileZilla window consists of six panes each with their own purpose.

[![Imgur](http://i.imgur.com/t0q88Wfm.png)](http://i.imgur.com/t0q88Wf.png)


1. **Message Log:** Displays information about the current status of your connect to the server.
1. **Local Directory Tree:** Displays the drives and folders that are found on the local computer (the one you are running FileZilla on at the moment).
1. **Local File Listing:** Displays the contents of the folder that is currently selected in the Local Directory Tree.
1. **Remote Directory Tree:** Displays the drives and folders that are found on the remote computer (the server you are currently logged on to).
1. **Remote File Listing:** Displays the contents of the folder that is currently selected in the Remote Directory Tree.
1. **Transfer Queue:** Displays the status of current and past file uploads and downloads including the number of transfers pending, the number that have successfully completed, and any failed transfers as well.

We will need to create an entry for the class server so FileZilla can know how to connect to it. Click the File menu, and select Site Manager...

[![Imgur](http://i.imgur.com/82bHGRbm.png)](http://i.imgur.com/82bHGRb.png)

On the Site Manager dialog click the New Site button and give the entry a name. In the picture below I've called the site "Web Dev Server."

[![Imgur](http://i.imgur.com/y9EF8dzm.png)](http://i.imgur.com/y9EF8dz.png)

We will need to fill in the Host, Protocol, Logon Type, User, and Password fields as follows:

* Host: lbccwebdev.net
* Protocol: SFTP - SSH File Transfer Protocol
* Logon Type: Normal
* User: *your user name*
* Password: *your password*

[![Imgur](http://i.imgur.com/PoWlvNXm.png)](http://i.imgur.com/PoWlvNX.png)

Once you've filled in the required fields click the Connect button. The first time you connect to the server you will see the dialog below. Check the "Always trust this host, add this key to the cache" checkbox, then click the OK button.

[![Imgur](http://i.imgur.com/LBvGEcom.png)](http://i.imgur.com/LBvGEco.png)

You should now be connected to the remote server. FileZilla should be displaying the contents of the `public_html` folder in the Remote Directory Tree window (4) and you should see a file named index.html in the Remote File Listing window (5).

## Downloading, Modifying, and Uploading Files

FileZilla makes transferring files simple. To practice this, follow these steps.

First, let's copy the file `index.html` from the remote server to the local computer so we can edit it. As you can see in the image below I'm connected to the class server and am showing the contents of my Desktop folder in the Local File Listing window (3). To copy the `index.html` file down I can either double-click on it in the Remote File Listing window or drag it from that window and drop it in the Local File Listing window. In either case the file will be copied to the local machine where I can edit it.

[![Imgur](http://i.imgur.com/tfmwvmIm.png)](http://i.imgur.com/tfmwvmI.png)

Once you've downloaded your `index.html` file make some changes to it. After you've saved your changes, upload the edited file by either double-clicking it from the Local Files Window or dragging it into the Remote File Listing window. Your files will always be copied to whatever folder is currently selected on the destination computer.

When you transfer a file that already exists on the destination computer you will be presented with a dialog like the following. This is FileZilla telling you that a file with the same name was found in the destination and asking you how you would like to proceed. Select the option that makes the most sense and click OK. I find "Overwrite if source is newer" to be safest.

[![Imgur](http://i.imgur.com/6Z2emwDm.png)](http://i.imgur.com/6Z2emwD.png)

Now that you've uploaded your edited home page, open a browser and navigate to **http:lbccwebdev.net/*username*** to see your file on the Web!

[![Imgur](http://i.imgur.com/YC125IOm.png)](http://i.imgur.com/YC125IO.png)

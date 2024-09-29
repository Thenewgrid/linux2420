# Assignment 1
## Digital ocean server set up
login into digital ocean in your web browser and navigate to your first-project.
> First-project is just what I called my project. Your project can be called whatever you want.
> 
> Just make sure that you are clicking the same place as me.

![image 1](picture1.png)

This project section will be where we store our droplet.

>### Arch linux image
>If you already have a recent image, please continue past this step.
>
>If you do not already have an arch linux image, [click here](https://gitlab.archlinux.org/archlinux/arch-boxes/-/packages/).
>
>click on the most recent folder. In my case it is this one.
>
>![image 2](picture2.png)
>
>Once inside the folder, scroll down until you find an Arch-Linux file, with file extension ".qcow2". This is the arch linux image you want.
>
>The image will be close to 500 MiB in size.
>
>![image 3](picture3.png)

### SSH keygen

Leave digital ocean the way it is and minimize your web browser. Open your terminal.

I am on a windows OS, so I will be using powershell.

>If you can't locate your terminal open your file or system search tool and type "terminal".

Change "digo-key" to what you want to name your ssh key. 

Change "your email" to your email address or your name.

- -t specifies the type of encryption algorithm we want to use.
- -f specifies the file name. 
- -C is a comment that will be attached to the ssh key.

>**Don't change the encryption or make it blank.** 
>
>unspecified encryption will just turn into RSA encryption.
>
>We want to use ed25519 over the default RSA encryption.

Copy the following command into your terminal:

```
ssh-keygen -t ed25519 -f ~/.ssh/digo-key -C "your email or name"
```

![image 4](picture4.png)

>Once you get to this screen I recommend just pressing enter for no pass phrase.
>
>This is because you will need to enter it every time you login using ssh.
>
>If you do choose to use a passphrase I recommend writing it down.

![image 5](picture5.png)
>
>SSH key generation may not always work when using powershell. This is beacuse windows may not view the tilde (~) as the user's home directory.
>
>If your key generation failed and you are in powershell.
>
>Copy the following command and try again, remember to change "user name" to your user name.

```
ssh-keygen -t ed25519 -f C:\Users\user name\.ssh\digo-key -C "your email or name"
```

>If you get "failed" it might mean that the .ssh directory or folder does not exist.
>
>Open the file explorer. This is called finder on Mac. For linux it may depend on your distribution.
>
>For windows;
>
>![image 6](picture6.png)
>
>Copy and paste the following line into the area left from search. Make sure you change "user name" to your user name.
>
>make a folder called ".ssh" inside your username folder.
>
>Try to generate your ssh keys again.

```
C:\Users\user name
```

>For MacOS, open finder and do `shift` + `command` + `G`.
>
>Copy and paste the following line into the search pop up.
>
>change "user name" to your user name.
>
>make a folder in your username folder and call it ".ssh".
>
>Try to generate your ssh keys again.
```
~/user name
```

After you enter your pass phrase, (empty for no passphrase) your public and private ssh keys should be generated.

### Public and Private keys

Close your terminal and open the file explorer.

For windows copy and paste the following into the area left from search. Make sure to change "user name".

```
C:\Users\user name\.ssh
```

For Mac open finder and do `shift` + `command` + `G` again.

Then copy and paste the following.

```
~/user name/.ssh
```

When you access your .ssh folder, you should be able to see digo-key and digo-key.pub.

![image 7](picture7.png)

The key we want to get right now is digo-key.pub. Right click on the "digo-key.pub" file and click open with visual studio code.

once you are inside visual studio code. Copy the text in the file and close visual studio code.

### Security with SSH

Open your web browser again. You should be inside your project section in Digital Ocean. 

## Resources
**in MLA or APA format**

---
created: 2024-05-17T02:22:41 (UTC -05:00)
source: chrome-extension://pcmpcfapbekmbjjkdalcgopdkipoggdi/
author: Luke Reynolds
banner: https://linuxconfig.org/wp-content/uploads/2013/03/02-ssh-login-without-password.png
banner_y: 0.02333
---
If you ever get tired of typing in your [SSH](chrome-extension://pcmpcfapbekmbjjkdalcgopdkipoggdi/how-to-make-the-most-of-openssh) password, we’ve got good news. It’s possible to configure public key authentication on [Linux systems](chrome-extension://pcmpcfapbekmbjjkdalcgopdkipoggdi/linux-download), which allows you to connect to a server through SSH, without using a password.

The best part is, using key authentication is actually more secure than typing in a password each time. This is in addition to being far more convenient. It also allows you to automate certain tasks, such as [rsync](chrome-extension://pcmpcfapbekmbjjkdalcgopdkipoggdi/rsync-command-examples) scripts or other [Bash scripts](chrome-extension://pcmpcfapbekmbjjkdalcgopdkipoggdi/bash-scripting-tutorial-for-beginners) that utilize SSH, SCP, etc.

The process for setting up key authentication involves generating RSA keys on one system, then copying the key to a remote host. This works on any [Linux distribution](chrome-extension://pcmpcfapbekmbjjkdalcgopdkipoggdi/how-to-choose-the-best-linux-distro) and is a short and easy process. Follow along with the instructions below as we take you through the step by step guide to configure passwordless SSH on Linux.

**In this tutorial you will learn:**

-   Generate RSA keys and transfer to remote system
-   How to login with SSH without a password

![[../03 - MEDIA & FILES/02-ssh-login-without-password 1.avif]]

Configuring SSH login without password between two systems

Software Requirements and Linux Command Line Conventions
| Category | Requirements, Conventions or Software Version Used |
| --- | --- |
| System | Any [Linux distro](chrome-extension://pcmpcfapbekmbjjkdalcgopdkipoggdi/linux-download) |
| Software | OpenSSH |
| Other | Privileged access to your Linux system as root or via the `sudo` command. |
| Conventions | **#** – requires given [linux commands](chrome-extension://pcmpcfapbekmbjjkdalcgopdkipoggdi/linux-commands) to be executed with root privileges either directly as a root user or by use of `sudo` command  
**$** – requires given [linux commands](chrome-extension://pcmpcfapbekmbjjkdalcgopdkipoggdi/linux-commands) to be executed as a regular non-privileged user |

## Configure SSH login without password

---

---

1.  Start by opening a terminal and generating RSA keys on the system that you will be connecting from. Run the following command, then press `Enter` three times.
    
    ```
    $ ssh-keygen
    ```
    

![[../03 - MEDIA & FILES/01-ssh-login-without-password.avif]]

Generating RSA keys for SSH

3.  Next, we copy our key to the remote system by using the `ssh-copy-id` command. We’ll also specify our SSH user and the remote system’s hostname or IP address. Then, you’ll be prompted for the SSH login password.
    
    ```
    $ ssh-copy-id user@hostname
    ```
    

![[../03 - MEDIA & FILES/02-ssh-login-without-password.avif]]

Copying the RSA keys to the remote system

5.  Now that the key has been copied to the remote system, you will be able to connect like usual, but without needing to give the password anymore.
    
    ```
    $ ssh user@hostname
    ```
    

That’s all there is to it. You won’t need to specify a password again. However, if the RSA keys are deleted or replaced, you will have to delete the old pair and generate them again by following this same set of instructions.

---

---

## Closing Thoughts

In this guide, we saw how to configure SSH login without a password on Linux. Not only does this save us some keystrokes every time we have to login, but it also provides additional security and allows us to automate tasks with Bash scripts that utilize SSH login.

---

---

**Comments and Discussions**  

> 
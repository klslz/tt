# tt
Touch Toolbox (no longer maintained)

The Touch Toolbox is a tuning/optimization tool for the 
Linux based Logitech Squeezebox Touch (SBT) audio streamer.
The SBT is afaik more then ten years (2012?) out of production.
Around that time frame I also stopped maintaining the Toolbox. 

I still (2023) receive mails asking for the Touch Toolbox though.

I finally decided to put it on github. I can neither support 
anybody nor I am willing to maintain the Toolbox.
You'll be 100% on your own. 

I'll add the setup documentation that I had realeased on my 
blog in the past. And you'll get the Touch Toolbox Version 3.0.
Version 3.0 was the last version I released back than. 

You might have noticed I put it under GPL3 license. Read that
to know what your're dealing with.

Enjoy.

_________________________________________________________________

Note (2023-02-09):

There might be problems to ssh into the Squeezebox Touch due to
meanwhile rather outdated ssh keys and algorithms on the SBTouch. 
After looking into it I found a solution. If you encounter problems
you might want to try below command after you've enabled ssh access
on the Squeezebox Touch inside the "Settings/Advanced/Remote Login"
menu. Don't forget to insert your own SBT IP Address.

```
ssh -o KexAlgorithms=+diffie-hellman-group1-sha1 \
    -o HostKeyAlgorithms=+ssh-rsa \
    -o PubkeyAcceptedAlgorithms=+ssh-rsa \
    -c aes128-cbc \
    -o PubkeyAuthentication=no \
    -o PreferredAuthentications=keyboard-interactive,password \
    -o RSAMinSize=1024 \
    root@192.xxx.x.xxx
```


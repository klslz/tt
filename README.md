# tt
Touch Toolbox (no longer maintained)

This is the repo for the Touch Toolbox.

The Touch Toolbox is a tuning/optimization tool for the 
Linux based Logitech Squeezebox Touch audio streamer.
It's about ten years that the device is out of production.

I still (2023) receive mails asking for the TouchToolbox.

I now decided to put it on github. I can neither support 
anybody nor I am able to maintain the toolbox. I simply do 
not have a working Squeezebox Touch at hand anymore.
You'll be 100% on your own, if you use/apply it. 

I'll add the setup documentation I had on my blog in the past.
And you'll find the TouchToolbox 3.0. 3.0 was the last version 
I released back than. 

You might have noticed I put it under GPL3 license.

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


---
title: "Lessons Learned"
date: 2026-02-18
draft: false
---

Working on these security simulations taught me that theory is very different from practice. I decided to build these labs because I wanted to see how vulnerabilities actually look when you are the one finding and fixing them.

One of the biggest takeaways for me was seeing how dangerous legacy software can be. I found that old services like vsftpd often have known backdoors that give an attacker full control almost instantly. It made me realize that keeping systems updated is not just a chore but a critical part of defense.

I also spent a lot of time learning about how attackers move through a network. I used metasploit to set up a reverse shell which taught me that firewalls do not always stop an attack if the compromised server is the one initiating the connection. This showed me why it is so important to monitor outgoing traffic just as much as incoming traffic.

If you are starting your own projects like this my best advice is to embrace the parts that break. I learned more from fixing broken docker configurations and toml errors than I did from the parts that worked perfectly the first time. Understanding why something failed gives you a much deeper understanding of the technology.
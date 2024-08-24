---
title: Guides
layout: default
nav_order: 3

has_toc: false
has_children: true
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

# Guides

This guide is intented to be started on a fresh installation of ubuntu on your server. You can also follow this simply by creating a new user, or even using your current user. However, running this root will typicall lead to issues with permissions and for that reason we recommend using a new user.

**For Part one, you will run all the commands as root, and for part two, you will run as the new user.**

## Part One (Root)

Download Docker and Docker Compose v2
```
sudo curl -s https://raw.githubusercontent.com/InstaHost/InstaHost/main/Docker/Docker_and_Docker-Compose.sh | bash
```
(For manual installation see:LINK TO MANUAL INSTALLATION GUIDE)

---

**Create a new user to run docker**

Create the user
```
sudo adduser 'USERNAME'
```

Find the users GIUD and GPID
```
sudo id 'USERNAME'
```

Give sudo permissions to new user
```
usermod -a -G sudo 'USERNAME'
```

Login to your newly created user
```
su 'USERNAME`
```

Go into the directory of the newly created user
```
cd
```

---

## Part Two (User)

Clone the github repoistory
```
git clone https://github.com/InstaHost/InstaHost
```

Open the directory of the clones repository
```
cd InstaHost
```

Run the python CLI
```
python3 InstaHost.py
```
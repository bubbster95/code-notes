# Copy Pasta

Table of Contents:
1. [Various Import Scripts](#import-packages) 
2. [Helpful Links](#helpful-links)
3. [Miscallanious Notes](#misc-notes)

Other Files:
1. #### [Python Flask](./BackEnd/python_flask)
2. #### [Node Express](./BackEnd/node_express)
3. #### [SQL](./BackEnd/sql)

# Import Packages

### Jquery

    <script src="http://unpkg.com/jquery"></script>

### Axios

    <script src="https://cdnjs.cloudflare.com/ajax/libs/axios/0.19.2/axios.min.js"></script>

---

# Helpful links

### [Local Host](http://127.0.0.1:5500/)

### [Json parser](https://jsonformatter.org/json-parser)

### [List of Public apis](https://github.com/public-apis/public-apis#open-source-projects)

### [Repo About Readmes](https://github.com/matiassingers/awesome-readme)

### [Markdownn syntax](https://www.markdownguide.org/cheat-sheet/)

---

# Misc Notes

### Access Downloads through ubuntu
    /mnt/c/Users/stile/Downloads

### Eric's Github handle
    sdxl

#### If WSL ever pulls this BS:
> "VS Code Server for WSL closed unexpectedly."

#### Go into Powershell and restart WSL:
    wsl --shutdown
    wsl

---

### Change PG Authentication

#### Edit file 
    sudo nano /etc/postgresql/12/main/pg_hba.conf

#### Files original configuration

    local   all             postgres                                peer

    # TYPE  DATABASE        USER            ADDRESS                 METHOD

    # "local" is for Unix domain socket connections only
    local   all             all                                     peer
    # IPv4 local connections:
    host    all             all             127.0.0.1/32            md5
    # IPv6 local connections:
    host    all             all             ::1/128                 md5
    # Allow replication connections from localhost, by a user with the
    # replication privilege.
    local   replication     all                                     peer
    host    replication     all             127.0.0.1/32            peer
    host    replication     all             ::1/128                 md5
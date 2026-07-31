# [![github](favicon.ico)](https://github.com/donmor) donmor-repos

This organization is for unofficial repositories set up by me.


## Quick configuration
Install [`donmor-repos-keyring`](pub/donmor-repos-keyring_0.0.1_all.deb), and choose one or more repo config packages:
- TiddlyWiki ([`node-tiddlywiki-debian`](pub/node-tiddlywiki-debian-repo_0.0.1_all.deb))
  - `node-tiddlywiki`
 
Be sure to run `apt-get update` before installing any package.
 
## Manual configuration
#### Add keyring:
``` bash
curl -sLOJR --output-dir /usr/share/keyrings https://donmor-repos.github.io/pub/donmor-repos-keyring.gpg
```
#### Add `<repo>`:
``` bash
tee /etc/apt/sources.list.d/<repo>.sources <<EOF
Types: deb deb-src
URIs: https://github.com/donmor-repos/<repo>/releases/latest/download
Suites: /
Signed-By: /usr/share/keyrings/donmor-repos-keyring.gpg
EOF
apt-get update
```
`<repo>`s:
- `node-tiddlywiki-debian`

# RailsDevOps
Automatically Deploy &amp; Configure A Production Server For Ruby On Rails Applications

## Overview
This tutorial uses Vagrant & Ansible to build a production Nginx/Passenge/PostGres webserver on Ubuntu 20.04 (Foca Fossa) Virtual Box Machine. The configurations
for this repository was adapted from [Deploying Ruby On Rails](https://gorails.com/deploy/ubuntu/20.04#vps) from [GoRails](https://gorails.com)

Feel free to modify the code in this tutorial to launch your own applications. Have fun !

## Packages
  Rbenv was installed as a Ruby version manager, we then install Ruby 3.1.1

  because Ubuntu apt repo for rbenv is out of date we cloned
[rbenv from git](https://github.com/rbenv/rbenv#basic-git-checkout)

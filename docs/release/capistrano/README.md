>how to setup capistrano with magento2

[install ruby](https://www.ruby-lang.org/en/documentation/installation/#apt)

>install Ruby using Rbenv

- sudo yum install git-core zlib zlib-devel gcc-c++ patch readline readline-devel libyaml-devel libffi-devel openssl-devel make bzip2 autoconf automake libtool bison curl sqlite-devel

- curl -sL curl -fsSL https://github.com/rbenv/rbenv-installer/raw/HEAD/bin/rbenv-installer | bash

- echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
- echo 'eval "$(rbenv init -)"' >> ~/.bashrc
- source ~/.bashrc
- rbenv install -l 
- rbenv install 3.0.3 
- rbenv global 3.0.3
- ruby -v
- gem install bundler
- gem install capistrano
- gem install capistrano-magento2


- cd <project_root>
- mkdir -p tools/cap
- cd ./tools/cap
- cap install

> this will triggered following commands

- mkdir -p config/deploy
- create config/deploy.rb
- create config/deploy/staging.rb
- create config/deploy/production.rb
- mkdir -p lib/capistrano/tasks
- create Capfile
- Capified

















[Reference](https://www.siphor.com/using-capistrano-for-magento-to-deploy/)



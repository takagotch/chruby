### chruby
---

https://github.com/postmodern/chruby

```
wget -O chruby-0.3.9.tar.gz https://github.com/postmodern/chruby/archive/v0.3.9.tar.gz
tar -xzvf chruby-0.3.9.tar.gz
cd chruby-0.3.9/
sudo make install

wget https://raw.github.com/postmodern/chruby/master/pkg/chruby-0.3.9.tar.gz.asc
gpg --verify chruby-0.3.9.tar.gz.asc chruby-0.3.9.tar.gz

sudo ./scripts/setup.sh

brew install chruby
brew install chruby --HEAD
yaourt -S chruby

cd /usr/ports/devel/chruby/ && make install clean

ruby-install ruby
ruby-install jruby
ruby-install rubinius
ruby-install maglev

ruby-build 1.9.3-p392 /opt/rubies/ruby-1.9.3-p392
ruby-build jruby-1.7.3 /opt/rubies/jruby-1.7.3
ruby-build rbx-2.0.0-rc1 /opt/rubies/rubinius-2.0.0-rc1
ruby-build maglev-1.0.0 /opt/rubies/maglev-1.0.0

source /usr/local/share/chruby/chruby.sh

if [ -n "$BASH_VERSION" ] || [ -n "$ZSH_VERSION" ]; then
  source /usr/local/share/chruby/chruby.sh
fi

source /usr/local/share/chruby/chruby.sh
RUBIES+=(
  /opt/jruby-1.7.0
  "$HOME/src/rubinius"
)

RUBIES+=(~/.rvm/rubies/*)
RUBIES+=(~/.rbenv/versions/*)
RUBIES+=(~/.rbfu/rubies/*)

source /usr/local/share/chruby/chruby.sh
source /usr/local/share/chruby/auto.sh

chruby ruby-1.9
echo "ruby-1.9" > ~/.ruby-version

chruby
chruby 1.9.3
chruby
echo $PATH
gem env
chruby jruby --1.9
ruby -v
chruby system
echo $PATH
chruby-exec jruby -- gem update
chruby_use /path/to/ruby

exec $SHELL
sudo make uninstall

```


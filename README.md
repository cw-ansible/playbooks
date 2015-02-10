

	cd ~
	mkdir Developer
	cd Developer
	mkdir ansible
	cd ansible
	git clone https://github.com/ansible/ansible.git


	mkdir -p /srv/sw/
	cd /srv/sw/
	git clone https://github.com/Homebrew/homebrew.git
	sudo mkdir /usr/local
	sudo chown $USER /usr/local
	ln -nfs /srv/sw/homebre/Cellar /usr/local
	brew install caskroom/cask/brew-cask
	brew install python
	export PYTHONPATH="$(brew --prefix)/lib/python2.7/site-packages:$PYTHONPATH"
	export HOMEBREW_CASK_OPTS='--caskroom=/srv/sw/cask'



export PYENV_ROOT=/srv/sw/pyenv/
eval "$(pyenv init -)"
pyenv install 2.7.8
pyenv local 2.7.8

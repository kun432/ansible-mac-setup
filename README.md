#  ansible_mac_setup

setting up my Mac(Macbook Pro 2016) using ansible.

## Usage

1. Install Homebrew and ansible.

```shell
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
$ brew install ansible
```

2. Clone this repository.

```shell
$ git clone https://github.com/kun432/ansible_mac_setup/
$ cd ansible_mac_setup
```

3. Run playbook.

```shell
$ ansible-playbook -i hosts playbook.yml
```

## ToDo

- change touchpad settings (enable drag)
- change iCloud settings (disable Mail)
- change Dock settings (enlarge dock icon)
- change various Safari settings
- disable spell check settings
- change hostname
- clone dotfiles

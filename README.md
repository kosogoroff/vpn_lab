# Лабораторный стенд ДЗ по занятию "35 - Мосты, туннели и VPN"

Для развёртывания выполните команды:

```
git clone https://github.com/kosogoroff/vpn_lab.git
cd vpn_lab
vagrant up
```

Для создания репоозитория использовались команды:

```
[admin_insta11@mv334 vpn_lab]$ git init
подсказка: Using 'master' as the name for the initial branch. This default branch name
подсказка: is subject to change. To configure the initial branch name to use in all
подсказка: of your new repositories, which will suppress this warning, call:
подсказка: 
подсказка: 	git config --global init.defaultBranch <name>
подсказка: 
подсказка: Names commonly chosen instead of 'master' are 'main', 'trunk' and
подсказка: 'development'. The just-created branch can be renamed via this command:
подсказка: 
подсказка: 	git branch -m <name>
Инициализирован пустой репозиторий Git в /home/admin_insta11/vpn_lab/.git/
[admin_insta11@mv334 vpn_lab]$ 
[admin_insta11@mv334 vpn_lab]$ git add .
[admin_insta11@mv334 vpn_lab]$ 
[admin_insta11@mv334 vpn_lab]$ git commit -m "first commit"
[master (корневой коммит) c560ac5] first commit
 8 files changed, 307 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 README.md
 create mode 100644 Vagrantfile
 create mode 100644 ansible/hosts
 create mode 100644 ansible/playbook.yml
 create mode 100644 client.conf
 create mode 100755 generate_inventory.sh
 create mode 100644 inventory.ini
[admin_insta11@mv334 vpn_lab]$ 
[admin_insta11@mv334 vpn_lab]$ git branch -M main
[admin_insta11@mv334 vpn_lab]$ 
[admin_insta11@mv334 vpn_lab]$ git remote add origin https://github.com/kosogoroff/vpn_lab.git
[admin_insta11@mv334 vpn_lab]$ 
[admin_insta11@mv334 vpn_lab]$ git push -u origin main

(gnome-ssh-askpass:329569): dbind-WARNING **: 17:18:52.052: Couldn't connect to accessibility bus: Empty address ''

(gnome-ssh-askpass:329586): dbind-WARNING **: 17:19:03.192: Couldn't connect to accessibility bus: Empty address ''
Перечисление объектов: 10, готово.
Подсчет объектов: 100% (10/10), готово.
При сжатии изменений используется до 24 потоков
Сжатие объектов: 100% (8/8), готово.
Запись объектов: 100% (10/10), 4.29 КиБ | 1.43 МиБ/с, готово.
Total 10 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/kosogoroff/vpn_lab.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
[admin_insta11@mv334 vpn_lab]$ 
```

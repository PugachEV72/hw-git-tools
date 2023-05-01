# Домашнее задание к занятию «Инструменты Git» - Пугач Евгений.

---

### Ответ:


1. Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.

`git show --pretty=format:"%H %s" aefea`

`aefead2207ef7e2aa5dc81a34aedf0cad4c32545 Update CHANGELOG.md`

Полный хэш: aefead2207ef7e2aa5dc81a34aedf0cad4c32545  
Комментарий: Update CHANGELOG.md

---
2. Какому тегу соответствует коммит 85024d3?

`git show 85024d3`

`commit 85024d3100126de36331c6982bfaac02cdab9e76 (tag: v0.12.23)`

Тег: v0.12.23

---
3. Сколько родителей у коммита b8d720? Напишите их хеши.

`git show --pretty=format:"Hash: %H%nParents: %P" b8d720`

```
Hash: b8d720f8340221f2146e4e4870bf2ee0bc48f2d5    
Parents: 56cd7859e05c36c06b56d013b55a252d0bb7e158 9ea88f22fc6269854151c571162c5bcf958bee2b
```

У коммита b8d720 2 родителя, их хеши:  
56cd7859e05c36c06b56d013b55a252d0bb7e158, 9ea88f22fc6269854151c571162c5bcf958bee2b

---
4. Перечислите хеши и комментарии всех коммитов которые были сделаны между тегами v0.12.23 и v0.12.24.

`git log --pretty=oneline v0.12.23..v0.12.24`

```
33ff1c03bb960b332be3af2e333462dde88b279e (tag: v0.12.24) v0.12.24
b14b74c4939dcab573326f4e3ee2a62e23e12f89 [Website] vmc provider links
3f235065b9347a758efadc92295b540ee0a5e26e Update CHANGELOG.md
6ae64e247b332925b872447e9ce869657281c2bf registry: Fix panic when server is unreachable
5c619ca1baf2e21a155fcdb4c264cc9e24a2a353 website: Remove links to the getting started guide's old location
06275647e2b53d97d4f0a19a0fec11f6d69820b5 Update CHANGELOG.md
d5f9411f5108260320064349b757f55c09bc4b80 command: Fix bug when using terraform login on Windows
4b6d06cc5dcb78af637bbb19c198faff37a066ed Update CHANGELOG.md
dd01a35078f040ca984cdd349f18d0b67e486c35 Update CHANGELOG.md
225466bc3e5f35baa5d07197bbc079345b77525e Cleanup after v0.12.23 release
```
 
Между тегами v0.12.23 и v0.12.24 было сделано 10 коммитов.

---
5. Найдите коммит в котором была создана функция func providerSource.

`git log -S 'func providerSource('`

```
commit 8c928e83589d90a031f811fae52a81be7153e82f
Author: Martin Atkins <mart@degeneration.co.uk
Date:   Thu Apr 2 18:04:39 2020 -0700
```

Коммит: 8c928e83589d90a031f811fae52a81be7153e82f.

---
6. Найдите все коммиты в которых была изменена функция globalPluginDirs.

`git log -S 'func globalPluginDirs'`

```
commit 65c4ba736375607b6af6c035972f7f151232b6c6
Author: Valeriy Pastushenko <i@combin.name>
Date:   Sat May 21 19:53:24 2022 +0300
...

commit 125eb51dc40b049b38bf2ed11c32c6f594c8ef96
Author: Alisdair McDiarmid <alisdair@users.noreply.github.com>
Date:   Thu May 5 10:12:00 2022 -0400
...

commit 22c121df8631c4499d070329c9aa7f5b291494e1
Author: Anna Winkler <3526523+annawinkler@users.noreply.github.com>
Date:   Tue May 3 12:28:41 2022 -0600
...

commit 7c7e5d8f0a6a50812e6e4db3016ebfd36fa5eaef
Author: Valeriy Pastushenko <i@combin.name>
Date:   Fri Sep 3 18:33:10 2021 +0300
...

commit 35a058fb3ddfae9cfee0b3893822c9a95b920f4c
Author: Martin Atkins <mart@degeneration.co.uk>
Date:   Thu Oct 19 17:40:20 2017 -0700
...

commit c0b17610965450a89598da491ce9b6b5cbd6393f
Author: James Bardin <j.bardin@gmail.com>
Date:   Mon Jun 12 15:04:40 2017 -0400
```

Найдено 6 коммитов, следовательно в наиболее раннем из них  
c0b17610965450a89598da491ce9b6b5cbd6393f функция создана,  
а в остальных отредактирована.

---
7. Кто автор функции synchronizedWriters?

`git log -S 'func synchronizedWriters(' --pretty=format:"%h %an %ad"`

```
bdfea50cc8 James Bardin Mon Nov 30 18:02:04 2020 -0500
5ac311e2a9 Martin Atkins Wed May 3 16:25:41 2017 -0700
```

Автор функции synchronizedWriters() — Martin Atkins.

---

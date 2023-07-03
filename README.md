Начало


1. Просмотрите историю коммитов в своём проекте и выберите три случайных коммита. Просмотрите изменения, которые были в них сделаны.

2. Верните эти изменения командой git revert последовательно, чтобы в итоге получилось тоже три коммита.

3. Попробуйте отменить эти три коммита:
* последний — командами git reset --soft и git restore;
* предпоследний — командой git reset --mixed и git restore;
* первый — командой git reset --hard.



## Информация по командам git reset --soft и git restore

1. git reset --soft: Эта команда позволяет отменить коммиты, сохраняя изменения в рабочей директории и индексе Git. При использовании git reset --soft указывается коммит, до которого вы хотите откатиться. После выполнения этой команды изменения из указанного коммита будут удалены из истории коммитов, но останутся в рабочей директории и индексе. Вы можете внести дополнительные изменения и создать новый коммит, сохраняя предыдущую историю коммитов.

2. git restore: Эта команда позволяет восстанавливать файлы из индекса или из последнего коммита. С помощью git restore вы можете отменить изменения, сделанные в файлах и вернуть их к состоянию, которое они имели в последнем коммите или в индексе. Команда принимает различные флаги и аргументы для указания файлов или директорий, которые нужно восстановить.
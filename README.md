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

## Информация по командам git reset --mixed и git restore

1. git reset --mixed: Эта команда используется для отмены коммитов и сброса индекса Git. При выполнении git reset --mixed указывается коммит, до которого вы хотите откатиться. Все коммиты после указанного коммита будут удалены из истории, а изменения этих коммитов вернутся в рабочую директорию как незафиксированные изменения. Однако, состояние индекса также будет изменено, и все изменения будут сняты с индекса, позволяя вам сделать новые выборы о том, какие изменения включить в следующий коммит.

2. git restore: Команда git restore используется для восстановления файлов в рабочей директории из индекса или последнего коммита. Вы можете указать конкретные файлы или директории, которые нужно восстановить. Если вы используете git restore без указания флагов или путей к файлам, он будет применяться к текущей директории и всем ее содержимым. Команда восстанавливает файлы в их состояние из индекса или последнего коммита, но не изменяет историю коммитов.
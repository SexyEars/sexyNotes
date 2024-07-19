Mutex (mutual exclusion) - примитив синхронизации, обеспечивающий взаимное исключение исполнения критических участков кода.

Методы mutex'a:
1. Lock - перед тем как обращаться к разделяемым данным (захватываем mutex)
2. Unlock (когда заканчиваем работать с разделяемыми данными)

Код между lock и unlock - критическая секция.
![[mutexLockUnlock.png]]

Свойства mutex'a:
1. Взаимное исключение (safety) - между lock'ом и unlock'ом всегда есть как минимум 1 поток.
2. Свобода от взаимной блокировки (liveness) - если один или несколько потоков пытаются захватить свободный mutex, то один из lock'ов должен завершиться. Также называется гарантией прогресса.
	1. Глобальный прогресс - каждый захватывает mutex.
	2. Прогресс - кто-то захватывает mutex (один из них может никогда не захватить mutex).

Легкая и тяжелая форма взаимных блокировок:
1. Deadlock - потоки не выйдут из deadlock'a что бы ни делал планировщик.
2. Livelock - потоки мешают прогрессу друг друга, но при удачном планировании разойдутся.

Атомарные операции (store, load, fetchAnd(прочитать и добавить), compareAndSwap) — операции, выполняющиеся как единое целое либо не выполняющиеся вовсе. Т. е. это операция, во время исполнения которой данные, читаемые/изменяемые этой операцией не могут быть изменены другой операцией.

Spinlock - блокирует поток и при ожидании заставляет его кружиться на ядре.
Busy waiting (паттерн ожидания) - крутимся до тех пор, пока другой поток не отпустит спинлок. #pattern
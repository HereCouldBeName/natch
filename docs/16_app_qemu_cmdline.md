<div style="page-break-before:always;">
</div>

# <a name="app_qemu_cmdline"></a>Приложение 2. Командная строка эмулятора QEMU

Пример командной строки для запуска QEMU выглядит следующим образом:

``./qemu-system-x86_64 -hda debian.qcow2 -m 6G -monitor stdio -netdev user,id=net0 -device e1000,netdev=net0``

- ``qemu-system-x86_64``: исполняемый файл эмулятора
- ``-hda debian.qcow2``: подключение образа гостевой операционной системы
- ``-m 6G``: выделение оперативной памяти гостевой системе
- ``-monitor stdio``: подключение управляющей консоли эмулятора к терминалу
- ``-netdev user,id=net0 -device e1000,netdev=net0``: настройка сети и подключение сетевой карты модели е1000

Командная строка выше просто запускает эмулятор с заданным образом диска. Для работы с *Natch* рекомендуется использовать
команды инструмента (подробнее в разделе [Командный интерфейс Natch](3_natch_cmd.md#natch_cmd)).

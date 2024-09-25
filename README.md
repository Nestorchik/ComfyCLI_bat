<p aling="center"><img src="img\cli.png"></p>

# Установка ComfyUI через Comfy-CLI

В этом примере показана установка и развертывание системы **ComfyUI** с использованием исключительно команд **"comfy-cli"**.

- Скачайте bat-файл, поместите его в новую папку (можно с кириллицей и пробелами!).
- проверьте, что у вас в системе установлены "curl" + "tar" + "git", и что они находятся "в путях" (PATH).
- как проверить и скачать, описано тут: [ссылка](https://dzen.ru/a/ZvRGuDDkgRuJAEr2)
- запустите файл **"new_comfy_cli.bat"**, и ждите конца установки.

  **Бат-файл выполняет следующие действия в следующем порядке:**

- включает изоляцию системных переменных **setlocal** от изменений из самого себя
- добавляет свои пути в PATH
- с помощью **"curl"** скачивает дистрибутив питона
- с помощью **"tar"** разархивирует его
- обновляет в питоне "**pip"**
- устанавливает пакет **"comfy-cli"**
- дает команду "comfy-cli" установить **ComfyUI** в текущую папку "без вопросов", "карта NVIDIA"
- _в комментах перечислены варианты ключей установки на разные видеокарты_
- дает команду на установку кастомных нод **"ComfyUI-Crystools"** и **"ComfyUI-Crystools-save"**
- генерирует и сохраняет бат-файл **"run_ComfyUI.bat"** с командами на запуск **ComfyUI** через интерфейс **"comfy-cli"**
- генерирует и сохраняет бат-файл **"example_download_model.bat"** с набором команд текущему **"comfy-cli"** на скачивание и установку файла модели **"v1-5-pruned-emaonly.ckpt"**
- генерирует и сохраняет бат-файл **"example_install_node.bat"** с набором команд текущему **"comfy-cli"** на скачивание и установку кастомной ноды **"ComfyUI-OpenPose-Editor"**
- генерирует и сохраняет бат-файл **"update_all_ComfyUI.bat"** с набором команд текущему **"comfy-cli"** на обновление всех установленных нод и самого **ComfyUI**
- запускает установленный с помощью **"comfy-cli"** интерфейс **ComfyUI**

  Сгенерированные bat-файлы сохраняются в текущую папку и из самого bat-файла не запускаются, запускайте их самостоятельно.

  Этот файл является **ПРИМЕРОМ** управления интерфейсом **ComfyUI** через интерфейс командной строки **"comfy-cli"**, в котором применены основные команды **"comfy-cli"** на установку интерфейса, добавления кастомных нод, установки моделей и обновления всего установленного.

  Кто заинтересуется, может, разобравшись с этим примером, ознакомиться [с остальными командами **"comfy-cli"** на PyPi](https://pypi.org/project/comfy-cli)

  И, да: comfy-cli под Windows хранит свой ini-файл по адресу:
  
  - Users\User_Name\AppData\Local\comfy-cli\config.ini
  - %LOCALAPPDATA%\comfy-cli\config.ini

  Dzen: https://dzen.ru/a/ZvQHVE-FzDG136lc

  >
  > # Installing ComfyUI via Comfy-CLI

This example shows the installation and deployment of the **ComfyUI** system using only the **"comfy-cli"** commands.

- Download the bat file, place it in a new folder (you can use Cyrillic and spaces!).
- check that you have "curl" + "tar" + "git" installed in your system, and that they are "in the paths" (PATH).
- how to check and download is described here: [link](https://dzen.ru/a/ZvRGuDDkgRuJAEr2)
- run the **"new_comfy_cli.bat"** file, and wait for the installation to complete.

**The bat file performs the following actions in the following order:**

- enables isolation of system variables **setlocal** from changes from itself
- adds its paths to PATH
- downloads the python distribution using **"curl"**
- unzips it using **"tar"**
- updates "**pip"** in python
- installs the **"comfy-cli"** package
- gives the "comfy-cli" command to install **ComfyUI** in the current folder "no questions asked", "NVIDIA card"
- _the comments list options for installing keys for different video cards_
- gives the command to install custom nodes **"ComfyUI-Crystools"** and **"ComfyUI-Crystools-save"**
- generates and saves the bat file **"run_ComfyUI.bat"** with commands to launch **ComfyUI** through the interface **"comfy-cli"**
- generates and saves the bat file **"example_download_model.bat"** with a set of commands for the current **"comfy-cli"** to download and install the model file **"v1-5-pruned-emaonly.ckpt"**
- generates and saves the bat file **"example_install_node.bat"** with a set of commands for the current **"comfy-cli"** to download and install the custom node **"ComfyUI-OpenPose-Editor"**
- generates and saves the bat file **"update_all_ComfyUI.bat"** with a set of commands for the current **"comfy-cli"** to update all installed nodes and **ComfyUI** itself
- launches the **ComfyUI** interface installed using **"comfy-cli"**

Generated bat files are saved to the current folder and from bat file itself does not run, run them yourself.

This file is an **EXAMPLE** of managing the **ComfyUI** interface via the **"comfy-cli"** command line interface, which uses the basic **"comfy-cli"** commands to install the interface, add custom nodes, install models and update everything installed.

If you are interested, you can, after figuring out this example, familiarize yourself with [the other **"comfy-cli"** commands on PyPi](https://pypi.org/project/comfy-cli)

And, yes: comfy-cli under Windows stores its ini file at:

- Users\User_Name\AppData\Local\comfy-cli\config.ini
- %LOCALAPPDATA%\comfy-cli\config.ini

Dzen: https://dzen.ru/a/ZvQHVE-FzDG136lc
  

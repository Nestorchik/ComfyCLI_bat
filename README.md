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
  
  >
  > # 通过 Comfy-CLI 安装 ComfyUI

此示例显示仅使用 **“comfy-cli”** 命令安装和部署 **ComfyUI** 系统。

- 下载bat文件，将其放在一个新文件夹中（您可以使用西里尔字母和空格！）。
- 检查您的系统上是否安装了“curl”+“tar”+“git”，并且它们位于“路径”(PATH) 中。
- 如何检查和下载如下所述：[链接](https://dzen.ru/a/ZvRGuDDkgRuJAEr2)
- 运行文件**“new_comfy_cli.bat”**并等待安装完成。

 **bat 文件按以下顺序执行以下操作：**

- 能够将系统变量 **setlocal** 与其自身的更改隔离
- 将您的路径添加到 PATH
- 使用 **“curl”** 下载 python 发行版
- 使用 **“tar”** 解压它
- 更新 python 中的“**pip”**
- 安装**“comfy-cli”**包
- 给出命令“comfy-cli”将 **ComfyUI** 安装到当前文件夹“无问题”、“NVIDIA 卡”
- _不同显卡安装密钥的评论列表选项_
- 提供安装自定义节点的命令 **“ComfyUI-Crystools”** 和 **“ComfyUI-Crystools-save”**
- 生成并保存一个bat文件**“run_ComfyUI.bat”**，其中包含通过**“comfy-cli”**界面启动**ComfyUI**的命令
- 生成并保存一个bat文件**“example_download_model.bat”**，其中包含当前**“comfy-cli”**的一组命令，用于下载和安装模型文件**“v1-5-pruned-emaonly” .ckpt"**
- 生成并保存一个bat文件**“example_install_node.bat”**，其中包含当前**“comfy-cli”**的一组命令，用于下载和安装自定义节点**“ComfyUI-OpenPose-Editor”* *
- 生成并保存一个bat文件**“update_all_ComfyUI.bat”**，其中包含当前**“comfy-cli”**的一组命令，以更新所有已安装的节点和**ComfyUI**本身
- 启动使用 **“comfy-cli”** 安装的 **ComfyUI** 界面

 生成的bat文件保存在当前文件夹中，并且不是从bat文件本身启动运行它们；

 该文件是通过命令行界面**“comfy-cli”**管理**ComfyUI**界面的**示例**，其中基本**“comfy-cli”**命令用于安装界面并添加自定义节点，安装模型并更新安装的所有内容。

 任何有兴趣的人都可以在了解这个示例后，查看[PyPi 上的 **“comfy-cli”** 命令的其余部分](https://pypi.org/project/comfy-cli)

 并且，是的：Windows 上的 comfy-cli 将其 ini 文件存储在：

 - 用户\用户名\AppData\Local\comfy-cli\config.ini
 -%LOCALAPPDATA%\comfy-cli\config.ini

 德禅：https://dzen.ru/a/ZvQHVE-FzDG136lc

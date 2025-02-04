# NVDA remote远程协助插件-NVDA Remote Access
版本 2.4

欢迎使用NVDA 远程协助插件，此插件允许您连接到运行免费NVDA屏幕阅读器的另一台计算机。无论两台电脑就在一间屋里面，还是在地球两端，都没有区别。连接很简单，只需要几步操作。您可以连接到其他人的计算机，或允许受信任的人连接到您的系统以执行日常维护，诊断问题或提供培训。

## 使用之前

您需要在两台计算机上安装NVDA 和 远程协助插件。

NVDA和远程协助插件的安装都是基本操作。如果您不会，可以在NVDA的用户指南中找到相关的帮助。

## 更新

更新插件时，如果已在安全桌面上安装了NVDA 远程，则建议您也在安全桌面上更新副本。
请先更新现有的插件。然后打开NVDA菜单 > 选项 > 设置 > 常规，并按下“应用以保存的配置到欢迎界面和其他安全界面（需要管理员权限）”的按钮。

## 通过中继服务器开始远程会话
### 在被控端的计算机上
1. 打开NVDA菜单 > 工具 > 远程 > 连接。
2. 在第一组单选按钮中选择“客户端”。
3. 在第二组单选按钮中选择允许此计算机被控制。
4. 在主机编辑框中，输入要连接的服务器的主机，例如nvdaremote.com。当特定服务器使用备用端口时，您可以用 host:port 的形式输入主机，例如 nvdaremote.com:1234。
5. 在密钥编辑框中输入一个密要，或按下生成密钥按钮。
   - 这个密钥是其他人用来控制您的计算机的关键凭证。
   - 被控端与控制端需要使用相同的密钥。
6. 按确认。完成后，您将听到一声蜂鸣声，这时就已经连接了。

### 在控制端的计算机上
1. 打开NVDA菜单 > 工具 > 远程 > 连接。
2. 在第一组单选按钮中选择“客户端”。
3. 在第二组单选按钮中选择控制另一台计算机。
4. 在主机编辑框中，输入要连接的服务器的主机，例如nvdaremote.com。当特定服务器使用备用端口时，您可以用 host:port 的形式输入主机，例如 nvdaremote.com:1234。
5. 在密钥编辑框中输入一个密要，或按下生成密钥按钮。
   - 这个密钥是其他人用来控制您的计算机的关键凭证。
   - 被控端与控制端需要使用相同的密钥。
6. 按确认。完成后，您将听到一声蜂鸣声，这时就已经连接了。

## 直接连接
“连接”对话框中的“服务器”选项允许您设置直接连接。
选择此项后，选择您的连接模式（控制另一台计算机还是允许这台计算机被控制）。
对方应该用相反的方式与您建立连接。

选择模式后，您可以使用“获取公网 IP”按钮获取公网 IP地址
确保正确转发了在端口编辑框中输入的端口。
如果检测到您的端口（默认情况下为6837）无法访问，则会显示警告。
请转发您的端口，然后重试。
注意：转发端口的过程超出了本文档的范围。有关详细说明，请参阅路由器随附的信息。

在密钥编辑框中输入密钥，或按下生成按钮。对方需要您的公网 IP和密钥。如果您在端口编辑框中输入了默认端口（6837）以外的端口，请确保另一方将指定的端口正确添加到了主机地址，格式为 公网ip地址:端口。

按下确认后，您将成功连接。
在对方连接过程中，您可以正常使用 NVDA 远程。

## 控制远程计算机

一旦两方连接成功，控制方可以按f11开始控制远程计算机（如，发送键盘按键或盲文输入）。
当NVDA朗读“控制远程计算机”时，您执行的键盘按键和盲文输入将发送到远程计算机。此外，当控制方使用盲文点显器时，也会在点显器上显示来自远程计算机的信息。再次按 f11 可停止控制并切换回本地计算机。
为获得最佳的兼容性，请确保控制方与被控方的 NVDA 使用了相同的键盘布局。

## 分享您的绘画

要共享链接以便其他人可以轻松加入您的NVDA 远程会话，请在“远程”菜单中选择“复制链接”。
如果您作为控制方，此链接可以让其他人的计算机被控制。
如果您作为被控方，则此链接可以让其他人来控制您的计算机。
得到链接的一方，可以将链接复制到剪贴板，然后使用 Windows + R 打开运行对话框，粘贴以 nvdaremote:// 开头的链接并确定，随后按照提示可以控制对方的计算机或者允许对方控制自己的计算机。

## 发送 Ctrl + Alt + Del
在控制另一台计算机的过程中，无法正常发送 CTRL + Alt + del 快捷键。
如果需要发送CTRL + Alt + del，使远程计算机进入安全桌面，请使用此命令。

## 远程控制无人值守的计算机

有时，您可能希望远程控制您自己的另一台计算机。比如您正在外面旅行，此时希望通过手边的笔记本控制家里的计算机，这就特别有用了。又或者，您就在家里，只是想控制另一个房间的计算机。仅需要进行一点额外的准备工作就可以方便地实现无人值守的远程控制。

1. 进入NVDA菜单，选择“工具”，然后选择“远程”。最后，找到“选项”按“回车键”打开远程插件的“选项对话框”。
2. 选中“启动时自动连接到控制服务器”复选框。
3. 选择是“使用远程中继服务器”还是“主控服务器”。
4. 在第二组单选按钮中选择“允许此计算机被控制”。
5. 如果您选择“主控服务器”，则要确保在端口编辑框里填入的端口可以被访问（默认端口为6837）。
6. 如果要使用中继服务器，请填写主机和密钥，按“tab键”切换到“确认”按钮，然后按下“回车键”。在这种情况下，“生成密钥”选项不可用。最好输入一个你记的住的密钥，这样你就可以从任何位置轻松使用NVDA 远程了。

对于一些高级用途，您还可以将NVDA 远程设置为“启动后自动连接到控制服务器”，然后在第二组单选按钮中选择“控制另一台计算机”。

注意： 您需要重新启动 NVDA 来使选项对话框中配置的自动连接等选项生效。


## 远程计算机静音

如果您不想听到远程计算机的语音或 NVDA 的提醒声音，只需打开 NVDA菜单 > 工具 > 远程。下光标找到“远程计算机静音”，然后按回车键。请注意，当控制方在此状态下操作被控方计算机时，此选项不会禁用控制方点显器的远程盲文输出。

## 结束远程会话

要结束远程会话，请执行以下操作：

1. 在控制计算机上，按F11停止控制远程机器。您应该听到或在点显器上读到消息：“控制本地计算机”。如果您听到或读到“控制远程计算机”，请再按一次F11。
2. 打开NVDA菜单，然后选择工具，远程，然后找到“断开连接”案回车确认。

## 发送剪贴板

远程菜单中的“发送剪贴板”选项允许您从剪贴板中发送文本内容。
使用该功能，剪贴板上的任何文本都会被发送到对方计算机。

## 配置 NVDA 远程在安全桌面上运行

若使 NVDA 远程能够在安全桌面上运行，必须在安全桌面上运行的 NVDA 中安装远程插件。

1. 从NVDA菜单中，选择：选项，然后找到常规设置。
2. 选择“应用以保存的配置到欢迎界面和其他安全界面（需要管理员权限）”按钮，然后按下回车键。
3. 对有关复制设置和复制插件的提示选择“是”，并接受可能出现的“用户帐户控制”提示。
4. 复制设置后，点击“确认”按钮。按tab键再找到“确认”按钮后按回车键退出对话框。

在安全桌面上安装 NVDA 远程后，您在远程控制过程中，切换到安全桌面时，您也会接收到语音和盲文输出。

## 贡献者
我们要感谢以下贡献者，其中包括帮助实现NVDA 远程项目的人员。

* Hai Nguyen Ly
* Chris Westbrook
* Thomas Huebner
* John F Crosotn III
* Darrell Shandrow
* D Williams
* Matthew McCubbin
* Jason Meddaugh
* ABDULAZIZ ALSHMASI.
* Tyler W Kavanaugh
* Casey Mathews
* Babbage B.V.
* Leonard de Ruijter
* NV Access
* Reef Turner

## 更新日志
### 版本 2.4（非官方更新日志）
1. 兼容 NVDA2021.1；
2. 受信任的指纹，安全机制增强；
3. 使用快捷键切换远程计算机静音时给出状态提示；
4. 连接状态可选使用音效代替 Beep 提示；

### 版本 2.3
* 迁移到 Python 3
* 移除 Python 2 支持
* 升级到 NVDA 2019.3的 meet changed API , 包括：
  - Speech refactor
  - 修改点显器支持。

### 版本 2.2

* 支持IPv6
* 支持NVDA 2018.3以及旧版本
* 支持特定型号的盲文手势

### 版本 2.1

* 允许控制本机时固定连接不保存
* 添加了一个脚本，用ctrl + shift + NVDA + c发送剪贴板
* 盲文输入现在可在浏览模式下使用
* 支持模型特定的盲文显示手势
* NVDA Remote生成的蜂鸣声不再使NVDA卡死

### 版本 2.0

* 支持远程盲文
* 支持nvdaremote://这种链接形式
* 把设置集中到一个对话框，与NVDA的其余部分相符
* 修复了我们控制的域名portcheck.nvdaremote.com 恢复检查端口功能
* 支持在主模式下自动连接到控制服务器
* 修复了文档中的渲染错误
* 更新到协议版本2，其中包括每个远程消息中的原始字段
* 重要的代码清理允许将来更容易修改代码


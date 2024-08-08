## 验证系统需求

为了安装和运行Flutter,
您的 {{include.os}} 环境必须满足以下软硬件需求。

### 硬件需求

您在 {{include.os}} 的Flutter开发环境必须满足以下最小硬件需求：

|     要求                      |                                    最小值                                |    推介值     |
|:-----------------------------|:------------------------------------------------------------------------:|:-------------------:|
| 处理器核心数量                 | 4                                                                        | 8                   |
| 内存大小(GB)                  | 8                                                                        | 16                  |
| 屏幕分辨率                     | WXGA (1366 x 768)                                                        | FHD (1920 x 1080)   |
| 空余硬盘大小                   | {% include docs/install/reqs/linux/storage.md target=include.target %}

{:.table .table-striped}

{% if include.os == 'ChromeOS' and include.target == 'Android' %}
寻找哪些Chrome OS设备适用于安卓Flutter应用开发,
请查看 [ChromeOS docs][chromeos-docs]。
{% endif %}

[chromeos-docs]: https://chromeos.dev/en/android-environment

### 软件需求

为了在 {{include.target}} 上运行和编译Flutter代码,
您需要拥有以下版本的 {{include.os}} 系统和列出的所有软件。

{% render docs/install/admonitions/install-dart.md %}

#### 操作系统

{% if include.os == 'Linux' %}
{%- capture supported-os %}
Debian Linux {{site.devmin.linux.debian}} 或更新
和 Ubuntu Linux {{site.devmin.linux.ubuntu}} 或更新
{% endcapture -%}
{% else %}
{% assign supported-os = 'ChromeOS' %}
{% endif %}

Flutter支持 {{supported-os}}.

#### 开发工具 {:.no_toc}

{% include docs/install/reqs/linux/software.md target=include.target os=include.os %}

{% render docs/install/reqs/flutter-sdk/flutter-doctor-precedence.md %}

上述软件的开发者或公司，组织为他们的软件提供支持。
如果对安装这些软件有问题，请参阅各自的开发文档。

## 配置一个文本编辑器或IDE

您可以用任意您喜欢的文本编辑器或带有Flutter命令行工具的IDE开发Flutter应用。


使用带有Flutter扩展或插件的IDE可以完成代码，语法高亮显示、小部件编辑辅助、调试和其他功能。

比较热门的选择:

* [Visual Studio Code][vscode] {{site.appmin.vscode}} 或更新
  带有 [Flutter extension for VS Code][]扩展。
* [Android Studio][] {{site.appmin.android_studio}} 或更新
  带有 [Flutter plugin for IntelliJ][]插件。
* [IntelliJ IDEA][] {{site.appmin.intellij_idea}} 或更新
  带有 [Flutter plugin for IntelliJ][]插件。

:::推介
Flutter团队推介安装 [Visual Studio Code][vscode]
{{site.appmin.vscode}}或更新，并且安装[Flutter extension for VS Code][] 扩展。
这种组合会简化Flutter SDK的安装

:::
[Android Studio]: https://developer.android.com/studio/install#linux
[IntelliJ IDEA]: https://www.jetbrains.com/help/idea/installation-guide.html
[vscode]: https://code.visualstudio.com/docs/setup/linux
[Flutter extension for VS Code]: https://marketplace.visualstudio.com/items?itemName=Dart-Code.flutter
[Flutter plugin for IntelliJ]: https://plugins.jetbrains.com/plugin/9212-flutter

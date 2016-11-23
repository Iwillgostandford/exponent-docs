..建立和运行:

**************
建立和运行
**************

这份指南的目标就是建立一个 Exponent 程序并尽可能让它运行起来。

关于这个，我们应该在机器开发环境中安装好了 XDE 和在 emulator 中安装好了 Exponent 的服务。如果没有，现在在继续之前返回的安装指南`Installation <../introduction/installation.html>`_ 。

好了，让我们开始吧！

创建一个新账户。
"""""""""""""""""

在打开 XDE 之前，你会被要求输入用户名和密码。用你喜欢的用户名和密码填完这个表格并点击继续按钮——如果用户名还没被用，我们会自动新建一个账户给你。

创建项目
""""""""""""""""""""

按下``Project``并选择``New Project``，然后选择``Tab Navigation``选项因为这会是一个好的开始，然后在弹出窗口输入你的项目名称，在这里我将其命名为``first-project``，然后点创建。

然后，选择项目的储存位置，我在``~/coding``保存了我所有的有趣项目，所以我找到了那个目录并点击了打开。

现在 XDE 已被初始化，而且新项目已经在指定目录建立好了：它复制了基本的模板和安装了``react``, ``react-native``和``exponent``。

但项目已经初始化而且可以使用时，你会在 XDE 记录中看到"React packager ready"的字样。

"React packager" 是一个用`Babel <https://babeljs.io/>`_来编译我们的 app JavaScript 代码的简单的 HHTP 服务，并将其呈递到 Exponent app 中。

.. epigraph::
  **提示:** 如果你使用的是 MacOS 然后 XDE 卡在了"Waiting for packager and tunnel to start"，你可能需要`安装 watchman 在你的机器 <https://facebook.github.io/watchman/docs/install.html#build-install>`_。最简单的方法是使用`Homebrew <http://brew.sh/>`_, ``brew install watchman``。

在你的手机或者虚拟机上打开应用
"""""""""""""""""""""""""""""""""""""""

You'll see that XDE shows you a URL like ``http://4v-9wa.notbrent.mynewproject.exp.direct:80``- feel free to open this up in your browser, you will see that it serves up some JSON. This JSON is the Exponent manifest.
We can open our app by opening the Exponent app on our phone typing this URL into the address bar. Alternatively, press ``Send Link``, enter your phone number, and press ``Send Link`` again. Open the message on your phone and tap on the link to open it in Exponent.
You can share this link with anybody else who has the Exponent app installed, but it will only be available as long as you have the project open in XDE.

To open the app in the iOS simulator you can press the ``Device`` button and choose ``Open on iOS Simulator`` (macOS only).
To open the app in the Android emulator, first boot it up and then press ``Device`` and ``Open on Android``.

Making your first change
""""""""""""""""""""""""

Open up ``screens/HomeScreen.js`` in your new project and change any of the
text in the ``render()`` function. You should see your app reload with your changes.

.. _live-reload-help:
Can't see your changes?
^^^^^^^^^^^^^^^^^^^^^^^
Live reload is enabled by default, but let's just make sure we go over the
steps to enable it in case somehow things just aren't working.

- First, make sure you have :ref:`development mode enabled in XDE <development-mode>`.
- Next, close the app and reopen it.
- Once the app is open again, shake your device to reveal the developer menu. If you are using an emulator, press ``⌘+d`` for iOS or ``ctrl+m`` for Android.
- If you see ``Enable Live Reload``, press it and your app will reload. If you
  see ``Disable Live Reload`` then exit the developer menu and try making
  another change.

  .. figure:: img/developer-menu.png
    :width: 70%
    :alt: In-app developer menu

Manually reloading the app
-------------------------
- If you've followed the above steps and live reload **still** doesn't work,
  press the button in the bottom right of XDE to send us a support request.
  Until we resolve the issue for you, you can either shake the device and press
  ``Reload``, or use one of the following tools which work both with an without
  development mode.

  .. figure:: img/exponent-refresh.png
    :width: 90%
    :alt: Refresh using Exponent buttons

Congratulations!
----------------

You have created a new Exponent project, made a change, and seen it update.

Next Steps
----------

- The :ref:`Additional Resources <additional-resources>` page has links to several
  open-source Exponent projects so you can see some working examples.
- Read about the :ref:`Exponent SDK <exponent-sdk>` to learn about some useful
  APIs we provide out of the box.
- Read some of our other guides, such as how to implement
  :ref:`Push Notifications <push-notifications>`, how we can take care of
  :ref:`Assets <all-about-assets>` for you, or how to build
  :ref:`Standalone Apps <building-standalone-apps>` you can submit to Apple or Google.
- Join us on Slack to get your questions answered.

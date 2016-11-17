.. _faq:

FAQ
==========================

Exponent收费吗? 怎么收?
----------------------------

Exponent是完全免费的。

我们的计划是无限期的免费。

Exponent也是开源的, 所以你不需要非得相信我们会坚持免费。

我们可能最终会通过一些服务(基于Exponent)或者一些高级的支持和咨询来收取一些费用。

如果Exponent免费的话，你们怎么赚钱?
------------------------------------------

暂时，我们不赚钱。我们是一个比较小的团队，大家都想做这个东西。我们一直保持较低的开销，大部分是自筹资金。只有有人用Exponent, 我们就会继续做下去。

我们认为如果Exponent足够好，最终我们会帮助开发者赚到钱，然后我们可以分享一小部分钱。可以通过帮助开发者赚钱(别人用他们的软件), 或者帮助他们在apps里边投广告，或者其他途径。这方面我们目前没有清晰的计划，我们的首要任务是让Exponent真正帮助用户，并且尽可能有更多人来用。

Exponent和React Native有什么区别?
---------------------------------------------------------

Exponent类似Rails for React Native。很多东西已经帮你搭建好了，所以你可以更快开始，并且避免入更多没必要的坑。

Exponent开发不需要Xcode或者Android Studio。你仍然用你最钟爱的编辑器(Atom, vim, emacs, Sublime, VS Code, 等等)来写Javascript(或者其他能编译成Javascript的语言). 你可以在Mac, Windows或者Linux上运行XDE(我们的桌面应用)。

下面是一些Exponent提供的一些开箱即用的功能:

* **支持 iOS 和 Android**

  你可以同时在iOS和Android上使用用Exponent开发的应用, 你不需要分别为不同平台编译。只需要在Exponent手机客户端(或者PC虚拟机)上打开任何应用就可以了。

* **推送通知**
  推送通知同时支持iOS和Android, 统一的API.
  你不需要设置APNS，GCM/FCM, 或者设置ZeroPush之类的。我们已经支持的不能再简单了!

* **Facebook, Google 登录**
  通常你自己设置的话，需要花费比较长的时间。而在Exponent上，大概你需要10分钟或者更少时间。

* **即时更新**
  所有的Exponent应用只需要点击 `Publish` 就可以在几秒内更新。你不需要设置任何东西, 直接可以用。如果你不用Exponent的话，要么你是用microsoft Code Push, 要么是自己的解决方案。

* **资源(图片等)管理**
  在Exponent里图片，视频，字体等都是在网上动态分布的。这也就意味它们都支持即时更新，可以实时更换。 Exponent负责上传这些资源到一个CDN，所以你的用户就会加载快一些。

  没有Exponent的话, 通常你需要打包这些资源到应用里，这样子你就不能实时替换。或者你需要自己上传到一个CDN。

* **使React Native版本更新真正简单**

  我们每隔几个礼拜会发布新的Exponent版本。你可以停留在稍微老一点的React Native版本，或者升级到新的版本。不需要担心重新编译你的app. 你只需要负责升级你的Javascript代码就好了。

**但是不支持native modules...**

Exponent目前最大的限制就是不支持自己写的native代码。
下面这个问题会详细解释。

那我怎么添加自己写的或者三方库native代码?
-------------------------------------------------------

目前Exponent不支持custom native代码, 包括需要native组件的三方库。在Exponent项目里，你不会去写native代码--纯Javascript。

在 :ref:`Exponent SDK <exponent-sdk>` 里，我们提供很多常用的，高质量的native库。 但是如果你需要一些非常自定义的功能，比如实时视频处理或者底层蓝牙无线升级控制--Exponent目前满足不了，你应该用React Native。

你可以仅仅用Javascript做很多你认为做不了的事情--实际上，我们建议可能的话尽量用JS, 因为支持多个平台，而且更健壮些--你就不需要用native写的UI组件了(几乎都有对应的用pure Javascript实现的更好的实现)。

我们一直在改进SDK还有支持更多native功能。请告诉我们如果有哪些我们没有提供的功能，然后我们会添加支持如果有更多的人需要这些功能。(Tweet @我们, 或者加入Slack, 或者e-mail support@getexponent.com)。

最后, Exponen是开源的，所以你可以fork代码或者贡献。如果你想提PR的话，请加入我们的Slack。

我可以在Exponent上用Relay吗?
------------------------------

当然可以! 修改你的 ``.babelrc`` 成:

.. code-block:: json

  {
    "presets": [
      "react-native-stage-0/decorator-support",
      {"plugins": ["./pathToYourBabelRelayPlugin/babelRelayPlugin"]}
    ],
    "env": {
      "development": {
        "plugins": ["transform-react-jsx-source"]
      }
    }
  };

替换 ``./pathToYourBabelRelayPlugin`` 你的Relay插件路径。

我怎么迁移已经存在的React Native项目到Exponent上?
--------------------------------------------------------------------

我们提供了一些迁移工具:
- 安装Exponent命令行工具 ``npm install -g exp``
- 在你的项目目录，运行 ``exp convert``

我们会尽最大可能自动迁移你的项目，而且我门会提供接下来你需要手动操作的一些提示。

注意: 请先备份或者commit你的代码
convert的结果可能会有很大差异，取决于你的项目里包含了什么。如果你的native库依赖和Exponent SDK比较类似，通常这个过程需要几分钟(不包含 ``npm install`` 时间)。请随时问我们如果你遇到任何问题。

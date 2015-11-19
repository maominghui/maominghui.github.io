---
layout: post
title: NSUserDefaults用法
description: "iOS"
category: iOS
tags: [iOS]
imagefeature: pic-2014-09-08.jpg
comments: true
mathjax: null
featured: true
published: true
---


<code>

	NSDictionary* defaults = [[NSUserDefaults standardUserDefaults] 	dictionaryRepresentation];
 
	NSLog(@"Defaults: %@", defaults);
</code>

> 用来获取设备上的所有的NSUserDefaults的设置
<code>

	Defaults:{
    AddingEmojiKeybordHandled = 1;
    AntialiasedFontDilationEnabled = 0;
    AppleITunesStoreItemKinds =     (
        podcast,
        artist,
        "itunes-u",
        booklet,
        document,
        movie,
        eBook,
        software,
        "software-update",
        "podcast-episode"
    );
    AppleKeyboards =     (
        "zh_Hans-Pinyin@sw=Pinyin-Simplified;hw=US",
        "en_US@hw=US;sw=QWERTY",
        "emoji@sw=Emoji",
        "en_US@hw=US;sw=QWERTY"
    );
    AppleKeyboardsExpanded = 1;
    AppleLanguages =     (
        "zh-Hans-US",
        "en-US"
    );
    AppleLanguagesDidMigrate = "9.1";
    AppleLocale = "zh-Hans_US";
    ApplePasscodeKeyboards =     (
        "en_US"
    );
    MSVLoggingMasterSwitchEnabledKey = 0;
    NSInterfaceStyle = macintosh;
    NSLanguages =     (
        "zh-Hans-US",
        "en-US",
        en
    );
</code>




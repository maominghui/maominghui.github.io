---
layout: post
title: Objective-C Autorelease Pool及强引用和弱引用
description: "Objective-C Autorelease Pool"
category: iOS
tags: [iOS]
imagefeature: pic-2014-09-08.jpg
comments: true
mathjax: null
featured: true
published: true
---

{% highlight Objective-C %}
#import "ViewController.h"
__weak NSString *string_weak_ = nil;

@interface ViewController ()

@end

@implementation ViewController



- (void)viewDidLoad {
    [super viewDidLoad];
    
    //场景 1
    NSString *string = [NSString stringWithFormat:@"Maominghui"];
    string_weak_ = string;
    NSLog(@"string: %@", string_weak_);
    // Do any additional setup after loading the view, typically from a nib.
}

-(void)viewWillAppear:(BOOL)animated
{
    [super viewWillAppear:animated];
    NSLog(@"string: %@", string_weak_);
}

-(void)viewDidAppear:(BOOL)animated
{
    [super viewDidAppear:animated];
    NSLog(@"string : %@", string_weak_);
}

- (void)didReceiveMemoryWarning {
    [super didReceiveMemoryWarning];
    // Dispose of any resources that can be recreated.
}
{% endhighlight %}

####场景1的打印效果


###

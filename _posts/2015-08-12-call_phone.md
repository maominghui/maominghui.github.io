---
layout: post
title:  "一句代码完成多媒体打电话"
description: "iOS"
category: iOS
tags: [iOS]
imagefeature: pic-2014-09-08.jpg
comments: true
mathjax: null
featured: true
published: true
---

[https://github.com/nsdictionary/CoreMediaFuncManagerVC](https://github.com/nsdictionary/CoreMediaFuncManagerVC)


{% highlight Objective-C %}

#import <UIKit/UIKit.h>
@interface CoreMediaFuncManagerVC : UIViewController

/**
*  打电话
*
*  @param no                   电话号码
*  @param inViewController     需要打电话的控制器
*/
+(void)call:(NSString *)no inViewController:(UIViewController *)vc failBlock:(void(^)())failBlock;
@end
{% endhighlight %}

---

{% highlight Objective-C %}
#import "CoreMediaFuncManagerVC.h"

@interface CoreMediaFuncManagerVC ()


/**
 *  webView
 */
@property (nonatomic,strong) UIWebView *webView;



@end

@implementation CoreMediaFuncManagerVC


- (instancetype)init
{
    self = [super init];
    if (self) {
        
        _webView=[[UIWebView alloc] init];
        
    }
    return self;
}



-(void)viewDidDisappear:(BOOL)animated{
    
    [super viewDidDisappear:animated];
    
    [self removeFromParentViewController];
}


/**
 *  打电话
 *
 *  @param no                   电话号码
 *  @param inViewController     需要打电话的控制器
 */
+(void)call:(NSString *)no inViewController:(UIViewController *)vc failBlock:(void(^)())failBlock{
    
    //拨打电话
    NSURL *url=[NSURL URLWithString:[NSString stringWithFormat:@"tel://%@",no]];
    
    BOOL canOpen = [[UIApplication sharedApplication] canOpenURL:url];
    
    if(!canOpen){//不能打开
        if(failBlock!=nil) failBlock(); return;
    }
    
    CoreMediaFuncManagerVC *mediaVC=[[CoreMediaFuncManagerVC alloc] init];
    
    [vc addChildViewController:mediaVC];
    
    mediaVC.view.frame=CGRectZero;
    mediaVC.view.alpha=.0f;
    
    [vc.view addSubview:mediaVC.view];
    
    //打电话
    NSURLRequest *request=[NSURLRequest requestWithURL:url];
    
    [mediaVC.webView loadRequest:request];
    NSLog(@"Success");
}

-(void)dealloc{
    
    self.webView=nil;
    
    NSLog(@"CoreMediaFuncManagerVC被释放");
}

@end
{% endhighlight %}
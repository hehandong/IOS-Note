###OC宏指令笔记

  ```
  //弱应用，用于block
  #define WS(weakSelf)  __weak __typeof(&*self)weakSelf = self;
  
  
  //调试用的Log，上线后自动会不执行
  #ifdef DEBUG
  #define MTLog(...) NSLog(__VA_ARGS__)
  #else
  #define MTLog(...)
  #endif

  //自定义的颜色宏
  #define MTColor(r, g, b) [UIColor colorWithRed:(r)/255.0 green:(g)/255.0 blue:(b)/255.0 alpha:1.0]
  
  #define MTGlobalBg MTColor(230, 230, 230)
  
  //自定义的通知宏
  #define MTNotificationCenter [NSNotificationCenter defaultCenter]
  ```
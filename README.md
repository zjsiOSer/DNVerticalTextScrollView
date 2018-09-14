# DNVerticalTextScrollView    
### 一种简单的文字轮播    
#### 1. 主要实现思路    
1. 使用 UIScrollView 作为底部承载视图    
2. 根据传入的数组 dataArray 计算其 contentSize ，并添加对应的 UILabel    
#### 2. 创建及使用    
1. 
     
    DNVerticalTextScrollView * scrollView = [[DNVerticalTextScrollView alloc] initWithDataArray:@[@"我是谁",@"我在哪",@"我在干什么"]];
    scrollView.frame = CGRectMake(0, 100, [UIScreen mainScreen].bounds.size.width, 50);
    [self.view addSubview:scrollView];
    scrollView.delegate = self;    
        
2. initWithDataArray
           
    
3. 使用代理回调点击 UILabel 的响应事件    
     
     - (void)dn_textScrollViewSelectedAtIndex:(NSInteger)index content:(NSString *)content {
    
          NSLog(@"%ld---------%@",index,content);
     }

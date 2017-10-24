# OC 代码块

#### Mark Section Title

| Title | Mark Section Title |
| --- | --- |
| Summary | 内容标记 |
| Completion Shortcut | Mark Section Title |

```
#pragma mark - <#Section Title #>
```

#### Mark ChildNode Of Section

| Title | Mark ChildNode Of Section |
| --- | --- |
| Summary | 标记章节的子节点 |
| Completion Shortcut | Mark ChildNode Of Section |

```
#pragma mark └ <#ChildNode#>
```

#### Singleton Instance

| Title | Singleton Instance |
| --- | --- |
| Summary | 单例 |
| Completion Shortcut | Singleton Instance |

```
+ (instancetype)sharedInstance {
    static dispatch_once_t pred;
    __strong static id instance = nil;
    dispatch_once( &pred, ^{
        instance = [[self alloc] init];
    });
    return instance;
}
```

#### Standardize Structure Of Code (VC)

| Title | Standardize Structure Of Code (VC) |
| --- | --- |
| Summary | VC 代码结构 |
| Completion Shortcut | Structure VC |

```
#pragma mark - LifeCycle 生命周期
#pragma mark └ Dealloc
- (void)dealloc {
}
- (void)didReceiveMemoryWarning {
    [super didReceiveMemoryWarning];
    // Dispose of any resources that can be recreated.
}
#pragma mark └ Init
- (instancetype)init {
    if(self = [super init]) {
        
    }
    return self;
}
#pragma mark └ Content View Loading
- (void)viewDidLoad {
    [super viewDidLoad];
    
    [self setupContentViews];
    [self fetchContentData];
    [self setExtentdedLayoutEdgeZero];
}
/**
 *  初始化界面并设置布局
 */
- (void)setupContentViews {
    [self layoutPageSubViews];
}
/**
 *  设置布局
 */
- (void)layoutPageSubViews {
}
/**
 *  获取数据并绘制界面
 */
- (void)fetchContentData {
    [self renderContentViews];
}
/**
 *  绘制界面
 */
- (void)renderContentViews {
}
/**
 *  设置顶部导航栏拓展布局为空
 */
- (void)setExtentdedLayoutEdgeZero {
    if ([self respondsToSelector:@selector(edgesForExtendedLayout)]) {
        self.edgesForExtendedLayout = UIRectEdgeNone;
    }
}

#pragma mark - Event Response 事件响应
#pragma mark - Delegate Realization 委托方法
#pragma mark - Custom Method    自定义方法
#pragma mark └ Other
#pragma mark - Custom Accessors 自定义属性
```

#### Standardize Structure Of Code (View)

| Title | Standardize Structure Of Code (View) |
| --- | --- |
| Summary | View 代码结构 |
| Completion Shortcut | Structure View |

```
#pragma mark - + 静态方法
+ (instancetype)view {
    id view = [[NSBundle mainBundle] loadNibNamed:NSStringFromClass(self) owner:nil options:nil].firstObject;
    return view;
}
#pragma mark - Overridden Methods
#pragma mark └ Dealloc
- (void)dealloc { }
#pragma mark └ LifeCycle 生命周期
- (instancetype)initWithFrame:(CGRect)frame {
    if (self = [super initWithFrame:frame]) {
        [self commonInit];
    }
    return self;
}

- (void)awakeFromNib {
    [super awakeFromNib];
    [self commonInit];
}

- (void)commonInit {
    
}
#pragma mark - Private Method    自定义方法
#pragma mark - Event Response 事件响应
#pragma mark - Delegate Realization 委托实现
#pragma mark - Helper Method 帮助方法
#pragma mark - Custom Accessors 自定义属性
```

#### Standardize Structure Of Code (Object)

| Title | Standardize Structure Of Code (Object) |
| --- | --- |
| Summary | Object 代码结构 |
| Completion Shortcut | Structure Object |


```
#pragma mark - LifeCycle 生命周期
#pragma mark └ Dealloc
- (void)dealloc {
}
#pragma mark └ Init
- (instancetype)init {
    if(self = [super init]) {
        
    }
    return self;
}

#pragma mark - Event Response 事件响应
#pragma mark - Delegate Realization 委托方法
#pragma mark - Custom Method    自定义方法
#pragma mark └ Other
#pragma mark - Custom Accessors 自定义属性
```


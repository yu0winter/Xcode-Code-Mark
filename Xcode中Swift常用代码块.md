
```
    // MARK: - LifeCycle 生命周期
    // MARK: └ DeInit
    deinit {
        
    }
    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }
    // MARK: └ Init
    required init?(coder aDecoder: NSCoder) {
        super.init(coder: aDecoder)
        fatalError("init(coder:) has not been implemented")
    }
    
    override init(nibName nibNameOrNil: String?, bundle nibBundleOrNil: Bundle?) {
        super.init(nibName: nibNameOrNil, bundle: nibBundleOrNil)
    }
    
    convenience init() {
        self.init()
        NSLog("是否调用了 convenience init() {")
    }

    // MARK: └ Content View Loading
    override func viewDidLoad() {
        super.viewDidLoad()
        self.setupContentViews();
        self.fetchContentData();
        self.setExtentdedLayoutEdgeZero();
    }

    /**
     *  初始化界面并设置布局
     */
    func setupContentViews () {
        self.layoutPageSubViews()
    }
    /**
     *  设置布局
     */
    func layoutPageSubViews () {
    }
    /**
     *  获取数据并绘制界面
     */
    func fetchContentData () {
        self.renderContentViews()
    }
    /**
     *  绘制界面
     */
    func renderContentViews () {
    }
    /**
     *  设置顶部导航栏拓展布局为空
     */
    func setExtentdedLayoutEdgeZero () {
        self.edgesForExtendedLayout = UIRectEdge.init(rawValue: 0)
    }
    
    // MARK: - Event Response 事件响应
    // MARK: - Delegate Realization 委托方法
    // MARK: - Custom Method    自定义方法
    // MARK: └ Other
    // MARK: - Custom Accessors 自定义属性
```
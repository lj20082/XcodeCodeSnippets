### XcodeCodeSnippets

本工程主要收集xcode平时常用的一些代码片段，使用时有2种方式：

1. 通过运行脚本下载snippets，脚本将自动拷贝到对应文件夹。
2. 手动下载snippets并拷贝到对应文件夹，通常路径再Library/Developer/Xcode/UserData/CodeSnippets。
3. 脚本安装方式如下：

```
git clone https://github.com/lj20082/XcodeCodeSnippets.git
cd XcodeCodeSnippets
sh setup_snippets.sh

```

4. 目前整理的snippets说明:

- 内存管理相关

*快捷键：sss*

```
@property (nonatomic, strong) <#dataTpye#> *<#name#>;

```

*快捷键：aaa*

```
@property (nonatomic, assign) <#DataType#> <#name#>;

```
*快捷键：ccc*

```
@property (nonatomic, copy) <#DataType#> *<#name#>;

```
*快捷键：@www*

```
@weakify(self);

```

- 控件相关

*快捷键：@label*

```
UILabel *label = [[UILabel alloc] init];
label.font = [UIFont <#font#>];
label.text = <#text#>
label.textColor = [UIColor <#textColor#>];
label.textAlignment = NSTextAlignmentCenter;
label.backgroundColor = [UIColor clearColor];
[<#view#> addSubview:label];

```
*快捷键：@button*

```
UIButton *button = [UIButton buttonWithType:<#(UIButtonType)#>];
button.backgroundColor = [UIColor <#backgroundColor#>];
button.titleLabel.font = [UIFont <#font#>];
[button setTitle:<#title#> forState:UIControlStateNormal];
[button setTitleColor:[UIColor <#titleColor#>] forState:UIControlStateNormal];
[button setImage:<#(nullable UIImage *)#> forState:<#(UIControlState)#>];
[button setBackgroundImage:<#(nullable UIImage *)#> forState:<#(UIControlState)#>];
[button addTarget:self action:@selector(<#buttonClicked:#>) forControlEvents:UIControlEventTouchUpInside];
[<#view#> addSubview:button];

```

*快捷键：@table*

```

UITableView *tableView = [[UITableView alloc] initWithFrame:CGRectZero style:UITableViewStylePlain];
[tableView registerClass:[<#classCell#> class] forCellReuseIdentifier:<#kReuseIdentifier#>];
tableView.separatorStyle = UITableViewCellSeparatorStyleNone;
tableView.dataSource = self;
tableView.delegate = self;
tableView.backgroundColor=[UIColor <#clearColor#>];
[<#view#> addSubview:tableView];

```

- 单例创建

*快捷键：@sharedInstance*

```
+ (instancetype)sharedInstance
{
    static id _sharedInstance = nil;
    static dispatch_once_t onceToken;
    dispatch_once(&onceToken, ^{
        _sharedInstance = [[self alloc] init];
    });
    return _sharedInstance;
}
```

- 常量声明


*快捷键：@staticNSString*

` static NSString* const <#name#> = <#value#>;`

*快捷键：@staticInteger*

`static const NSInteger <#name#> = <#value#>; `

- DataSource & Delegate

*快捷键：@tableDelegate* 等，具体可以在Xcode snippets里面看到具体内容。上面只是提供一个思路，可自行按需添加。

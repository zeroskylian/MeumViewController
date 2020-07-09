
只需定义一个枚举,即可显示popview 
```
enum MenuItem :String,CaseIterable{
        case update = "update"
        case insert = "insert"
        case delete = "delete"
}

@objc func buttonClick(sender:UIButton) {
        let menu = MeumViewController<MenuItem> ()
        menu.action = { (item) in
            print(item.rawValue)
        }
        menu.show(sourceVc: self,barButtonItem: navigationItem.leftBarButtonItem)
}
```

![SimulatorScreenShot-iPhoneSE(2ndgeneration)-2020-07-09at14.50.24](https://raw.githubusercontent.com/zeroskylian/Images/master/uPic/Simulator%20Screen%20Shot%20-%20iPhone%20SE%20%282nd%20generation%29%20-%202020-07-09%20at%2014.50.24.png)

# StudyCoreData
iOS/CoreDataの勉強用repository

# repositoryに含むこと
* CoreDataに関係するファイル
* どのようにデータを保存するか
* どのようにデータを取り出すか
* データのマイグレーションはどのようにできるか

# Swift UI AppでのCore Data
Xcode12からSwift UI App([[Xcode 12] アプリの起動について変更になった部分まとめ | Developers.IO](https://dev.classmethod.jp/articles/xcode12_change_appdelegate/))が選べるようになり、Swift UI AppではAppDelegateやSceneDelegateが生成されない。

この時`@main`([swift-evolution/0281-main-attribute.md at master · apple/swift-evolution](https://github.com/apple/swift-evolution/blob/master/proposals/0281-main-attribute.md))がエントリーポイントとなる。

この時、従来のようにAppやSceneでのイベントにて処理を行う場合は、[Using Core Data with SwiftUI App P… | Apple Developer Forums](https://developer.apple.com/forums/thread/650876)のように、`@Environment(\.scenePhase)`を利用する。

# 参考
* [Core Data with SwiftUI Tutorial: Getting Started | raywenderlich.com](https://www.raywenderlich.com/9335365-core-data-with-swiftui-tutorial-getting-started)

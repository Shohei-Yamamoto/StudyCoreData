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

# Tips
## Cannnot find -- Core Dataのentityがクラスとして認識されない場合は？
`Cannnot find 'Entity' in scope`のようになってしまう場合。
クリーンしてXcodeを再度起動しなおせば良い。

* [ios - SwiftUI 2.0 CoreData issues with new project - 'Cannot find type 'Item' in scope' - Stack Overflow](https://stackoverflow.com/questions/63603754/swiftui-2-0-coredata-issues-with-new-project-cannot-find-type-item-in-scope)

## CoreDataのデータの初期化
* どうやら事前にデータを入れておいてそれをコピーしたモデルを利用することで可能らしい。([ios — コアデータを事前入力する方法はありますか？](https://www.it-swarm-ja.tech/ja/ios/%E3%82%B3%E3%82%A2%E3%83%87%E3%83%BC%E3%82%BF%E3%82%92%E4%BA%8B%E5%89%8D%E5%85%A5%E5%8A%9B%E3%81%99%E3%82%8B%E6%96%B9%E6%B3%95%E3%81%AF%E3%81%82%E3%82%8A%E3%81%BE%E3%81%99%E3%81%8B%EF%BC%9F/968387802/))
* こちらの記事にAppDelegateでのやり方も書いており、少数であればこちらで問題なさそう -> 難しい
* ListのonAppearでifチェックして挿入のやり方が簡単 -> [Initialize Core Data Objects Swift… | Apple Developer Forums](https://developer.apple.com/forums/thread/132746)



# 参考
* [Core Data with SwiftUI Tutorial: Getting Started | raywenderlich.com](https://www.raywenderlich.com/9335365-core-data-with-swiftui-tutorial-getting-started)
* [(116) Core Data Tutorial - Lesson 5: Entities and Relationships - YouTube](https://www.youtube.com/watch?v=hEz1cUZdsCE)

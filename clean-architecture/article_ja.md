---
title: "クリーンアーキテクチャってつまりこういうこと?"
canonical: https://GoodRelax.github.io/articles/clean-architecture/article_ja.html
tags: clean-architecture, dip, design
lang: ja
---
# クリーンアーキテクチャーってつまりこういうこと？

よくある間違いに**手段**と**目的**の混同ってのがある。

ソフトウェアの世界で言うと、どこかの会社のフレームワークを使うことが目的のシステムを作ってしまったケース。
これをやってしまうとフレームワーク提供会社に自社のビジネスを支配されてしまう。

正しくは自社内にインターフェースを設けて、そのインターフェース経由でフレームワークを使う。
こうしておけば、フレームワークが気に入らなくなったら他のに乗り換えれば良い。

この自分でインターフェースを定義することで依存関係を逆転する技が
- DIP (Dependency Inversion Principle)

ってやつ。

ボブおじさん先生は

- Entity (Enterprise Business Rules)
- Use Case (Application Business Rules)
- Interface Adapters
- Frameworks

の4階層で説明されてるけど、つまるところ

- 目的: 原理原則 (Entity) に従ってお仕事 (Use Case) しましょう
- 手段: そのために線引き (Adapter) して道具 (Framework) を上手く使いましょう

ってことかな。
 
クラス図で書くと次の通り。

## Class Diagram of Dirty Architecture (before CA)

依存の向きが内→外ではなく、外→内になっている状態が汚い

![ダーティーアーキテクチャ クラス図](./class_diagram_dirty_arch.svg)
<!--
```plantuml
@startuml

skinparam rectangleBorderThickness 3
skinparam rectangleFontColor black
skinparam defaultTextAlignment center

rectangle "Frameworks" #4A7EBB {
    rectangle "UI, DB, Web, Devices, External Interfaces" as FW_content #F2F2F2
    
    rectangle "Interface Adapters" #7EAC54 {
        rectangle "Controllers, Presenters, Gateways" as IA_content #F2F2F2
        
        rectangle "Use Cases" #FBC02D {
            rectangle "Application Business Rules" as UC_content #F2F2F2
			
            rectangle "Entities" #E67E48 {
                rectangle "Enterprise Business Rules" as EN_content #F2F2F2
            }
        }
    }
}


IA_content -d-> FW_content : "depends on"
UC_content -d-> IA_content : "depends on"
EN_content -d-> UC_content : "depends on"

@enduml
```
-->


## Class Diagram of Clean Architecture (after CA)

内側の Use Case や Interface Adapter は 自分たちの都合で定義した interface を経由して外側の道具を使うのがポイント

![クリーンアーキテクチャ クラス図](./class_diagram_clean_arch.svg)
<!--
```plantuml
@startuml

skinparam rectangleBorderThickness 3
skinparam rectangleFontColor black
skinparam defaultTextAlignment center

rectangle "Frameworks" #4A7EBB {
    rectangle "UI, DB, Web, Devices, External Interfaces" as FW_content #F2F2F2
    
    rectangle "Interface Adapters" #7EAC54 {
        rectangle "Controllers, Presenters, Gateways" as IA_content #F2F2F2
        rectangle "<<interface>> \n IA" as IA_if #D1C4E9
        
        rectangle "Use Cases" #FBC02D {
            rectangle "Application Business Rules" as UC_content #F2F2F2
            rectangle "<<interface>> \n UC" as UC_if #D1C4E9
            
            rectangle "Entities" #E67E48 {
                rectangle "Enterprise Business Rules" as EN_content #F2F2F2
            }
        }
    }
}

FW_content .u.|> IA_if : "implements"
IA_content -d-> IA_if : "depends on"
IA_content .u.|> UC_if : "implements"
UC_content -d-> UC_if : "depends on"
UC_content .u.> EN_content : "depends on"

@enduml
```
-->

## ただの感想

DIP (Dependency Inversion Principle)ってずるいよね？
Interface ってのは契約書みたいなもんだけど、中世の世界観で言うと...

 - 王様が契約書に従って領民を使っているが
 - 契約書は公証人役場で公平に管理せずに王様が持っているから
 - 領民は契約書に基づいて働いているつもりだけど
 - 結局は王様の言いなりにされてしまう
 
ってことだよね？ 考えた人は天才だわ。

**参考資料**:
- Robert C. Martin "Clean Architecture" (2017)
- https://blog.cleancoder.com/ーncle-bob/2012/08/13/the-clean-architecture.html


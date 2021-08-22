# CustomFont_Space_Resourcepack

カスタムフォントでよく位置調整に使うので配布することにしました

## 例
/tellraw @a ["",{"translate":"yrf_system:space_250","font":"yrf_system/space"},"a"]

## 使い方
リソースパックを入れるだけで使えます。

"translate":"yrf_system:space_<-512~512までの任意の整数[^1]>"。

[^1]: ここでスペースの幅を決めます。負の値に設定すると、下の画像の様に文字同士を重ねて表示することもできます

![2021-02-16_02 02 23](https://user-images.githubusercontent.com/74122979/107977938-4b8ff000-6fff-11eb-8288-d6115c16e099.png)

~~"font"で指定しているフォントは競合対策です。基本的にはフォントを指定することを推奨しますが、指定しなくても使えます。どうしても指定できない場合でなければ、指定しておく方が良いと思います。~~

~~また、assets\minecraft\font\default.jsonを消して置くと競合のリスクが更に下がるので、必ずフォント指定するよ！という方は消してもらって大丈夫です。~~

バニラのアイテムの表示がずれてしまっていたので、一度default.jsonを消しました。

## 注意
/tellraw @a [{"translate":"yrf_system:space_25","font":"yrf_system/space"},"a",{"translate":"yrf_system:space_25","font":"yrf_system/space"},"a"] のように書いてしまうと、フォントの初期値が"yrf_system/space"になってしまい、その後の"a"等にフォントが対応していないため、下の画像の様に四角く文字化けのようになってしまいます。

![2021-02-16_02 28 50](https://user-images.githubusercontent.com/74122979/107977706-e3d9a500-6ffe-11eb-88ab-412ee7b7af3e.png)

それを防ぐためにも、/tellrawや/titleを使う時は["",{"translate":"yrf_system:space_250","font":"yrf_system/space"},"a"]のように、最初に""を挟んでおくと良いと思います。

## 最後に
作品に組み込んだりすることは自由です。 何か不具合があれば報告していただけるとありがたいです

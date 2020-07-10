# UniNaturalComparer

自然順で文字列をソートできる機能

## 使用例

```cs
using Kogane;
using System.Linq;
using UnityEngine;

public class Example : MonoBehaviour
{
    private void Awake()
    {
        var list = new[]
        {
            "icon12.png",
            "icon11.png",
            "icon2.png",
            "icon1.png",
        };

        // icon1.png
        // icon11.png
        // icon12.png
        // icon2.png
        foreach ( var str in list.OrderBy( x => x ) )
        {
            Debug.Log( str );
        }
        
        // icon1.png
        // icon2.png
        // icon11.png
        // icon12.png
        foreach ( var str in list.OrderBy( x => x, new NaturalComparer() ) )
        {
            Debug.Log( str );
        }
    }
}
```

## 謝辞

* このリポジトリは下記のサイト様で公開されているスクリプトを  
Unity Package Manager で使用できるようにしたものになります  
    * https://qiita.com/tomochan154/items/1a3048f2cd9755233b4f
    * https://github.com/tomochan154/toy-box/blob/master/NaturalComparer.cs
* 改変箇所は名前空間のみとなります  

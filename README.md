[![license](https://img.shields.io/github/license/tomori-hikage/state-machine.svg?style=flat-square)](https://github.com/tomori-hikage/state-machine/blob/master/LICENSE)
[![release](https://img.shields.io/github/release/tomori-hikage/state-machine.svg?style=flat-square)](https://github.com/tomori-hikage/state-machine/releases)
[![GitHub](https://img.shields.io/github/followers/tomori-hikage.svg?label=@tomori-hikage&style=social)](https://github.com/tomori-hikage)
[![Twitter](https://img.shields.io/twitter/follow/tomori_hikage.svg?label=@tomori_hikage&style=social)](https://twitter.com/tomori_hikage)

# state-machine

## Description

state-machineはUniRxをベースにしたステートマシンです

## Install

### UnityPackage

[releases](https://github.com/tomoriaki/state-machine/releases) からstate-machine.unitypackageをダウンロードしてプロジェクトにインポートしてください

### UPM Package

<details>
<summary>GitHubから追加</summary>

Unity2019.4以上はGitHubから直接追加できます。この方法はPackage Managerから更新を受け取れないので手動で更新します。

- Package Managerを開きます
- <kbd>+</kbd>をクリックします
- <kbd>Add from Git URL</kbd>を選択します
- `https://github.com/neuecc/UniRx.git?path=Assets/Plugins/UniRx/Scripts` を貼り付けます
- <kbd>Add</kbd>をクリックします
- `https://github.com/tomori-hikage/state-machine.git?path=state-machine/Assets/StateMachine` を貼り付けます
- <kbd>Add</kbd>をクリックします
</details>

## Example

```csharp
using UnityEngine;
using UniRx;
using HC.AI;


[DisallowMultipleComponent]
public class Example : State
{
    #region event

    private void Start()
    {
        BeginStream.Subscribe(_ => Debug.Log("State Begin"));
        UpdateStream.Subscribe(_ => Debug.Log("State Update"));
        FixedUpdateStream.Subscribe(_ => Debug.Log("State FixedUpdate"));
        LateUpdateStream.Subscribe(_ => Debug.Log("State LateUpdate"));
        EndStream.Subscribe(_ => Debug.Log("State End"));
        OnDrawGizmosStream.Subscribe(_ => Debug.Log("State OnDrawGizmos"));
        OnGUIStream.Subscribe(_ => Debug.Log("State OnGUI"));
    }

    #endregion
}
```

## Author

- JINZO  
GitHub: [@JINZO631](https://github.com/JINZO631)  
Twitter: [@jinzo_631](https://twitter.com/jinzo_631)

- takaaptech  
GitHub: [@takaaptech](https://github.com/takaaptech)

- chorome  
GitHub: [@chromee](https://github.com/chromee)  

## Use License

state-machineはUniRxをベースに作成しています

[Copyright (c) 2014 Yoshifumi Kawai](https://github.com/neuecc/UniRx/blob/master/LICENSE)


[© Unity Technologies Japan/UCL](http://unity-chan.com/contents/license_jp/)

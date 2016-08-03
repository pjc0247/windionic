example
====
`.Net` 어셈블리 빌드 -> 빌드 스크립트 -> 어셈블리로부터 `bridge.d.ts` 파일 생성 -> pppppppppppppaaaaaaaacckkk<br><br>
![ex](example.gif)<br><Br>
```cs
[Export]
public class DeviceInfo
{
    public static string osVersion()
     => Environment.OSVersion.ToString();
    public static string machineName()
     => Environment.MachineName;
    public static string userName()
      => Environment.UserName;
    public static int processorCount()
      => Environment.ProcessorCount;
}

[Export]
public class Mathf
{
    public static float sum(float a, float b) 
      => a + b;
}
```
```html
<ion-content padding class="about">
  <b>System Info</b><br>
  UserName : {{ userName }} <br>
  Cores : {{ processorCount }} <br>
  OS : {{ osVersion }} <br>
</ion-content>
```
```typescript
constructor(private navCtrl: NavController) {
  this.userName = DeviceInfo.userName();
  this.processorCount = DeviceInfo.processorCount().toString();
  this.osVersion = DeviceInfo.osVersion();
}
```

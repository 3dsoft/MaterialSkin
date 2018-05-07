MaterialSkin for .NET WinForms
=====================

<a href="https://www.youtube.com/watch?v=A8osVM_SXlg" target="_blank">![alt tag](http://i.imgur.com/JAttoOo.png)</a>

---

#### 현재까지 구현된 MaterialSkin components 목록

Component | Supported | Dark & light version | Disabled mode | Animated
--- | --- | --- | --- | ---
Checkbox | Yes | Yes | Yes | Yes 
Divider | Yes | Yes | N/A | N/A 
Flat Button | Yes | Yes | Yes | Yes 
Label | Yes | Yes | N/A | N/A
Radio Button | Yes | Yes | Yes | Yes
Raised Button | Yes | Yes | Yes | Yes 
Single-line text field | Yes | Yes | No | Yes
TabControl | Yes | N/A | N/A | Yes
ContextMenuStrip | Yes | Yes | Yes | Yes
ListView | Yes | Yes | No | No
ProgressBar | Yes | Yes | No | No 
FloatingActionButton | No | No | No | No
Dialogs | No | No | No | No
Switch | No | No | No | No
More... | No | No | No | No

---

#### MaterialSkin 설치 방법


**1. .Net 버전 설정

MaterialSkin은 .Net 4.5부터 설치 가능하니, 본인의 프로젝트 닷넷버전을 확인할것


**2. Nuget에서 MaterialSkin 설치**

Nuget에서 MaterialSkin을 검색하여  설치한다. 


**3. [도구상자]에 MaterialSkin의 콤포넌트 설치하기**

위의 2번에서 MaterialSkin을 설치하고난  뒤에 그냥 빌드를 하면 /Bin/Debug 폴더에 MaterialSkin.dll이 만들어진다. 

[도구상자]를 열어놓은 상태에서 MaterialSkin.dll을 [도구상자]에 끌어다 놓으면 콤포넌트가 자동으로 추가된다. 

가급적 [도구상자]에 MaterialSkin 관련 탭을 만든뒤에 추가하는걸 권장한다. 


**4. 메인 폼에 MaterialForm 설정**

Form에 MaterialForm을 적용시키려고 한다면, 아래처럼 Form1을 MaterialForm으로부터 상속받도록 설정하면 된다. 

(폼에 MaterialForm을 적용하지 않고 콤포넌트만 사용해도 무방하다)
  
  C# (Form1.cs)
  ```cs
  public partial class Form1 : MaterialForm
  ```
  
  VB.NET (Form1.Designer.vb)
  ```vb
  Partial Class Form1
    Inherits MaterialSkin.Controls.MaterialForm
  ```


**5. 컬러스키마 초기화하기**

위 4번에서 MaterialForm을 적용했을경우,  컬러 테마를 추가로 설정할 수 있다. 

(아래 코드에서 Theme 설정부분까지만 설정해도 충분함)

C# (Form1.cs)
  ```cs
  public Form1()
  {
      InitializeComponent();

      var materialSkinManager = MaterialSkinManager.Instance;
      materialSkinManager.AddFormToManage(this);
      materialSkinManager.Theme = MaterialSkinManager.Themes.LIGHT;
      materialSkinManager.ColorScheme = new ColorScheme(Primary.BlueGrey800, Primary.BlueGrey900, Primary.BlueGrey500, Accent.LightBlue200, TextShade.WHITE);
  }
  ```

VB.NET (Form1.vb)
```vb
Imports MaterialSkin

Public Class Form1

    Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
        Dim SkinManager As MaterialSkinManager = MaterialSkinManager.Instance
        SkinManager.AddFormToManage(Me)
        SkinManager.Theme = MaterialSkinManager.Themes.LIGHT
        SkinManager.ColorScheme = New ColorScheme(Primary.BlueGrey800, Primary.BlueGrey900, Primary.BlueGrey500, Accent.LightBlue200, TextShade.WHITE)
    End Sub
End Class
```

---


#### Material Design in WPF

If you love .NET and Material Design, you should definitely check out [Material Design Xaml Toolkit](https://github.com/ButchersBoy/MaterialDesignInXamlToolkit) by ButchersBoy. It's a similar project but for WPF instead of WinForms.

---



#### State of the project

This project is no longer under active development. Though, contributions are still welcome and the community will likely still help if you open an issue.

---


#### Contact

If you wish to contact me for anything you can get in touch at:

- Twitter: https://twitter.com/Ignace_Maes
- Personal Website: http://ignacemaes.com

---


#### Images

![alt tag](http://i.imgur.com/Ub0N9Xf.png)

*A simple demo interface with MaterialSkin components.*

![alt tag](http://i.imgur.com/eIAtRkc.png)

*The MaterialSkin checkboxes.*

![alt tag](http://i.imgur.com/sAPyvdH.png)

*The MaterialSkin radiobuttons.*

![alt tag](http://i.imgur.com/3Zpuv6x.png)

*The MaterialSkin ListView.*

![alt tag](http://i.imgur.com/07MrJZQ.png)

*MaterialSkin using a custom color scheme.*

## 创建项目

``` csharp
//安装prism模板
dotnet new --install Prism.Templates
//创建项目模板
dotnet new wpf-core-full -n projectname
//创建模块模板
dotnet new wpf-module-core -n XXXXModule

```

## 模板

|模板名                          | 短名称          | 语言  |标记|
|------------------------------- | --------------- | ----  |------------------------------------------------------------|
|Prism .NET MAUI App             | prism-maui      | [C#]  |MAUI/Android/iOS/macOS/Mac Catalyst/Windows/Tizen|
|Prism Blank App (Uno Platform)  | uno-blank       | [C#]  |Prism/Xamarin/Uno Platform/WebAssembly/iOS/Android/WinUI/UWP|
|Prism Blank App (WPF)           | wpf-core-blank  | [C#]  |Desktop|
|Prism Blank App (Xamarin.Forms) | xf-blank        | [C#]  |Prism/Xamarin/Xamarin.Forms|
|Prism Full App (WPF)            | wpf-core-full   | [C#]  |Desktop|
|Prism Module (WPF)              | wpf-module-core | [C#]  |Desktop|
|Prism Module (Xamarin)          | xf-module       | [C#]  |Prism/Xamarin/Xamarin.Forms|

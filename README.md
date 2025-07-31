# mynotes
Note some?

## Command lines

> dotnet nuget add source "-" --name gitlab --username name --password pwd

>dotnet nuget push "*.nupkg" --source gitlab

>dotnet publish xxx -p:Version=2.0.2.0 -o:output --runtime win-x64 --framework net6.0-windows -c Release --self-contained false

>iscc /DCurrentAppVersion=1.1.0.0 xxx.iss /Q

>if defined XXX set XXX=AAA

## Build About

### import `Directory.Build.props`

> `<Import Project="$([MSBuild]::GetPathOfFileAbove('Directory.Build.props', '$(MSBuildThisFileDirectory)../'))" />`


### Copy dependencies

> [CopyLocalLockFileAssemblies](https://learn.microsoft.com/en-us/dotnet/core/project-sdk/msbuild-props#copylocallockfileassemblies) to set library project build with dependencies.

### Run target once when multitargeting

> [learn](https://learn.microsoft.com/en-us/visualstudio/msbuild/run-target-exactly-once?view=vs-2022)


## Git Commands

### Undo things

>[git reset --mixed HEAD^ ](https://git-scm.com/docs/git-reset)

>[Others](https://git-scm.com/book/en/v2/Git-Basics-Undoing-Things)


## TeamCity 

> ``` Delete all files in the checkout directory before the build``` if selected, the custom build can not select brunch.


## Articles

> [tateful-or-stateless-classes](https://dzone.com/articles/stateful-or-stateless-classes)


## Books

>[Hello world! ](https://refactoring.guru/)

>[Git basic](https://git-scm.com/book/en/v2)

>[fluent2](https://fluent2.microsoft.design/)

>[martinfowler](https://martinfowler.com/)


## Some Configs

### Use UseArtifacts

``` code csharp
    <PropertyGroup>
        <UseArtifactsOutput>true</UseArtifactsOutput>
        <AppendTargetFrameworkToOutputPath>false</AppendTargetFrameworkToOutputPath>
        <ArtifactsPath>$(MSBuildThisFileDirectory)Build</ArtifactsPath>
    </PropertyGroup>

```

### Clear _wpftmp folder when use UseArtifacts ([usefull](https://github.com/dotnet/wpf/issues/4299) [usefull](https://github.com/dotnet/wpf/issues/2930) )

``` coed chsarp
    <Target Name="RemoveWpfTemporaryFolder" AfterTargets="_CompileTemporaryAssembly" Condition="Exists('$(OutDir)') And '$(UseArtifactsOutput)'=='True' And $(MSBuildProjectName.EndsWith('_wpftmp'))">
        <RemoveDir Directories="$(BaseOutputPath)">
        </RemoveDir>
    </Target>
```

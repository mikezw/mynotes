# mynotes
Note some?

## Command lines

> dotnet nuget add source "-" --name gitlab --username name --password pwd

>dotnet nuget push "*.nupkg" --source gitlab

>dotnet publish xxx -p:Version=2.0.2.0 -o:output --runtime win-x64 --framework net6.0-windows -c Release --self-contained false

>iscc /DCurrentAppVersion=1.1.0.0 xxx.iss /Q


## Build About

### import `Directory.Build.props`

> `<Import Project="$([MSBuild]::GetPathOfFileAbove('Directory.Build.props', '$(MSBuildThisFileDirectory)../'))" />`


### Copy dependencies

> [CopyLocalLockFileAssemblies](https://learn.microsoft.com/en-us/dotnet/core/project-sdk/msbuild-props#copylocallockfileassemblies) to set library project build with dependencies.


## Git Commands

### Undo things

>[git reset --mixed HEAD^ ](https://git-scm.com/docs/git-reset)

>[Others](https://git-scm.com/book/en/v2/Git-Basics-Undoing-Things)

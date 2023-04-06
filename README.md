# mynotes
Note some?

## Command lines

> dotnet nuget add source "-" --name gitlab --username name --password pwd

>dotnet nuget push "*.nupkg" --source gitlab

>dotnet publish xxx -p:Version=2.0.2.0 -o:output --runtime win-x64 --framework net6.0-windows -c Release --self-contained false

>iscc /DCurrentAppVersion=1.1.0.0 xxx.iss /Q

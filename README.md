# TestMSBuild
Test repo for MS demonstrating issues with MS Build not respecting Configuration when publishing File Systems

MSBuild Version: 15.7.179.6572

Visual Studio Version: 15.7.3

Powershell command: "C:\Program Files (x86)\Microsoft Visual Studio\2017\BuildTools\MSBuild\15.0\Bin\msbuild.exe" `
"TestMSBuild.Web.csproj" `
/p:DeployOnBuild=true `
/p:PublishProfile="Release Deploy"

Expected to see Web config transofrmed to Release web config but does not happen. I also see this in output - "Auto ConnectionString Transformed obj\Debug\Package\PackageTmp\Web.config into obj\Debug\CSAutoParameterize\transformed\Web.config." which says to me Debug build is being used and not Release as specified in "Release Deploy" publish profile.

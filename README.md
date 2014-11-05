Unity3D.Sample
==============

Minimal project for developing with Unity3D in Visual Studio 2013. Target framework of the project is 

'Unity 3.5 .NET full Base Class Libraries' (a subset of Microsoft.NET 3.5)

First install Visual Studio 2013 tools for Unity 4.5

[https://visualstudiogallery.msdn.microsoft.com/20b80b8c-659b-45ef-96c1-437828fe7cf2](https://visualstudiogallery.msdn.microsoft.com/20b80b8c-659b-45ef-96c1-437828fe7cf2)

To get it working:

. Clone repository

. Open UnitySources\UnityVS.UnityProject.sln in Visual Studio

. Rebuild. 
On build the following Post-Build command is executed to create a mono debug file (mdb):
"$(SolutionDir)\tools\pdb2mdb.exe" "$(TargetPath)"

If all goes well, in the directory UnityProject\Assets\Plugins 6 Unity3DPlugin files are created.

. Start UnityProject\Assets\main.unity in Unity

. Click 'Main Camera' (upper left), click button right to 'Script: Missing (Mono script)' doubleclick 'SampleBehaviour' 

. Press Run in Unity.
The camera background should turn black (see code in SampleBehaviour).

For debugging:

. Stop Unity with running

. Set a breakpoint in Samplebehaviour method Start()

. In Visual Studio click Debug ->   Attach Unity debugger and select the Unity instance

. Press start in Unity

Visual Studio should now hit the breakpoint in SampleBehaviour.

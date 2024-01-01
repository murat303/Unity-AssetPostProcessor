# Unity-AssetPostProcessor

Unity's [AssetPostprocessor](https://docs.unity3d.com/ScriptReference/AssetPostprocessor.html) lets you hook into the import pipeline and run scripts prior or after importing assets. 

In a production pipeline AssetPostprocessors should always be placed in pre-built dll's in the project instead of in scripts. AssetPostprocessors change the output of imported assets, thus a compile error in one of the scripts will lead to assets being imported differently. This can be a severe issue when working in a production pipeline. By using dll's for AssetPostprocessors you ensure that they can always be executed even if the scripts have compile errors. 

Unity guide on creating dll's: https://docs.unity3d.com/Manual/UsingDLL.html

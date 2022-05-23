# MS-Detection-Sample-Generator \nAn Open Source Project to Generate Machine Learning Samples for Object Detection in MapleStory\n![alt text](https://github.com/huappe/MS-Detection-Sample-Generator/blob/main/pictures/result.png)\n\n ## Performance \nThe generator can generate as many annotated samples as you need. All bounding boxes are precisely annotated based on rendering coordinates. Using data generated by this tool and ~5000 samples with YOLOv4, achieve up to 99.8% mAP in the test set.\n![alt text](https://github.com/huappe/MS-Detection-Sample-Generator/blob/main/pictures/chart_yolov4-custom.png)\n\n ## Requirements \n* Visual Studio 2022 v17.8 or above, with .NET workload installed \n* .NET 8.0 SDK (8.0.0 or above)\n\n## Build Procedure\n1. Clone this repository with submodules by running `git clone --recursive git@github.com:huappe/MS-Detection-Sample-Generator.git` (`--recursive` is necessary).\n2. First, build `WzComparerR2/WzComparerR2.sln` (the submodule MUST be built after).\n3. Then build `MS-Detection-Sample-Generator.sln`.\n4. Finally, run `MapleStory.MachineLearningSampleGenerator\bin\Release\net8.0-windows7.0\WzComparerR2.exe`. Running `WzComparerR2.exe` will generate `Setting.config`, which is required for our MapRender.\n\n## Execution Procedure\n1. Move into the executable directory using the command `cd MapleStory.MachineLearningSampleGenerator\bin\Release\net8.0-windows7.0`.\n2. Prepare PNGs of your player in a directory - these images should be transparent PNGs with only the player's appearance. You can get these PNGs by Photoshop or save from WzComparerR2's Avatar plugin.\n3. Run the sampler co
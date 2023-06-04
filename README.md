# Modify
Trying to enhance the functionality of the face swapping 'roop' project from @s0md3v via some python magic.

Kindly note, do not misuse this, do not swap faces without their consent, do not do to others what you wouldn't wanna be done to you or your loved ones. 

Features:
- Simple easy to understand UI.
- Process all files within a directory.
- No save dialogue boxes, all processed files are saved in the target files folder by default.
- Output files are renamed as Video_Face.mp4.
- Script checks if the video has already been processed and if the output file with same name exists it skips that file.

You can watch more demos of the roop face swapped videos [here](https://drive.google.com/drive/folders/1KHv8n_rd3Lcr2v7jBq1yPSTWM554Gq8e)

![demo](https://github.com/Aditya-A-Sharma/Modify/assets/110774846/00165ec2-5fb0-4499-83d5-d7938cc4fa82)

Future plans:
- Option to enable or disable gpu acceleration. (Script is slower without gpu but far more likely to run without errors).
- Install button to run anoher script which will install roop from @s0md3v is not found.
- Output directory option, which will overwrite the default of saving the processed file in the target video directory. (If requested by some user)

Simple mode : Just drop the modify.py file in the roop directory and you are good to go.

![Modify - One Click Face Swapper - simple mode](https://github.com/Aditya-A-Sharma/Modify/assets/110774846/22a6013e-916e-4ade-98e2-2f26efc1f2e3)


Advanced mode : If you have multiple versions or forks of roop, you can use this mode to select the venv activation file and the run.py. 

![Modify - One Click Face Swapper - advanced mode](https://github.com/Aditya-A-Sharma/Modify/assets/110774846/23540a05-40c8-432d-9d9c-cd2f3d6f4fd7)


## How do I install it?

**Issues according installation will be closed without ceremony from now on, we cannot handle the amount of requests.**

There are two types of installations: basic and gpu-powered.

- **Basic:** It is more likely to work on your computer but it will also be very slow. You can follow instructions for the basic install [here](https://github.com/s0md3v/roop/wiki/1.-Installation).

- **GPU:** If you have a good GPU and are ready for solving any software issues you may face, you can enable GPU which is wayyy faster. To do this, first follow the basic install instructions given above and then follow GPU-specific instructions [here](https://github.com/s0md3v/roop/wiki/2.-GPU-Acceleration).

## How do I use it?
> Note: When you run this program for the first time, it will download some models ~300MB in size.

Executing `python run.py` command will launch this window:
![gui-demo](gui-demo.png)

Choose a face (image with desired face) and the target image/video (image/video in which you want to replace the face) and click on `Start`. Open file explorer and navigate to the directory you select your output to be in. You will find a directory named `<video_title>` where you can see the frames being swapped in realtime. Once the processing is done, it will create the output file. That's it.

Don't touch the FPS checkbox unless you know what you are doing.

Additional command line arguments are given below:

```
options:
  -h, --help            show this help message and exit
  -f SOURCE_IMG, --face SOURCE_IMG
                        use this face
  -t TARGET_PATH, --target TARGET_PATH
                        replace this face
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        save output to this file
  --gpu                 use gpu
  --keep-fps            maintain original fps
  --keep-frames         keep frames directory
  --max-memory MAX_MEMORY
                        maximum amount of RAM in GB to be used
  --max-cores CORES_COUNT
                        number of cores to be use for CPU mode
  --all-faces           swap all faces in frame
```

Looking for a CLI mode? Using the -f/--face argument will make the program in cli mode.

## Future plans
- [ ] Improve the quality of faces in results
- [ ] Replace a selective face throughout the video
- [ ] Support for replacing multiple faces

## Credits
- [ffmpeg](https://ffmpeg.org/): for making video related operations easy
- [deepinsight](https://github.com/deepinsight): for their [insightface](https://github.com/deepinsight/insightface) project which provided a well-made library and models.
- and all developers behind libraries used in this project.

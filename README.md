![image](https://github.com/Dayer5/MinecraftAIWithNVIDIA/blob/main/Minecraft%20Biome%20Identifier%20with%20NVIDIA.png?raw=true)
# Minecraft Biome Identifier With NVIDIA
A machine learning model that identifies the minecraft biome based on an image. <br/><br/>
Biome Categories include:
- badlands
- basalt_deltas
- crimson_forest
- dark_forest
- desert
- jungle
- nether_wastes
- oak_forest
- ocean
- plains
- savanna
- soul_sand_valley
- taiga
- warped_forest <br/>
### Examples
![image](https://github.com/Dayer5/MinecraftAIWithNVIDIA/blob/main/input1.png?raw=true)
![image](https://github.com/Dayer5/MinecraftAIWithNVIDIA/blob/main/output1.png?raw=true)<br/>
![image](https://github.com/Dayer5/MinecraftAIWithNVIDIA/blob/main/input2.png?raw=true)
![image](https://github.com/Dayer5/MinecraftAIWithNVIDIA/blob/main/output2.png?raw=true)
## Behind The Scenes
The Minecraft Biome Identifier uses the resnet18 image recognition model retrained for the specific purpose of identifying biomes. The data images used to train, test and validate the model comes from two kaggle databases:
>[Minecraft Dimensions Screenshots by PR1M3R](https://www.kaggle.com/datasets/pr1m3r/minecraft-dimensions-screenshots?resource=download) <br/>
>[Minecraft Biomes by WILLOW C](https://www.kaggle.com/datasets/willowc/minecraft-biomes?resource=download)

## Running this project

1. Setup your Jetson Nano and Install VScode
2. Connect Jetson Nano onto your computer hotspot. Write down your Jetson Nano IP address for later use
3. Connect your VScode to your Jetson Nano using Connect Host and `ssh nvidia@IPAddress`
4. Open the NVIDIA home folder
5. Open the terminal and use `cd jetson-inference/python/training/classification` to enter the needed directory
6. Use `NET=models/minecraftV2` and `DATASET=data/minecraftDataV2` to set NET and DATASET for later reference
7. Move the photo of your minecraft biome into the `Ainput` folder
8. Run the model using `imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt Ainput/IMAGE_NAME Aoutput/IMAGE_OUTPUT_NAME` Replace IMAGE_NAME with the name of your image and IMAGE_OUTPUT_NAME with the name of what you want the output image to be.
9. Enjoy running the Minecraft Biome Identifier model!

## Credits
This was made possible with the help and support from **Cipher (Real Name Unknown)** and the rest of the **iDTech Community**. Thank you! :D

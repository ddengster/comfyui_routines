

# Prequisite LoRa models

- Go to civitai.com, search for something like 'game icon' and download a lora model. 

- Copy those models (usually .safetensor files) into your Documents/ComfyUI/models/loras/ folder.

Reference loras:

- https://civitai.com/models/134147/game-icon-institutekuijia

- https://civitai.com/models/68975/game-icon-researchbottlelora

# ComfyUI

- Click **Templates** on the LHS bar.

- Click **Getting Started**

- Click **Image Generation**

- You should see have a workflow of nodes. Install any required model. You may do a test run.

## Loading Lora node 

- First ensure your models are present. On the LHS bar, click **Models**, click the refresh icon, check if the **loras** folder has your downloaded models.

- Right click on an empty space, "Add Node -> loaders -> Load LoRA " OR drag and drop the LoRA from the folder itself.

- Link the `MODEL` of the `Load Checkpoint` output node to the `model` input of your lora model. See 1:45 of the video. Do the same for the other out/inputs.

- Link the `MODEL` of the `Load LoRA` output node to the `model` input of the Text prompt node. Do the same for the other out/inputs.

- Hit Run (top RHS) to generate the image.

![](lora_loading.mp4)

## Tweaking for multiple images

- For when you want the model to produce multiple images at a time.

- Find the `Empty Lantent Image` Node. Change sizes, and `batch_size`.

- Hit Run

![](latent_tweak.PNG)
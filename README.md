# ImageToCaption_Encoder_Decoder



| Image                      | Layer 1                             | Layer 2                             | Layer 3                             |
| -------------------------- | ----------------------------------- | ----------------------------------- | ----------------------------------- |
| ![Image 1](data/boat.png)  | ![Layer 1-1](data/pil_img_754.jpg)  | ![Layer 2-1](data/pil_img_214.jpg)  | ![Layer 3-1](data/pil_img_125.jpg)  |
| ![Image 2](data/bus.png)   | ![Layer 1-2](data/pil_img_859.jpg)   | ![Layer 2-2](data/pil_img_381.jpg)   | ![Layer 3-2](data/)   |
| ![Image 3](data/child.png) | ![Layer 1-3](data/pil_img_328.jpg) | ![Layer 2-3](data/pil_img_242.jpg) | ![Layer 3-3](data/pil_img_854.jpg) |
| ![Image 4](data/dog.png)   | ![Layer 1-4](data/pil_img_204.jpg)   | ![Layer 2-4](data/pil_img_792.jpg)   | ![Layer 3-4](data/pil_img_858.jpg)   |
| ![Image 5](data/horse.png) | ![Layer 1-5](data/pil_img_658.jpg) | ![Layer 2-5](data/pil_img_189.jpg) | ![Layer 3-5](data/pil_img_704.jpg) |


| Image                                       | Reference Caption                           | Model 1                                          | Model 2                                      |
|---------------------------------------------|---------------------------------------------|--------------------------------------------------|----------------------------------------------|
| <img src="data/boat.png" width="100px">     | A small boat in the ocean .                 | a boat is sitting on a boat overlooking water     | a boat is sailing over the water             |
| <img src="data/bus.png" width="100px">      | Bus driving by parked cars .               | a group of people are walking down a street      | a bus is parked on a street                  |
| <img src="data/child.png" width="100px">    | Child holding red frisbee outdoors .        | a little boy in a red shirt is holding a toy frisbee | a young boy with a red frisbee in the grass |
| <img src="data/dog.png" width="100px">      | Dog on a beach by the ocean .               | a dog stands in front of a large body of water   | a brown dog stands on the sand near the ocean |
| <img src="data/horse.png" width="100px">    | A cowboy riding a horse in the desert .     | two people walking on a sandy path               | two people are riding a horse on a mountain |

# Encoder-Decoder Architecture
$$
\boxed{\textbf{ENCODER:}}
\rightarrow
\boxed{\text{Image}}
\rightarrow
\boxed{\text{DINOv2 spatial tokens}}
$$

$$
\textbf{DECODER:}
\boxed{\text{Word embeddings + Positional Encoding}}
\rightarrow
\boxed{\text{Self-Attention}}
\rightarrow
\boxed{\text{Cross-Attention Layers (Image Embeddings)}}
\rightarrow
\boxed{\textbf{Softmax}(\text{Word embeddings})}
$$



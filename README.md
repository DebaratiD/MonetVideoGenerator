## Monet Style Video Generator

For this project I have taken the video input from Youtube [here](https://www.youtube.com/watch?v=yrlWYXEoqkM).
The LangSAM model has been used to segment the boat object from a given videoframe via a prompt. Read more about the LangSAM model [here](https://github.com/luca-medeiros/lang-segment-anything). 
LangSAM makes it easier to extract objects due to its GroundDino model base compared to SAM (Segment-Anything-Model). 

After Segmentation, each mask is passed through the Instruct-Pix2Pix model that converts it into a Monet-style artwork. I have used only 50 epochs due to time constraints, but more epochs could generate a clearer artwork.
I have used the Instruct-Pix2Pix model from [Hugging Face](https://huggingface.co/timbrooks/instruct-pix2pix). Each image took 8 seconds to generate.

After all the processing, I used OpenCV to combine the images back into a video.
![image](https://github.com/DebaratiD/MonetVideoGenerator/assets/37064721/31baf7c0-47bd-4f27-9561-0c4b9f4d0ed9)


https://github.com/DebaratiD/MonetVideoGenerator/assets/37064721/1f32e870-6c26-45c0-867f-69020d985620

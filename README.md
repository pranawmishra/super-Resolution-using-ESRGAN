# Real-ESRGAN Video Super-Resolution and Quality Evaluation

This repository demonstrates the usage of Real-ESRGAN for video super-resolution in Google Colab and provides a script to calculate quality metrics (PSNR and SSIM) for the generated videos.  

### check Super resolution.ipynb for complete code

## Getting Started
### Clone Real-ESRGAN Repository
Clone the Real-ESRGAN repository and set up the environment:

!git clone https://github.com/xinntao/Real-ESRGAN.git


### Upload Videos
Create the necessary folders and upload the videos to the 'upload' folder

### Video Super-Resolution
Perform video super-resolution using Real-ESRGAN  

We need to run the below command for each of the videos to generate its corresponding high-resolution video:  

! python inference_realesrgan_video.py -i upload/30_sec_videos..mp4 -n realesr-animevideov3 -s 2 --suffix outx2

### Arguments  
 -i, --input: input video  
 -n, --model_name: Used model name  
 -s, --outscale: Scale  
 -suffix: Suffix of the output video  

### Quality Metrics Calculation
Calculate PSNR and SSIM for the generated videos

### Test Video 1 (test1.mp4)
Average PSNR (Peak Signal-to-Noise Ratio): 16.82 dB  
Average SSIM (Structural Similarity Index): 0.81  
The PSNR value of 16.82 dB suggests that there may be a noticeable loss in quality compared to the original video. However, the relatively high SSIM value of 0.81 indicates a considerable structural similarity between the original and generated videos.

### Test Video 2 (test2.mp4)
Average PSNR (Peak Signal-to-Noise Ratio): 32.82 dB  
Average SSIM (Structural Similarity Index): 0.98  
The high PSNR value of 32.82 dB suggests a high quality of reconstruction, indicating a close match between the generated and original videos. The SSIM value of 0.98 further reinforces the high structural similarity observed in this case.

### Test Video 3 (test3.mp4)
Average PSNR (Peak Signal-to-Noise Ratio): 30.29 dB  
Average SSIM (Structural Similarity Index): 0.93  
The PSNR value of 30.29 dB suggests a good quality of reconstruction, while the SSIM value of 0.93 indicates a high structural similarity between the original and generated videos.

### Interpretation
PSNR Interpretation:  

PSNR values are expressed in decibels (dB), and higher values are generally considered better. A common range for good quality might be between 20 and 30 dB.  

SSIM Interpretation:  

SSIM values range from -1 to 1, where 1 indicates perfect similarity. Values closer to 1 imply a high level of structural similarity.  
In summary, while the PSNR values provide insights into the quality of reconstruction, the SSIM values emphasize the structural similarity between the original and generated videos. Visual inspection of the results is also recommended for a comprehensive assessment.  

Feel free to customize this section based on your specific preferences and any additional information you want to include.

### Link to the Google Drive video link  
I have also provided a link to the Google Drive folder where all the original videos with their corresponding high-resolution video generated are located.  
-[Google drive video folder](https://drive.google.com/drive/folders/1AN_zPEvt1mUROVhLNyIsGbetRNiU6J_n?usp=sharing)  
click on the above link to access all the test videos.  

## Sample Input and Output attached
-[test video 1](https://drive.google.com/file/d/1NVU1U9Fzo9VHDRVa_bxeL6EpRxbNPMEU/view?usp=sharing)  
-[test video 1 output](https://drive.google.com/file/d/1jECWDRetBmAy87_Ge0HyBakuQC3vHP7q/view?usp=sharing)  

### Note: I have utilized the Google Colab environment for development purposes to leverage the GPU to generate each frame at a faster rate.

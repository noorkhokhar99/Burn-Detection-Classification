

### Inferencing on your local machine (with the most accurate model):

####  Installation:

``` shell
# or just download this entire repo
git clone https://github.com/Michael-OvO/Burn-Detection-Classification.git
```

#### Install Dependencies (it is recommended that you set up a virtual environment through anaconda):

``` shell
cd Burn-Detection-Classification/
pip install -r requirements.txt
```

#### Begin Inferencing:

Download the pre-trained weights and place them into the same master folder: [Skin_burn_2022_8_21.pt](https://github.com/Michael-OvO/Burn-Detection-Classification/releases/download/v1.0.0/skin_burn_2022_8_21.pt)

The sample images can be found in the folder inference, the name of each image corresponds to the ground truth value of each image(the model should predict those values after each run).

Below is the file: `1st_degree_2.jpg` (which is sunburn so the model should know that it is first degree)

<div align="center">
    <a href="./">
        <img src="./inference/images/1st_degree_2.jpg" width="59%"/>
    </a>
</div>



On video:

``` shell
python detect.py --weights Skin_burn_2022_8_21.pt  --source yourvideo.mp4
```

On image:
``` shell
python detect.py --weights Skin_burn_2022_8_21.pt --source inference/images/first_degree_2.jpg
```

<div align="center">
    <a href="./">
        <img src="./inference/results/1st_degree_2.jpg" width="59%"/>
    </a>
</div>



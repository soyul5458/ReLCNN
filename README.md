# MCHeart
This repository provides the overall framework for training and evaluating heart murmur detection systems proposed in 'MCHeart: Multi-Channel based Heart Signal Processing Scheme for Heart Noise Detection using Deep Learning'

## Data Access  
The training data of [the George B. Moody PhysioNet Challenge 2022](https://moody-challenge.physionet.org/2022/) can be downloaded from [PhysioNet](https://physionet.org/content/circor-heart-sound/1.0.3/) [1]. You can also download it directly using this [link](https://physionet.org/static/published-projects/circor-heart-sound/the-circor-digiscope-phonocardiogram-dataset-1.0.3.zip) or the following command:
```
wget -r -N -c -np https://physionet.org/files/circor-heart-sound/1.0.3/
```

## How do I run these scripts?
You can install the dependencies for these scripts by creating a Docker image (see below) and running
```
pip install requirements.txt
```

You can train your model by running
```
python train_model.py training_data model
```

where

* training_data (input; required) is a folder with the training data files and
* model (output; required) is a folder for saving your model.

## Requirements
* Tensorflow (tested with version 1.3)
* Numpy (tested with version 1.13.1)
* Scipy (tested with version 0.19.1)  
For openmax experiments you will need to clone https://github.com/abhijitbendale/OSDN into the this directory.


## Model Training
```
python3 main.py \
        --batch_size 200 \
        --num_workers 40 \
        --max_epochs 30 \
        --embedding_dim $embedding_dim \
        --save_dir $save_dir \
        --encoder_name $encoder_name \
        --train_csv_path $train_csv_path \
        --learning_rate 0.001 \
        --encoder_name ${encoder_name} \
        --num_classes $num_classes \
        --trial_path $trial_path \
        --loss_name $loss_name \
        --num_blocks $num_blocks \
        --step_size 4 \
        --gamma 0.5 \
        --weight_decay 0.0000001 \
        --input_layer $input_layer \
        --pos_enc_layer_type $pos_enc_layer_type 
```

## Citation
If you use this code please cite the paper.
```
@
```
## Useful links
* [Challenge website](https://moody-challenge.physionet.org/2022/)
* [Scoring code](https://github.com/physionetchallenges/evaluation-2022)

## References
[1] Heart Murmur Detection from Phonocardiogram Recordings: The George B.
Moody PhysioNet Challenge 2022
```
@inproceedings{reyna2022heart,
  title={Heart murmur detection from phonocardiogram recordings: The george b. moody physionet challenge 2022},
  author={Reyna, Matthew A and Kiarashi, Yashar and Elola, Andoni and Oliveira, Jorge and Renna, Francesco and Gu, Annie and Alday, Erick A Perez and Sadr, Nadi and Sharma, Ashish and Mattos, Sandra and others},
  booktitle={2022 Computing in Cardiology (CinC)},
  volume={498},
  pages={1--4},
  year={2022},
  organization={IEEE}
}
```

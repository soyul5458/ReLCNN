# ReLCNN


## Data Preparation


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

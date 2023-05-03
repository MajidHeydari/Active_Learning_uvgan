# Active_Learning_uvgan
Active Learning and uvgan for Semi Supervised Semantic Segmentation in Satellite Images


### UC Merced Land Use Classification Dataset

- Download the images and classification labels for the UC Merced Land Use Classification Dataset [here](http://weegee.vision.ucmerced.edu/datasets/landuse.html)
- Download the semantic segmentation labels for the UC Merced Land Use Classification Dataset (DLSRD Dataset) [here](https://sites.google.com/view/zhouwx/dataset#h.p_hQS2jYeaFpV0)

**Training the Active Learner**  

```
python train_AL.py --dataset-name UCM   
                           --query-strategy margin 
                           --random-scale 
                           --random-mirror 
                           --data-dir ./tar/Images
                           --data-list ./train/image_list
                           --labeled-ratio 0.5
                           --model-name res50
                           --num-classes 21
                           --learning-rate 0.001 
                           --num-epochs 50 
                           --alpha alpha
                           --beta beta
```

# Toolkit for UAV-Human Pose Estimation for TE-GCN
Generating splited UAV-Human Pose datasets (XSUB1 and XSUB2) for [TE-GCN](https://github.com/xieyulai/TE-GCN)

More information about HAV_Human, plese refer [HUA-Human](https://github.com/SUTDCV/UAV-Human/)





Extract the downloaded data ``Skeleton.zip`` into ``data`` folder.


Expected directory in  ``data`` folder.
```
└───Skeleton
    ├───P000S00G10B10H10UC022000LC021000A000R0_08241716.txt
    ├───P000S00G10B10H10UC022000LC021000A001R0_08241716.txt
```


Run the following scripts to split the files into the train and the test set respectively:
```
python split_v1.py 
python split_v2.py 
```

Run the following script to preprocess the files:
```
python generate_data.py --data_path data/v1 
python generate_data.py --data_path data/v2 
```

Expected directory in `data/v1`
```
└───data/v1
    ├───train
        ├───P000S00G10B10H10UC022000LC021000A000R0_08241716.txt
        ├───P000S00G10B10H10UC022000LC021000A001R0_08241716.txt
        └───...
    ├───test
        ├───P000S00G10B10H10UC022000LC021000A000R0_08241716.txt
        ├───P000S00G10B10H10UC022000LC021000A001R0_08241716.txt
        └───...
    ├───train_label.pkl
    ├───train_data.npy
    ├───test_data.npy
    └───test_label.pkl
```

`data/v1` has the similar structure

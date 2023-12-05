# VDTR for INR projects

> by zzh

## training

CUDA_VISIBLE_DEVICES=4,5,6,7 python -m torch.distributed.launch --nproc_per_node=4 --master_port=10086 train.py ./configs/vdtr/vdtr_gopro_inr.yaml --gpus=4

> the training logs are saved in `./workdir/*`. 

## testing

CUDA_VISIBLE_DEVICES=6 python test.py ./configs/vdtr/vdtr_gopro_inr.yaml $Checkpoint_path

> the testing logs and frames are saved in `./workdir/*`. 
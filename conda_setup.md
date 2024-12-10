```
conda create -n dextreme python=3.8 && conda activate dextreme
cd isaacgym/python/
pip install -e . --no-deps
cd IsaacGymEnvs/
pip install -e . --no-deps
pip install hydra-core urdfpy trimesh pysdf warp-lang scipy ninja rl_games numpy==1.23.1

pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/home/avery/anaconda3/envs/dextreme/lib
python train.py task=Cartpole
```

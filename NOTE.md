## Note of reproduction

* Dependencies
    * conda create -n cuae_env python=3.10
    * pip install -r requirements.txt
    * pip install -e .
**python=3.10 !!!**
* Debug 
    * features_and_labels/map_base.py line 46
    **[Debug] ValueError: mutable default <class 'numpy.ndarray'> for field lane_indices is not allowed: use default_factory**
    * lib/rollout.py line 113
    **[Debug] TypeError: Object of type int32 is not JSON serializable**

    * learning/data_curator.py line 58 
    **[Debug] ValueError: Expected more than 1 value per channel when training, got input size torch.Size([1, 128])**

    * hydra_configs/training_config/data_curator_config/prediction.yaml line 9
    **[Debug] TypeError: h5py objects cannot be pickled**
* Update
    * dataset_plugins module
    * requirement.txt => remove pyg-lib
    * rename lib.random => lib.random_init
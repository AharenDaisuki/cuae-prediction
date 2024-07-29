## Note of reproduction

* Dependencies
* Debug 
    * features_and_labels/map_base.py line 46
    **[Debug] ValueError: mutable default <class 'numpy.ndarray'> for field lane_indices is not allowed: use default_factory**
    * lib/rollout.py line 113
    **[Debug] TypeError: Object of type int32 is not JSON serializable**
* Update
    * dataset_plugins module
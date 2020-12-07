# EEL6935-Final-Project
This repository contains instructions for reproducing our resutls for the final project.

## Installation instructions
First insall gym in your python environment, then clone the miniworld environment and follow the instrcutions there to insall the codebase:

https://github.com/maximecb/gym-miniworld


## Replicating trained models

We provide the final model checkpoints of each trial in this repository for convenience. However, if you wish to do an experiment from scratch you can use this command:

```
python main.py --algo ppo --num-frames 5000000 --num-processes 4 --num-steps 80 --lr 0.00005 --env-name MiniWorld-Hallway-v0
```

You just need to replace the algo, num-steps, lr, and env-name with the particular experiment from our report you want to run. To visualize the agent's operation, use this command:

```
python enjoy.py --env-name MiniWorld-Hallway-v0 --load-dir trained_models/ppo
```

Replace env-name with the particular environment you want to visualize, and load-dir should be the path to saved pytorch weights (either the weights from saved_trials in this repository or weights from a model you have trained).

## Replicating visualizations

You can use the analysis.ipynb script under saved_trials to reproduce all our graphs.
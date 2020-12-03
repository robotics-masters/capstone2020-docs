# guide to downgrade to tensorflow cpu mode

As posted in slack

#random–Sep 21st Ben 11:26 PM

If you install tensorflow-gpu then realise your GPU or CUDA is insufficient

If you followed instructions and installed inside an activated conda environment using

replace the variables that are shown like <var>

conda activate <env1>

conda install tensorflow-gpu

then you can do

conda list –revisions

to show you revisions, installations and package changes, upgrades, downgrades.

1st to backup I did a clone of the active environment, fast. (perhaps optional and skipable)

conda create --name <env2> --clone <env1>

I was able to roll back to previous revision before tensorflow-gpu with

conda install -rev <number>

give it a minute, it will show you a plan and it did ask to proceed

then my tensorflow was just CPU

It didn't need to download or install anything and it was fast. after researching.

# DeepFaceLab with Google Colab - Tutorial

![](https://i.imgur.com/aN8cwwWh.jpg)
 
https://github.com/chervonij/DFL-Colab

## What is Google Colab?

Google Colab is a cloud service that allows your to use their network GPU for free. The only catch is that you only get 12 hour sessions at a time. Besides this, use is pretty much unlimited.

## Who should use DeepFaceLab with Google Colab?

Since this platform does not have a pretty GUI, and it's hard to view real-time training data, and image files; I only recommend using this if you understand the process in making deepfakes. It'll be very helpful if you have successfully made a few before using this.

* Users who wish to train more than one model at a time but only have one GPU.
* Users who wish to train a model with higher settings (dims, batch, etc) but cannot due to their GPU.

## Things to Know Before Starting
* Google may not like heavy computation and extraneous use. It is recommended to split your training over 2 accounts, but you can always use one Google Drive account to store your backups.
* After 12 hours of use, your notebook will reset. This version of DFL is setup to back up your workspace at ~11 hours.
* You need to keep your browser open while Google Colab is running.

**NOTE: Google has gotten smart and some users have reported getting errors and random closing of their connections. Google Colab may also stop assigning you a GPU temporarily if you have constant usage. If this happens you can try again later.**

![](https://i.postimg.cc/qq5qNKsd/bankend.jpg)

## Getting Started with DeepFaceLab on Google Colab

**NOTE: you MUST leave your browser open at all times while using Google Colab.*

You can find the pre-coded DFL on the platform here: https://colab.research.google.com/github/chervonij/DFL-Colab/blob/master/DFL_Colab_Demo.ipynb

This notebook is already set up for you to use. Google Colab doesn't really have a friend GUI, but the instructions are pretty clear in this notebook. When you first visit the link above, you'll have a screen like this:

![](https://i.imgur.com/SqCszw8h.jpg)

Left hand side = table of contents

Clicking on any of the left links will bring you to the corresponding "cell" that describes exactly what it does.

## Installing DeepFaceLab onto Google Colab

Move to step 1. What we will start doing is clone the Github repository and install all the prerequisites and DFL. This way we can ensure we always have the most updated version running.

To do this, click on the round play button to start executing the code:
![](https://i.imgur.com/yhyPgKeh.jpg)

When you click this button, you'll see a warning stating that the notebook you're using was not made by Google. It's okay, we're aware of this, and just click "RUN ANYWAY". You should also leave "Reset all runtimes before running" checked off so that your timer resets and you'll have a full ~12 hours of training.

![](https://i.imgur.com/cOXLhb3h.jpg)

Next you'll appropriately get a warning stating that if you reset your runtime, you will lose everything. Yes, this includes all files on the notebook. Just click yes and continue on.

![](https://i.imgur.com/1lvHI3Ph.jpg)

Once you do that, you'' quickly see some text appear. It's basically installing everything you need to run DeepFaceLab. Just sit back and wait a few minutes until it's complete. Your output should looks something similar to this:

Code:
Cloning into 'DeepFaceLab'...
remote: Enumerating objects: 38, done.
remote: Counting objects: 100% (38/38), done.
remote: Compressing objects: 100% (30/30), done.
remote: Total 2979 (delta 14), reused 22 (delta 8), pack-reused 2941
Receiving objects: 100% (2979/2979), 303.30 MiB | 37.93 MiB/s, done.
Resolving deltas: 100% (1898/1898), done.
Checking out files: 100% (119/119), done.
Collecting git+https://www.github.com/keras-team/keras-contrib.git (from -r /content/DeepFaceLab/requirements-colab.txt (line 10))
 Cloning https://www.github.com/keras-team/keras-contrib.git to /tmp/pip-req-build-dcwygg6m
Requirement already satisfied: numpy==1.16.3 in /usr/local/lib/python3.6/dist-packages (from -r /content/DeepFaceLab/requirements-colab.txt (line 1)) (1.16.3)
Collecting h5py==2.9.0 (from -r /content/DeepFaceLab/requirements-colab.txt (line 2))
 Downloading https://files.pythonhosted.org/packages/30/99/d7d4fbf2d02bb30fb76179911a250074b55b852d34e98dd452a9f394ac06/h5py-2.9.0-cp36-cp36m-manylinux1_x86_64.whl (2.8MB)
   100% |████████████████████████████████| 2.8MB 10.5MB/s 
Requirement already satisfied: Keras==2.2.4 in /usr/local/lib/python3.6/dist-packages (from -r /content/DeepFaceLab/requirements-colab.txt (line 3)) (2.2.4)
Collecting opencv-python==4.0.0.21 (from -r /content/DeepFaceLab/requirements-colab.txt (line 4))
 Downloading https://files.pythonhosted.org/packages/37/49/874d119948a5a084a7ebe98308214098ef3471d76ab74200f9800efeef15/opencv_python-4.0.0.21-cp36-cp36m-manylinux1_x86_64.whl (25.4MB)
   100% |████████████████████████████████| 25.4MB 1.5MB/s 
Collecting tensorflow-gpu==1.13.1 (from -r /content/DeepFaceLab/requirements-colab.txt (line 5))
 Downloading https://files.pythonhosted.org/packages/7b/b1/0ad4ae02e17ddd62109cd54c291e311c4b5fd09b4d0678d3d6ce4159b0f0/tensorflow_gpu-1.13.1-cp36-cp36m-manylinux1_x86_64.whl (345.2MB)
   100% |████████████████████████████████| 345.2MB 62kB/s 
Collecting plaidml-keras==0.5.0 (from -r /content/DeepFaceLab/requirements-colab.txt (line 6))
 Downloading https://files.pythonhosted.org/packages/17/34/4102261e3d8867c31bae9f4def5d7e700fc25fff232fa1780040e8ed79b0/plaidml_keras-0.5.0-py2.py3-none-any.whl
Requirement already satisfied: scikit-image in /usr/local/lib/python3.6/dist-packages (from -r /content/DeepFaceLab/requirements-colab.txt (line 7)) (0.14.2)
Requirement already satisfied: tqdm in /usr/local/lib/python3.6/dist-packages (from -r /content/DeepFaceLab/requirements-colab.txt (line 8)) (4.28.1)
Collecting ffmpeg-python==0.1.17 (from -r /content/DeepFaceLab/requirements-colab.txt (line 9))
 Downloading https://files.pythonhosted.org/packages/3d/10/330cbc8e63d072d40413f4d470444a6a1e8c8c6a80b2a4ac302d1252ca1b/ffmpeg_python-0.1.17-py3-none-any.whl
Requirement already satisfied: six in /usr/local/lib/python3.6/dist-packages (from h5py==2.9.0->-r /content/DeepFaceLab/requirements-colab.txt (line 2)) (1.12.0)
Requirement already satisfied: scipy>=0.14 in /usr/local/lib/python3.6/dist-packages (from Keras==2.2.4->-r /content/DeepFaceLab/requirements-colab.txt (line 3)) (1.2.1)
Requirement already satisfied: keras-preprocessing>=1.0.5 in /usr/local/lib/python3.6/dist-packages (from Keras==2.2.4->-r /content/DeepFaceLab/requirements-colab.txt (line 3)) (1.0.9)
Requirement already satisfied: pyyaml in /usr/local/lib/python3.6/dist-packages (from Keras==2.2.4->-r /content/DeepFaceLab/requirements-colab.txt (line 3)) (3.13)
Requirement already satisfied: keras-applications>=1.0.6 in /usr/local/lib/python3.6/dist-packages (from Keras==2.2.4->-r /content/DeepFaceLab/requirements-colab.txt (line 3)) (1.0.7)
Requirement already satisfied: absl-py>=0.1.6 in /usr/local/lib/python3.6/dist-packages (from tensorflow-gpu==1.13.1->-r /content/DeepFaceLab/requirements-colab.txt (line 5)) (0.7.1)
Requirement already satisfied: tensorboard<1.14.0,>=1.13.0 in /usr/local/lib/python3.6/dist-packages (from tensorflow-gpu==1.13.1->-r /content/DeepFaceLab/requirements-colab.txt (line 5)) (1.13.1)
Requirement already satisfied: tensorflow-estimator<1.14.0rc0,>=1.13.0 in /usr/local/lib/python3.6/dist-packages (from tensorflow-gpu==1.13.1->-r /content/DeepFaceLab/requirements-colab.txt (line 5)) (1.13.0)
Requirement already satisfied: termcolor>=1.1.0 in /usr/local/lib/python3.6/dist-packages (from tensorflow-gpu==1.13.1->-r /content/DeepFaceLab/requirements-colab.txt (line 5)) (1.1.0)
Requirement already satisfied: wheel>=0.26 in /usr/local/lib/python3.6/dist-packages (from tensorflow-gpu==1.13.1->-r /content/DeepFaceLab/requirements-colab.txt (line 5)) (0.33.1)
Requirement already satisfied: gast>=0.2.0 in /usr/local/lib/python3.6/dist-packages (from tensorflow-gpu==1.13.1->-r /content/DeepFaceLab/requirements-colab.txt (line 5)) (0.2.2)
Requirement already satisfied: grpcio>=1.8.6 in /usr/local/lib/python3.6/dist-packages (from tensorflow-gpu==1.13.1->-r /content/DeepFaceLab/requirements-colab.txt (line 5)) (1.15.0)
Requirement already satisfied: protobuf>=3.6.1 in /usr/local/lib/python3.6/dist-packages (from tensorflow-gpu==1.13.1->-r /content/DeepFaceLab/requirements-colab.txt (line 5)) (3.7.1)
Requirement already satisfied: astor>=0.6.0 in /usr/local/lib/python3.6/dist-packages (from tensorflow-gpu==1.13.1->-r /content/DeepFaceLab/requirements-colab.txt (line 5)) (0.7.1)
Collecting plaidml (from plaidml-keras==0.5.0->-r /content/DeepFaceLab/requirements-colab.txt (line 6))
 Downloading https://files.pythonhosted.org/packages/48/b7/5c019a8c64e92fc69c77f077e9a1bc6ea7883eb8fd79c639082c7984bfb5/plaidml-0.5.0-py2.py3-none-manylinux1_x86_64.whl (15.0MB)
   100% |████████████████████████████████| 15.0MB 2.2MB/s 
Requirement already satisfied: pillow>=4.3.0 in /usr/local/lib/python3.6/dist-packages (from scikit-image->-r /content/DeepFaceLab/requirements-colab.txt (line 7)) (4.3.0)
Requirement already satisfied: dask[array]>=1.0.0 in /usr/local/lib/python3.6/dist-packages (from scikit-image->-r /content/DeepFaceLab/requirements-colab.txt (line 7)) (1.1.5)
Requirement already satisfied: matplotlib>=2.0.0 in /usr/local/lib/python3.6/dist-packages (from scikit-image->-r /content/DeepFaceLab/requirements-colab.txt (line 7)) (3.0.3)
Requirement already satisfied: PyWavelets>=0.4.0 in /usr/local/lib/python3.6/dist-packages (from scikit-image->-r /content/DeepFaceLab/requirements-colab.txt (line 7)) (1.0.3)
Requirement already satisfied: networkx>=1.8 in /usr/local/lib/python3.6/dist-packages (from scikit-image->-r /content/DeepFaceLab/requirements-colab.txt (line 7)) (2.3)
Requirement already satisfied: cloudpickle>=0.2.1 in /usr/local/lib/python3.6/dist-packages (from scikit-image->-r /content/DeepFaceLab/requirements-colab.txt (line 7)) (0.6.1)
Requirement already satisfied: future in /usr/local/lib/python3.6/dist-packages (from ffmpeg-python==0.1.17->-r /content/DeepFaceLab/requirements-colab.txt (line 9)) (0.16.0)
Requirement already satisfied: markdown>=2.6.8 in /usr/local/lib/python3.6/dist-packages (from tensorboard<1.14.0,>=1.13.0->tensorflow-gpu==1.13.1->-r /content/DeepFaceLab/requirements-colab.txt (line 5)) (3.1)
Requirement already satisfied: werkzeug>=0.11.15 in /usr/local/lib/python3.6/dist-packages (from tensorboard<1.14.0,>=1.13.0->tensorflow-gpu==1.13.1->-r /content/DeepFaceLab/requirements-colab.txt (line 5)) (0.15.2)
Requirement already satisfied: mock>=2.0.0 in /usr/local/lib/python3.6/dist-packages (from tensorflow-estimator<1.14.0rc0,>=1.13.0->tensorflow-gpu==1.13.1->-r /content/DeepFaceLab/requirements-colab.txt (line 5)) (2.0.0)
Requirement already satisfied: setuptools in /usr/local/lib/python3.6/dist-packages (from protobuf>=3.6.1->tensorflow-gpu==1.13.1->-r /content/DeepFaceLab/requirements-colab.txt (line 5)) (40.9.0)
Requirement already satisfied: enum34>=1.1.6 in /usr/local/lib/python3.6/dist-packages (from plaidml->plaidml-keras==0.5.0->-r /content/DeepFaceLab/requirements-colab.txt (line 6)) (1.1.6)
Requirement already satisfied: olefile in /usr/local/lib/python3.6/dist-packages (from pillow>=4.3.0->scikit-image->-r /content/DeepFaceLab/requirements-colab.txt (line 7)) (0.46)
Requirement already satisfied: toolz>=0.7.3; extra == "array" in /usr/local/lib/python3.6/dist-packages (from dask[array]>=1.0.0->scikit-image->-r /content/DeepFaceLab/requirements-colab.txt (line 7)) (0.9.0)
Requirement already satisfied: pyparsing!=2.0.4,!=2.1.2,!=2.1.6,>=2.0.1 in /usr/local/lib/python3.6/dist-packages (from matplotlib>=2.0.0->scikit-image->-r /content/DeepFaceLab/requirements-colab.txt (line 7)) (2.4.0)
Requirement already satisfied: python-dateutil>=2.1 in /usr/local/lib/python3.6/dist-packages (from matplotlib>=2.0.0->scikit-image->-r /content/DeepFaceLab/requirements-colab.txt (line 7)) (2.5.3)
Requirement already satisfied: cycler>=0.10 in /usr/local/lib/python3.6/dist-packages (from matplotlib>=2.0.0->scikit-image->-r /content/DeepFaceLab/requirements-colab.txt (line 7)) (0.10.0)
Requirement already satisfied: kiwisolver>=1.0.1 in /usr/local/lib/python3.6/dist-packages (from matplotlib>=2.0.0->scikit-image->-r /content/DeepFaceLab/requirements-colab.txt (line 7)) (1.0.1)
Requirement already satisfied: decorator>=4.3.0 in /usr/local/lib/python3.6/dist-packages (from networkx>=1.8->scikit-image->-r /content/DeepFaceLab/requirements-colab.txt (line 7)) (4.4.0)
Requirement already satisfied: pbr>=0.11 in /usr/local/lib/python3.6/dist-packages (from mock>=2.0.0->tensorflow-estimator<1.14.0rc0,>=1.13.0->tensorflow-gpu==1.13.1->-r /content/DeepFaceLab/requirements-colab.txt (line 5)) (5.1.3)
Building wheels for collected packages: keras-contrib
 Building wheel for keras-contrib (setup.py) ... done
 Stored in directory: /tmp/pip-ephem-wheel-cache-crmwvsgs/wheels/11/27/c8/4ed56de7b55f4f61244e2dc6ef3cdbaff2692527a2ce6502ba
Successfully built keras-contrib
albumentations 0.1.12 has requirement imgaug<0.2.7,>=0.2.5, but you'll have imgaug 0.2.8 which is incompatible.
Installing collected packages: h5py, opencv-python, tensorflow-gpu, plaidml, plaidml-keras, ffmpeg-python, keras-contrib
 Found existing installation: h5py 2.8.0
   Uninstalling h5py-2.8.0:
     Successfully uninstalled h5py-2.8.0
 Found existing installation: opencv-python 3.4.5.20
   Uninstalling opencv-python-3.4.5.20:
     Successfully uninstalled opencv-python-3.4.5.20
Successfully installed ffmpeg-python-0.1.17 h5py-2.9.0 keras-contrib-2.0.8 opencv-python-4.0.0.21 plaidml-0.5.0 plaidml-keras-0.5.0 tensorflow-gpu-1.13.1
Collecting scikit-image
 Downloading https://files.pythonhosted.org/packages/d4/ab/674e168bf7d0bc597218b3bec858d02c23fbac9ec1fec9cad878c6cee95f/scikit_image-0.15.0-cp36-cp36m-manylinux1_x86_64.whl (26.3MB)
   100% |████████████████████████████████| 26.3MB 1.4MB/s 
Requirement already satisfied, skipping upgrade: imageio>=2.0.1 in /usr/local/lib/python3.6/dist-packages (from scikit-image) (2.4.1)
Requirement already satisfied, skipping upgrade: scipy>=0.17.0 in /usr/local/lib/python3.6/dist-packages (from scikit-image) (1.2.1)
Requirement already satisfied, skipping upgrade: matplotlib!=3.0.0,>=2.0.0 in /usr/local/lib/python3.6/dist-packages (from scikit-image) (3.0.3)
Requirement already satisfied, skipping upgrade: networkx>=2.0 in /usr/local/lib/python3.6/dist-packages (from scikit-image) (2.3)
Requirement already satisfied, skipping upgrade: pillow>=4.3.0 in /usr/local/lib/python3.6/dist-packages (from scikit-image) (4.3.0)
Requirement already satisfied, skipping upgrade: PyWavelets>=0.4.0 in /usr/local/lib/python3.6/dist-packages (from scikit-image) (1.0.3)
Requirement already satisfied, skipping upgrade: numpy in /usr/local/lib/python3.6/dist-packages (from imageio>=2.0.1->scikit-image) (1.16.3)
Requirement already satisfied, skipping upgrade: pyparsing!=2.0.4,!=2.1.2,!=2.1.6,>=2.0.1 in /usr/local/lib/python3.6/dist-packages (from matplotlib!=3.0.0,>=2.0.0->scikit-image) (2.4.0)
Requirement already satisfied, skipping upgrade: cycler>=0.10 in /usr/local/lib/python3.6/dist-packages (from matplotlib!=3.0.0,>=2.0.0->scikit-image) (0.10.0)
Requirement already satisfied, skipping upgrade: python-dateutil>=2.1 in /usr/local/lib/python3.6/dist-packages (from matplotlib!=3.0.0,>=2.0.0->scikit-image) (2.5.3)
Requirement already satisfied, skipping upgrade: kiwisolver>=1.0.1 in /usr/local/lib/python3.6/dist-packages (from matplotlib!=3.0.0,>=2.0.0->scikit-image) (1.0.1)
Requirement already satisfied, skipping upgrade: decorator>=4.3.0 in /usr/local/lib/python3.6/dist-packages (from networkx>=2.0->scikit-image) (4.4.0)
Requirement already satisfied, skipping upgrade: olefile in /usr/local/lib/python3.6/dist-packages (from pillow>=4.3.0->scikit-image) (0.46)
Requirement already satisfied, skipping upgrade: six in /usr/local/lib/python3.6/dist-packages (from cycler>=0.10->matplotlib!=3.0.0,>=2.0.0->scikit-image) (1.12.0)
Requirement already satisfied, skipping upgrade: setuptools in /usr/local/lib/python3.6/dist-packages (from kiwisolver>=1.0.1->matplotlib!=3.0.0,>=2.0.0->scikit-image) (40.9.0)
albumentations 0.1.12 has requirement imgaug<0.2.7,>=0.2.5, but you'll have imgaug 0.2.8 which is incompatible.
Installing collected packages: scikit-image
 Found existing installation: scikit-image 0.14.2
   Uninstalling scikit-image-0.14.2:
     Successfully uninstalled scikit-image-0.14.2
Successfully installed scikit-image-0.15.0`

The whole process should only take around 2 minutes.

## Importing your workspace to DeepFaceLab on Google Colab

Next we want to import the workspace we have setup on our PC to the Google Colab notebook. To due this, we will have to go to Google Drive and upload our workspace in a zip file.

Right click on your "workspace" folder, and zip it.

Next go to https://drive.google.com and upload it to the main folder. Make sure you're using the same Google account as the one you're using on Google Colab.

Next go back to your notebook, and move down to the "Manage workspace" section. What we want to do is Import from Drive.

![](https://i.imgur.com/tIkHV2Fh.jpg)

Once you click on the play button, it'll prompt you to go to a URL to get your authorization code, which you'll then need to enter into the input field. 

![](https://i.imgur.com/cDOcZo0h.jpg)

Again, be sure to select the same Google account you're using on colab, and just click agree to all the permissions to receive your code. Put your code into the field, and then click enter.

It'll take a few minutes to import from Google Drive depending on how large your workspace folder is. Once completed you'll get an output similar to this:


`Code:
Mounted at /content/drive
/content
Done!`

Success! You're now ready to begin extracting, sorting, training or converting.

Since I use my own PC for most of the hands-on work, I usually only use Colab to train models 12 hours at a time.

## Training DeepFaceLab Models on Google Colab

Next, go back up to the "3. Train model" section. Here we can select the type of model we would like to train with the drop down menu. I mainly use SAE so that's what I've selected. Before training, make sure your data_src and data_dst aligned facesets are all cleaned and ready to go.

![](https://i.imgur.com/7lxARNrh.jpg)

After selecting, click on the play button again. You'll see some code once again as it prepares to train.


`Code:
Drive already mounted at /content/drive; to attempt to forcibly remount, call drive.mount("/content/drive", force_remount=True).
Time to backup: 11 hours
/content
Running trainer.

Loading model...
Press enter in 2 seconds to override model settings./usr/lib/python3.6/multiprocessing/semaphore_tracker.py:143: UserWarning: semaphore_tracker: There appear to be 1 leaked semaphores to clean up at shutdown
 len(cache))
Using TensorFlow backend.
WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/tensorflow/python/framework/op_def_library.py:263: colocate_with (from tensorflow.python.framework.ops) is deprecated and will be removed in a future version.
Instructions for updating:
Colocations handled automatically by placer.
WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/tensorflow/python/ops/math_ops.py:3066: to_int32 (from tensorflow.python.ops.math_ops) is deprecated and will be removed in a future version.
Instructions for updating:
Use tf.cast instead.`

As usual, if you wish to change your model training settings, click unter in the input field. Keep in mind there is a slight delay with this field, so sometimes you may have to push it a few times, or even earlier than the prompt.

The full output once it begins training looks like the usual one on Windows.

`Code:
Drive already mounted at /content/drive; to attempt to forcibly remount, call drive.mount("/content/drive", force_remount=True).
Time to backup: 11 hours
/content
Running trainer.

Loading model...
Press enter in 2 seconds to override model settings./usr/lib/python3.6/multiprocessing/semaphore_tracker.py:143: UserWarning: semaphore_tracker: There appear to be 1 leaked semaphores to clean up at shutdown
 len(cache))
Using TensorFlow backend.
WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/tensorflow/python/framework/op_def_library.py:263: colocate_with (from tensorflow.python.framework.ops) is deprecated and will be removed in a future version.
Instructions for updating:
Colocations handled automatically by placer.
WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/tensorflow/python/ops/math_ops.py:3066: to_int32 (from tensorflow.python.ops.math_ops) is deprecated and will be removed in a future version.
Instructions for updating:
Use tf.cast instead.
Loading: 100% 3123/3123 [00:03<00:00, 797.46it/s]
Loading: 100% 101635/101635 [01:49<00:00, 928.34it/s]
===== Model summary =====
== Model name: SAE
==
== Current iteration: 150263
==
== Model options:
== |== batch_size : 16
== |== sort_by_yaw : False
== |== random_flip : False
== |== resolution : 128
== |== face_type : f
== |== learn_mask : True
== |== optimizer_mode : 1
== |== archi : df
== |== ae_dims : 512
== |== e_ch_dims : 42
== |== d_ch_dims : 21
== |== remove_gray_border : False
== |== multiscale_decoder : True
== |== pixel_loss : False
== |== face_style_power : 0.1
== |== bg_style_power : 4.0
== |== ca_weights : False
== Running on:
== |== [0 : Tesla T4]
=========================
Starting. Press "Enter" to stop training and save model.
[03:06:45][#150270][2315ms][0.4100][0.4467]`

## Previewing Your Training

You can't get real-time preview training data like when you use DeepFaceLab on your desktop, but you can check the preview snapshot of your training. This is updated every 10 iterations, so it's almost real-time. Just navigate to the left panel, and go into your "model" folder. There will be a file called "SAE_preview_SAE.jpg". You can double click on the jpg file to open a new window for the preview. It is a small window, but you can scroll.

![Image: uPJkYydh.jpg](https://i.imgur.com/uPJkYydh.jpg)

![Image: eyT6ZKRh.jpg](https://i.imgur.com/eyT6ZKRh.jpg)


## Saving Your Model and Workspace

The good thing about this is the developer set in an automatic backup and save feature. Remember, your session will restart 12 hours after your first reset. To prevent you from losing data, this pre-made notebook will automaticially archive and upload your whole "workspace" to Google Drive after about 11 hours.

If you wish to manually export yourself, first you need to stop training. You can do this by clicking on the stop button.

![](https://i.imgur.com/yOVeus4h.jpg)

As soon as you do that, you'll see some shut down messages like this:

`Code:
/usr/lib/python3.6/multiprocessing/semaphore_tracker.py:143: UserWarning: semaphore_tracker: There appear to be 1 leaked semaphores to clean up at shutdown
 len(cache))
/usr/lib/python3.6/multiprocessing/semaphore_tracker.py:143: UserWarning: semaphore_tracker: There appear to be 1 leaked semaphores to clean up at shutdown
 len(cache))
/usr/lib/python3.6/multiprocessing/semaphore_tracker.py:143: UserWarning: semaphore_tracker: There appear to be 1 leaked semaphores to clean up at shutdown
 len(cache))
/usr/lib/python3.6/multiprocessing/semaphore_tracker.py:143: UserWarning: semaphore_tracker: There appear to be 1 leaked semaphores to clean up at shutdown
 len(cache))`

Then your button will have reset on the top left.

Next go back to the "Manage workspace" section and use the "Export to Drive" cell. You can choose to backup your entire workspace, or individual folders within it. I usually just do the entire workspace.

![Image: 3PxCjNHh.jpg](https://i.imgur.com/3PxCjNHh.jpg)

Once you click the play button again, it'll begin zipping your workspace, and uploading it automatically to your Google Drive. Once completed, you'll see a message similar to the following:

`Code:
Mounted at /content/drive
/content
Done!`

You can now check your Google Drive folder and download the recently exported workspace.

This is all I use the Google Colab for, but if you need to use the other features it's pretty self explanatory.

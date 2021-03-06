
### BEGAN-tensorflow

Training example:

    python main.py --dataset=portrait_64_64 --data_dir=../../datasets/ --load_path=logs/portrait_64_64_0404_100535 --use_gpu=True --is_train=False


### DCGAN-tensorflow

Training example:

    python main.py --dataset landscape_128 --data_dir ../../datasets/ --input_height=128 --output_height=128 --train
    
Training example:

    python main.py --dataset landscapes_128 --data_dir ../../datasets/ --input_height=128 --output_height=128 


### art-DCGAN

Training example:


Testing example:

    net=checkpoints/experiment4_800_net_G.t7 name=experiment imsize=1 display=0 th generate.lua 


### char-rnn-tensorflow

    python train.py --data_dir=./data/sherlock/
    python sample.py --save_dir=./save/ -n 200 --prime "hello"

### darknet

    ./darknet detect cfg/yolov3.cfg yolov3.weights data/dog.jpg
    ./darknet segmenter cfg/yolov3.cfg yolov3.weights data/dog.jpg
    # add deepdream
    
    

### neural-style

    th neural_style.lua -style_image examples/inputs/picasso_selfport1907.jpg -content_image examples/inputs/brad_pitt.jpg -output_image profile.png -num_iterations 1000 -image_size 512 
    

### pix2pix-tensorflow

    python tools/download-dataset.py facades
    python pix2pix.py  --mode train  --output_dir facades_train  --max_epochs 2 --input_dir facades/train --which_direction BtoA
    python pix2pix.py  --mode test --output_dir facades_test --input_dir facades/val --checkpoint facades_train


### pytorch-CycleGAN-and-pix2pix


### neural-enhance

    python3 enhance.py --type=photo --model=default --zoom=2 broken.jpg
    
### tensorflow-wavenet

    python train.py --data_dir=corpus
    python generate.py --samples 16000 --wav_out_path sample.wav logdir/train/2018-04-11T08-00-30/model.ckpt-19250

### densecap
    
    th run_model.lua -input_image ../../datasets/landscape/brookville.jpg
    python3 -m http.server 8181
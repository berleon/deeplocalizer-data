# Tagged BeesBook images

## Generate Dataset

Compile [deeplocalizer](https://github.com/berleon/deeplocalizer) and make sure
its binary directory is in your `$PATH` variable, then run:

```
$ generate_dataset --save-format Images --output-dir data tagged_images.txt
```

This will write the training dataset to the `data` directory.
Its structure is as follows:

```
- data \  train      \ train.txt       File with image paths and labels
       |             \ *.jpeg          The trainings images
       |- test       \ test.txt        File with image paths and labels
       |             \ *.jpeg          The trainings images
       |- validation \ validation.txt  File with image paths and labels
                     \ *.jpeg          The trainings images
```

Use `--save-format LMDB` if you want create a LMDB database for Caffe.
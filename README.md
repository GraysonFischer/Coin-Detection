# Project Name

The intention of my project was to catigorize different types of coins from around the world.

![Screenshot 2023-07-14 101543](https://github.com/GraysonFischer/Coin-Detection/assets/139392197/9005cb24-decf-445a-9ed9-50c0fefb4dc6)

## The Algorithm

To start, I found a file with lots of different pictures of all different coins. I only decided to go with three different coins, cents, euros, and chinese yuan. I put the images into three different files, test, train, and val, which all have different intentions. The tests file is where you pick the picture you want the computer to figure out. Train is where the computer learns the different types of coins and categorize them based on shape and color. The val file is what the computer looks at when you pick a coin form the tests, it does this so that it can find similarities between them. I started by running the program though 35 epochs, an epoch is the computers process of learning the different type of images and pictures in the train file. So where did this go wrong? Before, I said that the computer uses color and shape to categorize the different images, but for coins, they all look the same. I ran the computer countlessly through epochs and ended up doing a total of over 200, but no matter what, it still couldn't tell the difference between them.

## Running this project

Categorize the different images into the test, train, and val files. When running epochs, the computer will look throught the train file. When you pick a picture you want to test from the test file, it will look into the val file for recognitions between the two images and try and determin when type of coin it is. `imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=data/labels.txt data/coins_images/test/us_coins/1a1f6fe1c9.jpg` is the code I would use to test a picutre, here's how it works. First, we have to tell the computer where to go to get this picture, which is in the `coins_images` folder. So we would do `data` > `coins_images` > `test` > `us_coins` (or whatever coin you want). After the image is done loading, it should give you a class and a percent, the percent reprecent its cerenty to the class and the class is the type of coin it in.

https://www.youtube.com/watch?v=FKDRwUkoTt0

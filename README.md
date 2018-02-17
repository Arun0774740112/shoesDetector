# Shoes Detection using Faster R-CNN

We developed an application which detects different kinds of shoe such as a slipper, sandal and shoe.

![shoe detection example](readme_files/shoe_detector_example.png)

## Execution Procedure

![system configuration](readme_files/system_configuration.png)

1. Take a picture of shoes and send it to the GPU machine every few seconds
2. Count the number of each types of shoes in the picture and create a result image
3. Display the result on PC

## Experimental Results

<table>
    <tr>
      <td rowspan="2"></td>
      <td colspan=4 align="center">Classified As</td>
    </tr>
    <tr>
      <th>Shoe</th>
      <th>Sandal</th>
      <th>Slipper</th>
      <th>BG</th>
    </tr>
    <tr>
      <th>Shoe</th>
      <td align="right">9</td>
      <td align="right">3</td>
      <td align="right">0</td>
      <td align="right">12</td>
    </tr>
    <tr>
      <th>Sandal</th>
      <td align="right">0</td>
      <td align="right">10</td>
      <td align="right">0</td>
      <td align="right">3</td>
    </tr>
    <tr>
      <th>Slipper</th>
      <td align="right">0</td>
      <td align="right">0</td>
      <td align="right">17</td>
      <td align="right">4</td>
    </tr>
    <tr>
      <th>BG</th>
      <td align="right">1</td>    
      <td align="right">3</td>
      <td align="right">4</td>
      <td>-</td>
    </tr>
</table>

## How to Use

Egii, please fill in this part.

## Folders
We saved training, test images and annotations in *data/*.

## Training and test
We used *combo_master.py* to controls the slave script *train_frcnn.py* and *with_output_dir_test_frcnn.py*. As a result we can train multiple training and test phase in one run.

## Result
combo_master.py's result for detecting test pictures are saved in *result_imgs/*. Also training log, best score weight are saved in *logs/* and *weights/*. Saving name *model_frcnn_X* have an index *X* which is the identity for log, weight, pickle file.

Example in file naming:

weight: model_frcnn_5.hdf5  

log: model_frcnn_5.txt

result image directory: model_frcnn_5/

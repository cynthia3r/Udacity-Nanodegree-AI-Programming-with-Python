# Pre-Trained Dog Image Classifier
Implement code in python to use a pre-trained image classifier to identify dog breeds
------------------------------------------------------------------------------------------

## Principal Objectives:
1. Correctly identify which pet images are of dogs (even if breed is misclassified) and which pet images aren't of dogs.
2. Correctly classify the breed of dog, for the images that are of dogs.
3. Determine which CNN model architecture (ResNet, AlexNet, or VGG), "best" achieve the objectives 1 and 2.
4. Consider the time resources required to best achieve objectives 1 and 2, and determine if an alternative solution would have given a "good enough" result, given the amount of time each of the algorithms take to run.
&nbsp;  
&nbsp;

## Project implementation details:
1. Time image classifier program
..* Use Time Module to compute program runtime
2. Get program Inputs from the user
..* Use command line arguments to get user inputs
3. Create Pet Images Labels
..* Use the pet images filenames to create labels
..* Store the pet image labels in a data structure (e.g. dictionary)
4. Create Classifier Labels and Compare Labels
..* Use the Classifier function to classify the images and create the classifier labels
..* Compare Classifier Labels to Pet Image Labels
..* Store Pet Labels, Classifier Labels, and their comparison in a complex data structure (e.g. dictionary of lists)
5. Classifying Labels as "Dogs" or "Not Dogs"
..* Classify all Labels as "Dogs" or "Not Dogs" using dognames.txt file
..* Store new classifications in the complex data structure (e.g. dictionary of lists)
6. Calculate the Results
..* Use Labels and their classifications to determine how well the algorithm worked on 	   classifying images
7. Print the Results
&nbsp;  
&nbsp;

## The project meets the following specifications:
Timing Code:
..* calls the time functions before the start of main code and after the main logic has been finished
Command Line arguments:
..* adds command line argument for '--dir', uses default ='pet_images/'
..* adds command line argument for '--arch', uses default='vgg'
..* adds command line argument for '--dogfile', uses default='dognames.txt'
Pet Image Labels:
..* Makes sure files starting with '.' are ignored. Checks for '.' using a conditional statement.
..* Dictionary key and label are in the correct format and retrieves 40 key-value pairs.
e.g:- {'Poodle_07956.jpg': ['poodle'], 'fox_squirrel_01.jpg': ['fox squirrel'] ... }
..* 'in_arg.dir' is passed as an argument inside check_images.py while calling the get_pet_labels function.
Classifying Images:
..* Appends images_dir to each value before making the function call.
..* classifier(images_dir+users_key, model)
..* Convert the output to lower case and strip any whitespaces
..* Appends 1 to correct label, and 0 to falsely classified values
Classifying Labels as Dogs:
..* Check the displayed output and see if all matches are appropriately displayed.
..* Check the displayed output and see if all non matches are appropriately displayed
Results:
..* All three models score as expected.
&nbsp;  
&nbsp;

## Running the Project on a Local Computer
While it is recommended that you work on the project within the **_Project Workspace_**, to run the project on a local computer, you will have needed to have python 3.6 intalled on your computer. 
### Installing Anaconda 
The easiest way to install python and the appropriate python modules is to install [Anaconda](https://www.anaconda.com/download).
### Installing PyTorch and torchvision
### Linux, OSX(Mac), Windows
For this project you will also need to install the python packages pytorch and torchvision.  If your local computer has a Linux, OSX (Mac), or Windows operating system look to [*Get Started.*](http://pytorch.org/) for installation instructions. 
&nbsp;     
&nbsp;    
   
## Files Required to Run **_check_images.py_** Locally
The following files and folders need to be put in the same folder as the **_check_images.py_** python program on your local computer.
### List of supported Files:
* **pet_images**  (folder of 40 pet image)
* **uploaded_images** (a folder created to upload images to be identified by the pre-trained classifier)
* **classifier.py** (classifier function used to classify the images)
* **dognames.txt** (file that contains all the valid dog names from the classifier function and the pet image files)
* **imagenet1000_clsid_to_human.txt** (dictionary that converts the classifier function ids to text labels)
* **adjust_results4_isadog.py** (a program that contains the **adjust_results4_isadog** function that is defined as part of the project)
* **calculates_results_stats.py** (a program that contains the **calculates_results_stats** function that is defined as part of the project)
* **classify_images.py** (a program that contains the **classify_images** function that is defined as part of the project)
* **get_input_args.py** (a program that contains the **get_input_args** function that is defined as part of the project)
* **get_pet_labels.py** (a program that contains the **get_pet_labels** function that is defined as part of the project)
* **print_results.py** (a program that contains the **print_results** function that is defined as part of the project)
* **run_models_batch.sh** (a bash script that will run check_images.py sequentially for all 3 model architectures and output their results to text files - on Unix/Linux/OSX/Project Workspace from a terminal window)
* **run_models_batch.bat** (a batch script that will run check_images.py sequentially for all 3 model architectures and output their results to text files - on Windows from the Anaconda Prompt window)
* **run_models_batch_uploaded.sh** (a bash script that will run check_images.py sequentially for all 3 model architectures  on the uploaded images folder and output their results to text files - on Unix/Linux/OSX/Project Workspace from a terminal window)
* **run_models_batch_uploaded.bat** (a batch script that will run check_images.py sequentially for all 3 model architectures on the uploaded images folder and output their results to text files - on Windows from the Anaconda Prompt window)
* **test_classifier.py** (an example program that demonstrates how to use the classifier function)
* **print_functions_for_lab_checks.py** (a program that contains functions that allows to check the code)
&nbsp;  
&nbsp;

## Running Batch Files on Windows OS Locally
To run the files **_run_models_batch_** or **_run_models_batch_uploaded_** that run all 3 model architectures using **_check_images.py_** on a Windows OS locally; you will need to use the files that end with the extention **_.bat_** instead of the extension **_.sh_**.  You will have also needed to have installed Anaconda on your computer.
### Directions:
* Open the **Anaconda Prompt** - either from typing **_Anaconda Prompt_** within the search bar and selecting it _or_ by clicking on it once it's found within the **Anaconda** folder of programs.
* Navigate to the _folder_ within the **Anaconda Prompt** that contains the _Project files_ including **_check_images.py_** and **_run_models_batch.bat_** using the command [_cd_](https://en.wikipedia.org/wiki/Cd_(command)).
* Type the command within the **Anaconda Prompt**:
```terminal
run_models_batch.bat
```
If instead you are working with the uploaded images , you will need to replace all instances of **_run_models_batch.bat_** from the _directions_ above with **_run_models_batch_uploaded.bat_**.
&nbsp;     
&nbsp;         

## Final Result of image classification can be referred from the below output files:
* alexnet_pet-images.txt
* resnet_pet-images.txt
* vgg_pet-images.txt
* alexnet_uploaded-images.txt
* resnet_uploaded-images.txt
* vgg_uploaded-images.txt
&nbsp;  
&nbsp;

## Questions addressed regarding classification of uploaded images:
1. Did the three model architectures classify the breed of dog in Dog_01.jpg to be the same breed? If not, report the differences in the classifications.
 
ResNet and VGG model classified the dog breed as "basset, basset hound" and AlexNet 
classified the dog image as of "basenji" breed. The image of the dog I have used is of an Indian Mongrel which is not in the dictionary, but visually the image of the dog resembles a bit closer to basenji.

2. Did each of the three model architectures classify the breed of dog in Dog_01.jpg to be the same breed of dog as that model architecture classified Dog_02.jpg? If not, report the differences in the classifications.

ResNet and AlexNet CNN model classified both the Dog_01.jpg and its flipped image Dog_02.jpg as "basset, basset hound" and "basenji" repectively. But the result provided by VGG model was a bit inconsistent, it classified Dog_01.jpg image as "basset, basset hound" and its flipped image Dog_02.jpg as "brittany spaniel".

3. Did the three model architectures correctly classify Animal_Name_01.jpg and Object_Name_01.jpg to not be dogs? If not, report the misclassifications.

Yes, all three models correctly classified the images of another animal and object as not dogs.

4. Based upon your answers for questions 1. - 3. above, select the model architecture that you feel did the best at classifying the four uploaded images. Describe why you selected that model architecture as the best on uploaded image classification.

AlexNet model identified the dog breed consistently for both the flipped images, as well as classified the coffee mug as cup and the bird as goose. That was pretty satisfactory as compared to the results provided by the other two models ResNet and VGG.
Though ResNet and VGG correctly identified the uploaded image of other object as coffee mug and bird as "redshank, tringa totanus" and "goose" respectively. But both misidentified the dog breed and VGG provided inconsistent results for the flipped images.
Thus taking into consideration of identification of all images of dog, bird and coffee mug, AlexNet fared well as the optimal model architecture for classifying closely all the uploaded images.
&nbsp;  
&nbsp;


## Cdiscount image classification challenge
In this project objective is building a model that automatically classifies the products based on their images.

### Set the virtual environnement 
In order to run the code, an virtual environment should be created and the library installed by running the following commands

**Create virtual environment** 
```
python3 -m venv env
```
**Activate the virtual environment**
```
source env/bin/activate
```
**Install Python libraries**
```
pip install -r requirements.txt
```

**Launch the Jupyter Lab environnement**
```
jupyter lab
```

### Prepare the data
Run the entire data_prep.ipynb notebook to prepare the data.  
This notebook will extract the data from the BSON file and will make a csv (data.csv) out of it.  
The constants should be set properly before running all the cells of the notebook.  
```python
# Constants
IMAGES_FOLDER = "data/images"
NUMBER_IMAGE_MINIMUM = 3
MAX_RECORD = 1000000
``` 
**IMAGES_FOLDER**: Folder where the images will be generated. Each category will have their own sub-folder. 

**NUMBER_IMAGE_MINIMUM**: Minimum number of images each category should have. If a category has less than NUMBER_IMAGE_MINIMUM, this category will not be used for the challenge. This is done to ensure each category has enough data. 

**MAX_RECORD**: The number of data record to be extract from the BSON file. Given the data is huge, it can be interesting not to use all the data. Set MAX_RECORD accordingly.

Run all the cells to have the images and the CSV generated in the data/ folder.
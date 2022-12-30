# scTransSort
scTransSort: Transformers for intelligent annotation of cell types by gene embeddings

The repository contains the source code for the paper scTransSort.
Due to github's limit on uploading file size, the trained model is over 500M, so I only uploaded the core code. If you need a trained model for your research, you can contact me by email s20070042@s.upc.edu.cn.

The neural network model is implemented using TensorFlow 2.4.0 and the code is written in python 3.6. 

## Quick Start

scTransSort accepts scRNA-seq data format: CSV
### 1. Prepare datasets

#### CSV format

Take an example of mouse datasets (MCA, https://figshare.com/articles/dataset/MCA_DGE_Data/5435866) analyzed in the manuscript.

```shell
read mouse_Brain753_data.csv
```

### 2. Preprocess input files
The preprocessed files generated in this step can be found in the uploaded data/example data set.csv
 
In preprocessing, parameters are used:

- **filetype** defines file type (CSV))  
- **geneSelectnum** selects a number of most variant genes. The default gene number is 2000
- **code** preprocessing.py

### 3. Run scTransSort

We take an example of an analysis in mouse_Brain753. Here we use parameters to demo purposes:

- **batch-size** defines batch-size of the cells for training.here we set as 64.
- **epoch** defines epochs in feature autoencoder, here we set as 100.
- **initial_lr** defines the Initial learning rate, here we set as 0.001.
- **weight_decay** defines the weight_decay, here we set as 1e-4.

If you want to reproduce results in the manuscript, please use default parameters. 


## Contributing

Souce code: [Github](https://github.com/jiaojiao-123/scTransSort)  
Author email: s20070042@s.upc.edu.cn
<br>
We are continuing adding new features. Bug reports or feature requests are welcome.
<br>

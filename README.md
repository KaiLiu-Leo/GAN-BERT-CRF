# GAN-BERT-CRF AND GAN-BiLSTM-CRF
#### This is an algorithms which use BERT-CRF as the generator and a CNN-based netword as the discrminator. This algorithms can use both annotated samples and unannotated samples to maximize NER(i.e Name entity recognition) performances. Furthermore, it plays a role of active learning, and can effectively identify sequence samples with error labels. Thus, it has three features. The paper for this algorithm would be published soon.
* NER: Use both unannotated and annotated samples to maximize NER performances.
* Active leanring: Use both ouputs of CRF layer and the discrimitor to select unannotated samples to be labeled.
* Identification of error labels: The discriminator outputs smaller score for the sequences with error labels

### DataSet
The DataSet should be in the format of two columns. The words are in the first column and labels are in the second column. Sample data is in the Data Directory.<br>
The china_medical_char_data_cleaned directory process Chinese data and medical_char_data_cleaned process English data. First, Download dataset and put dataset into these two directories based on languages. Then put your embedding files into these dicrectories and  run .sh file to produce training data, validation data, test data and embedding npz.
```
bash makefile.sh
```


.

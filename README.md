# SMC_Thesis_Trained_Neural_Networks
PyTorch-based trained Neural Networks for the Neural-Texture-Sound-Synthesis-with-physically-driven-continuous-controls project (https://github.com/Metiu-Metiu/Neural-Texture-Sound-Synthesis-with-physically-driven-continuous-controls).
Refer to the Neural-Texture-Sound-Synthesis-with-physically-driven-continuous-controls repo's documentation for deeper insights on synthetic-to-real Domain Adaptation.

The Neural Networks are trained on synthetic and real waterflow sound files datasets (https://github.com/Metiu-Metiu/Neural-Texture-Sound-synthesis---data-sets).

# Neural Networks for Synthesis Control Parameters extraction
These networks, following the SMC_Thesis repo pipeline, are trained on extracting Synthesis Control Parameters from synthetic Audio files, and then Domain-shifted (adapted) to the distribution of Real audio files datasets.

## 2D_CNN_SynthParamExtractor_June26_2023_Batch128_NoDropouts_10000Dataset_32kHz_3FCLayers_4ConvFilters_IncreasedNumberOfChannels_BatchNorm

See following example.

## 2D_CNN_SynthParamExtractor_June26_2023_Batch128_NoDropouts_10000Dataset_32kHz_3FCLayers_4ConvFilters_IncreasedNumberOfChannels_BatchNorm_DBScale

<b> Network trained on the Synthetic dataset </b>

- 2D_CNN_SynthParamExtractor_June26_2023_Batch128_NoDropouts_10000Dataset_32kHz_3FCLayers_4ConvFilters_IncreasedNumberOfChannels_BatchNorm_DBScale.pth

PyTorch-serialized Neural model summary of the Architecture designed for extracting Synthesis Control Parameters from synthetic Audio files.

- 2D_CNN_SynthParamExtractor_June26_2023_Batch128_NoDropouts_10000Dataset_32kHz_3FCLayers_4ConvFilters_IncreasedNumberOfChannels_BatchNorm_DBScale_ModelArchitectureSummary.txt

A text-based summary of the Architecture trained on extracting Synthesis Control Parameters from synthetic Audio files.

- 2D_CNN_SynthParamExtractor_June26_2023_Batch128_NoDropouts_10000Dataset_32kHz_3FCLayers_4ConvFilters_IncreasedNumberOfChannels_BatchNorm_DBScale_Checkpoint.json

The pre-trained model state -with best error among all training epochs- of the Architecture trained on extracting Synthesis Control Parameters from synthetic Audio files.

- 2D_CNN_SynthParamExtractor_June26_2023_Batch128_NoDropouts_10000Dataset_32kHz_3FCLayers_4ConvFilters_IncreasedNumberOfChannels_BatchNorm_DBScale_ConfigDict.json

The interface configuration dictionary used as settings, containing also some general information like the path of the dataset used. Paths are local, but you can easily deduce which dataset from https://github.com/Metiu-Metiu/Neural-Texture-Sound-Synthesis-with-physically-driven-continuous-controls has been used.

- 2D_CNN_SynthParamExtractor_June26_2023_Batch128_NoDropouts_10000Dataset_32kHz_3FCLayers_4ConvFilters_IncreasedNumberOfChannels_BatchNorm_DBScale_ExtractedAudioFilesLabels_SynthDataset.csv / .json

The labels extracted with the trained Network. Extraction is performed on the synthetic dataset.

- 2D_CNN_SynthParamExtractor_June26_2023_Batch128_NoDropouts_10000Dataset_32kHz_3FCLayers_4ConvFilters_IncreasedNumberOfChannels_BatchNorm_DBScale_ExtractedAudioFilesLabels_RealDataset.csv

The labels extracted with the trained Network. Extraction is performed on the real dataset WITHOUT DOMAIN ADAPTATION as a test.

<b> Network trained on both Synthetic and Real dataset </b>

- 2D_CNN_SynthParamExtractor_June26_2023_Batch128_NoDropouts_10000Dataset_32kHz_3FCLayers_4ConvFilters_IncreasedNumberOfChannels_BatchNorm_DBScale_FCLayers_SyntheticAndRealAudioClassifier.pth

PyTorch-serialized Neural model summary of the Synthetic/Real classifier.

- 2D_CNN_SynthParamExtractor_June26_2023_Batch128_NoDropouts_10000Dataset_32kHz_3FCLayers_4ConvFilters_IncreasedNumberOfChannels_BatchNorm_DBScale_FCLayers_SyntheticAndRealAudioClassifier_Checkpoint.json

The Synthetic/Real classifier Model state with best performance during training.

<b> Network trained on the Real dataset </b>

- 2D_CNN_SynthParamExtractor_June26_2023_Batch128_NoDropouts_10000Dataset_32kHz_3FCLayers_4ConvFilters_IncreasedNumberOfChannels_BatchNorm_DBScale_ConvLayers_TargetDomainAdaptation.pth

PyTorch-serialized Neural model summary of the Synthesis Control Parameter extractor for Real files.

- 2D_CNN_SynthParamExtractor_June26_2023_Batch128_NoDropouts_10000Dataset_32kHz_3FCLayers_4ConvFilters_IncreasedNumberOfChannels_BatchNorm_DBScale_ConvLayers_TargetDomainAdaptation_Checkpoint.json

Domain adaptation for the convolutional layers of the Synthesis Control Parameters Network pre-trained on Synthetic data. The adaptation is towards the Real dataset distribution.
This .json file represents the state of the .pth model, trained at its best performance.

- 2D_CNN_SynthParamExtractor_June26_2023_Batch128_NoDropouts_10000Dataset_32kHz_3FCLayers_4ConvFilters_IncreasedNumberOfChannels_BatchNorm_DBScale_ExtractedAudioFilesLabels__DA_RealDataset.csv / .json

The labels extracted from the Real dataset.

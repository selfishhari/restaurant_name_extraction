# resturant_name_extraction
NER

Experiments:
model	description	f1 score	Remarks
BART	Baseline Candidate Model	36.00%	
BART	Batchsize=10, stepsize 20	41.80%	
BART	Cosine schedule with warmup	40.80%	
BART	Ep:50, Stepsize:10, batchsize:10	46.00%	
BART	Augmentation: Add POS tags to input	25.90%	
BART	Augmentation: Swap restaurant names beween texts, 50epochs	42.55%	
BERT	Batchsize:2, Epochs:20	37.90%	
BERT	Batchsize:36,Epochs:100	40.60%	
BERT	Batchsize:2, Epochs:20, Dropout:30%	44.06%	Hidden dropouts were increased due to try to reduce overfitting
BERT	Augmentation: Delete restaurant names and try to predict blank	37.00%	Precision was low for model, basically because of false positives. Hence tried to enhance model’s power of predicting blank by adding additional data with restaurant names removed from text and labels
BERT	Augmentation: Swap restaurant names beween texts, 20epochs	46.50%	Swap restaurant names in training text to create more data
BERT	Augmentation: Swap restaurant names beween texts, 10epochs	51.40%	
BERT	Augmentation: Swap restaurant names beween texts 2 times, 10epochs	46.04%	
BERT	Augmentation: Swap restaurant names beween texts, 10epochs with dropouts	20.10%	

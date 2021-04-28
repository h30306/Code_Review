# Long Document Coreference with Bounded Memory Neural Networks

There are two parts of this code

1. meniton_model
2. auto_memory_model

## document_encoder/
Span-BERT for doc_encoder

###### base_encoder
###### independent
###### overlap

## mention_model/

## auto_memory_model/

#### main.py : 
1. line150, passing args to run Experiment function from experiment.py

#### experiment.py : 
1. line80, pick different type of bounded memory model from controller.utils.py
2. line151, forward data to get loss

#### controller/

###### utils
setting the different type of bounded memory, the detail is define in controller/

###### base_controller
1. line26,28, choosing different type of Encoder(Independent of Overlap)

functions:
* **get_span_embeddings**
* **get_mention_width_scores**
* **get_candidate_endpoints**
* **get_pred_mentions**

* **get_genre_embedding**
* **get_mention_embs_and_actions**
1. get encoded document from doc_encoder
2. 

###### lfm_controller
Inherit from BaseController

1. line14, LearnedFixedMemory from ./memory/lfm_memory.py

forward pipeline:
get_mention_embs_and_actions from base_controller

###### lru_controller
###### um_controller_no_ignore
###### um_controller



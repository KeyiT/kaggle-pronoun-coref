# Instruction

## Steps to generate results in the second stage:

#### Preprocessing
1. Set the 'test_df_path2' in 'coref-data-preprocessing.ipynb' to the location of the test set in the second stage.
2. Run 'coref-data-preprocessing.ipynb'

#### Run bert encoder
3. Set the 'df_path1' and 'df_path2' in 'generate-full-bert-embeddings.ipynb', fork-of-generate-full-large-bert-embeddings.ipynb, 'generate-full-large-bert2-embeddings.ipynb', 'generate-full-large-bert3-embeddings.ipynb' to the output location of 'coref-data-preprocessing.ipynb'.
4. Run 'generate-full-bert-embeddings.ipynb', fork-of-generate-full-large-bert-embeddings.ipynb, 'generate-full-large-bert2-embeddings.ipynb', 'generate-full-large-bert3-embeddings.ipynb'.

#### Run Neural Models
1. Set the 'df_path1' and 'df_path2' in all 'coref-by-*.ipynb' to the output location of 'coref-data-preprocessing.ipynb'.
2. Set the 'embed_folder' in 'coref-by-flat-pair-mlp-model-on-layerwise-bert.ipynb' and 'coref-by-mapped-mlp-model-on-layerwise-bert.ipynb' to the output location of 'generate-full-bert-embeddings.ipynb'.
3. Set the 'embed_folder' in 'coref-by-flat-pair-mlp-model-on-layerwise-lbert.ipynb' and 'coref-by-mapped-mlp-model-on-layerwise-lbert.ipynb' to the output location of 'fork-of-generate-full-large-bert-embeddings.ipynb'.
4. Set the 'embed_folder' in 'coref-by-flat-pair-mlp-model-on-layerwise-lbert2.ipynb' and 'coref-by-mapped-mlp-model-on-layerwise-lbert2.ipynb' to the output location of 'generate-full-large-bert2-embeddings.ipynb'.
5. Set the 'embed_folder' in 'coref-by-flat-pair-mlp-model-on-layerwise-lbert3.ipynb' and 'coref-by-mapped-mlp-model-on-layerwise-lbert3.ipynb' to the output location of 'generate-full-large-bert3-embeddings.ipynb'
6. Run all 'coref-by-*.ipynb'.

#### Run Ensemble Model and Generate Results for both submitted models.
1. Set the 'SUB_DATA_FOLDER' in 'ensemble-model.ipynb' to directory of the test set in the second stage.
2. Set other '*_DATA_FOLDER' in 'ensemble-model.ipynb' to the output directory of 'coref-by-*.ipynb' accordingly.
3. Run 'ensemble-model.ipynb'. "submission1.csv" is the result of model1. "submission2.csv" is the result of the model2.
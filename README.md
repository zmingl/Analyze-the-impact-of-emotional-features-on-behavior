# Analyze-the-impact-of-emotional-features-on-behavior
This project analyzed the impact of emotions(valence, arousal, dominance) on behavior using two datasets respectively.
1. one dataset is Werewolf-Among-Us(https://huggingface.co/datasets/bolinlai/Werewolf-Among-Us)
2. the other is debates occuring during the US 2020 presidential elections from Kaggle(https://www.kaggle.com/headsortails/us-election-2020-presidential-debates) and annotated "relation" by Rafael Mestre and Matt Ryan

Main method:
1. extract valence, arousal, dominance(vad) from audio by wav2vec2 model
2. standardize per speaker vad by z-score
3. build relation on first dataset (the second set has this column)
4. cluster_vad_profiles
5. compute_enrichment(lift =  P(strategy|cluster)/P(strategy)) and permutation pvals for lift
6. plot heatmap


# COMPSCI-645-Lab

Please find the preprocessed tsv file

https://drive.google.com/file/d/1fmD9vpe2vJa4rUJuCTjDBmNW0zJ1gOBH/view?usp=drive_link

Code reference:
import pandas as pd
df = pd.read_csv("title.basics.tsv", sep="\t", low_memory=False)
sample_df = df[df['tconst'].apply(lambda x: len(x)) == 9]
sample_df = sample_df[sample_df['primaryTitle'].str.match(r'^[A-Za-z0-9 ]+$') == True]
sample_df.shape # 3 million records around

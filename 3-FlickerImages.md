# 3.Flicker Image

```
import numpy as np
import pandas as pd
from matplotlib import pyplot as plt
db=pd.read_csv('BL-Flickr-Images-Book.csv')
db


db.columns


irrelevant_columns=['Edition Statement','Corporate Author','Corporate Contributors',
                    'Former owner','Engraver','Contributors','Issuance type','Shelfmarks']
                    
                    
                    db.drop(irrelevant_columns,inplace=True,axis=1)
db


db.set_index('Identifier', inplace=True)


db


import re def clean date(date):

match-re.search(r'\d(4)',str(date)) return int (match.group()) if match else np.nan



db['Date of Publication']=db['Date of Publication'].apply(clean_date)


db


pub=db['Place of Publication"]

london-pub.str.contains('London')

oxford-pub.str.contains('Oxford')

db['Place of Publication']=np.where (London, "London", np. where (oxford, "Oxford)


db

```

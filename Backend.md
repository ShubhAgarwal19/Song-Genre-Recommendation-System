import pandas as pd
df = pd.read_csv('music.csv')
df
import pandas as pd
df = pd.read_csv('music.csv')
df.shape
import pandas as pd
df = pd.read_csv('music.csv')
df.describe
import pandas as pd
df = pd.read_csv('music.csv')
df.values
import pandas as pd
music_data = pd.read_csv('music.csv')
music_data
import pandas as pd
music_data = pd.read_csv('music.csv')
X = music_data.drop(columns=['genre'])
X
import pandas as pd
music_data = pd.read_csv('music.csv')
X = music_data.drop(columns=['genre'])
Y = music_data['genre']
Y
import pandas as pd
from sklearn.tree import DecisionTreeClassifier

music_data = pd.read_csv('music.csv')
X = music_data.drop(columns=['genre'])
Y = music_data['genre']

model = DecisionTreeClassifier()
model.fit(X,Y)
predictions = model.predict([[16,1], [16,0], [16,2], [17,1], [17,0], [17,2], [18,1], [18,0], [18,2], [19,1], [19,0], [19,2], [20,2], [20,1],[20,0],[21,1],[21,0], [21,2],[22,1],[22,0], [22,2],[23,1],[23,0], [23,2],[24,1],[24,0], [24,2],[25,1], [25,0], [25,2],[26,0], [26,1], [26,2],[27,1],[27,0], [27,2],[28,1],[28,0], [28,2],[29,1],[29,0], [29,2],[30,1],[30,0], [30,2],[31,1],[31,0], [31,2],[32,1],[32,0], [32,2],[33,1],[33,0], [33,2],[34,1],[34,0], [34,2],[35,1],[35,0], [35,2],[36,1],[36,0], [36,2],[37,1],[37,0], [37,2],[38,1],[38,0], [38,2],[39,1],[39,0], [39,2],[40,1],[40,0], [40,2],[41,1],[41,0], [41,2],[42,1],[42,0], [42,2],[43,1],[43,0], [43,2],[44,1],[44,0], [44,2],[45,1],[45,0], [45,2],[46,1],[46,0], [46,2],[47,1],[47,0], [47,2],[48,1],[48,0], [48,2],[49,1],[49,0], [49,2],[50,1],[50,1], [50,2]])
predictions
import pandas as pd
from sklearn.tree import DecisionTreeClassifier
from sklearn import tree

music_data = pd.read_csv('music.csv')
X = music_data.drop(columns=['genre'])
Y = music_data['genre']

model = DecisionTreeClassifier()
model.fit(X,Y)

tree.export_graphviz(model, out_file='music-recommender.dot', feature_names=['age', 'gender'], 
                     class_names=sorted(Y.unique()), label='all', rounded=True, filled=True)

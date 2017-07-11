## Notebook Summary
### Load data and data preprocessing
- Load csv data with Pandas `pd.read_csv`.  
- Assinging column names (headers) with `pd.read_csv('Data/wdbc.data', names=headers)`.  
- One-hot-encoder of string labels (Diagnosis -> Diagnosis_B and Diagnosis_M) with `pd.get_dummies(df[df.columns])`.  
### Data visualization
- Plotting pair grid plot with Seaborn `sns.PairGrid(df, vars=df.columns[1:11], hue="Diagnosis_B", palette={0:'r', 1:'b'})`.  
- Set the diagnal content of the pair grid plot with `g.map_diag(plt.hist, edgecolor='w', linewidth='1')`.
- Seaborn scatterplot with categorization:
```python
X = pd.concat([df["texture_WS"], df["concave_points_WS"]], axis=1)
plt.scatter(X['texture_WS'][y==l],
X['concave_points_WS'][y==l],
c=c, label=l, marker=m, alpha=0.5)
```  
- 3D scatterplot with categorization:  
```python
fig = plt.figure(dpi=100)
ax = fig.add_subplot(111, projection='3d')

for l, c in zip(np.unique(df["Diagnosis_B"]), ['r','b']):
   ax.scatter(df["texture_ME"][df["Diagnosis_B"]==l], df["concave_points_ME"][df["Diagnosis_B"]==l], df["area_ME"][df["Diagnosis_B"]==l], c=c)
```  
### Data analysis
- Check if linearly separable with Kernel PCA of kernels: `'linear', 'poly', 'rbf', 'cosine'`.  
- Feature scaling (standardization).
- Classification with 2D and Multiple Dimension Perceptron.  
- Classification with Logistic Regression.  
- Classification with Nearest Neighbors, Linear SVM, RBF SVM, Gaussian Process, Decision Tree, Random Forest, Neural Net, AdaBoost, Naive Bayes, QDA  
- Model parameter fine tuning with Validation Curve

# Notebook Summary
## Load data and data preprocessing
- Load csv data with Pandas `pd.read_csv` and assigning headers with `names`.  
- Cleaning certain data values that are abnormal (too large or too small).  
- Data imputing with 
```
ip = Imputer(missing_values='NaN', strategy='mean', axis=0)
X = ip.fit_transform(df)
```  
- Merge two different df into one with `pd.concat([df, temp], axis=1)`.
## Data visualization
## Data analysis
- One-hot-encoding with `keras` `y_train_ohe = to_categorical(y_train)`.  
- Using `keras` to build multilayer perceptron algorithm. 
```
model = Sequential()
model.add(Dense(input_dim=X_train.shape[1],
                units=500,
                kernel_initializer='uniform',
               activation='elu'))
model.add(Dense(input_dim=100,
                units=50,
                kernel_initializer='uniform',
               activation='elu'))
model.add(Dense(input_dim=50,
                units=y_train_ohe.shape[1],
                kernel_initializer='uniform',
               activation='elu'))
sgd = SGD(lr=0.001, decay=1e-7, momentum=0.9)
```
- Compile -> Fit -> Predict
```
model.compile(loss='categorical_crossentropy', optimizer=sgd)

model.fit(X_train, 
          y_train_ohe, 
          epochs=50,
          batch_size=300,
          verbose=1,
          validation_split=0.1)
          
y_test_pred = model.predict_classes(X_test, verbose=0)
```

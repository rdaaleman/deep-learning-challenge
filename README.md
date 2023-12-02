# deep-learning-challenge


got support from BCS for the following code

nn_model = tf.keras.Sequential()
    ##tf.keras.layers.Dense(2, activation='relu', input_shape=(2,)))

# First hidden layer
nn_model.add(tf.keras.layers.Dense(units=80, activation="relu", input_dim=len(X_train[0])))

# Second hidden layer
nn_model.add(tf.keras.layers.Dense(units=30, activation="relu"))

# Output layer
nn_model.add(tf.keras.layers.Dense(units=1, activation="relu"))

# Check the structure of the model
nn_model.summary()

nn_model.compile(loss="binary_crossentropy", optimizer="adam", metrics=["accuracy"])
fit_model = nn_model.fit(X_train_scaled, y_train, epochs=100)

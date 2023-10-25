	ASL_Num

	Model-01:

		epochs = 50

		monitor = "val_accuracy"

		Leyers = model.add(Flatten())

			model.add(Dropout(0.25))
			
			model.add(Dense(64, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9291 (from val_accuracy = 0.96382)

		test_acc = 0.9500 -- 0.9406

		val_acc = 0.9474 -- 0.9441





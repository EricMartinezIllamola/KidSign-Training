	ASL_Num

	Model-03:

		epochs = 100

		monitor = "accuracy"

		Leyers = model.add(Flatten())

			model.add(Dropout(0.25))
			
			model.add(Dense(64, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(32, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9228

		test_acc = 0.9594 -- 0.9563

		val_acc = 0.9572 -- 0.9572





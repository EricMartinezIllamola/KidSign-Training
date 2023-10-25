	ASL_global

	Model-01:

		epochs = 125

		monitor = "accuracy"

		Leyers = model.add(Flatten())
			
			model.add(Dense(2048, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9724

		test_acc = 0.9393 -- 0.9357

		val_acc = 0.9609 -- 0.9618





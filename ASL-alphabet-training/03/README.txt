	ASL_abc

	Model-03:

		epochs = 125

		monitor = "accuracy"

		Leyers = model.add(Flatten())
			
			model.add(Dense(512, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9892

		test_acc = 0.9855 -- 0.9814

		val_acc = 0.9878 -- 0.9840





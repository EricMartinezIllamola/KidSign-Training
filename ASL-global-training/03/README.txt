	ASL_global

	Model-03:

		epochs = 200

		monitor = "accuracy"

		Leyers = model.add(Flatten())
			
			model.add(Dense(4096, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.35))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9823

		test_acc = 0.9301 -- 0.9412

		val_acc = 0.9628 -- 0.9552





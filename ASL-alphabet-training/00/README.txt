	ASL_abc

	Model-00:

		epochs = 25

		monitor = "accuracy"

		Leyers = model.add(Flatten())
			
			model.add(Dense(512, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9569

		test_acc = 0.9569 -- 0.9581

		val_acc = 0.9623 -- 0.9583





	ASL_abc

	Model-01:

		epochs = 25

		monitor = "accuracy"

		Leyers = model.add(Flatten())
			
			model.add(Dense(1024, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9583

		test_acc = 0.9586 -- 0.9583

		val_acc = 0.9620 -- 0.9603





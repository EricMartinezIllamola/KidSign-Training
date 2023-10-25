	ASL_global

	Model-00:

		epochs = 70

		monitor = "accuracy"

		Leyers = model.add(Flatten())
			
			model.add(Dense(512, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9491

		test_acc = 0.9136 -- 0.9210

		val_acc = 0.9408 -- 0.9342





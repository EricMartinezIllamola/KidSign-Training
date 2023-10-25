	ASL_abc

	Model-04:

		epochs = 50

		monitor = "val_accuracy"

		Leyers = model.add(Flatten())
			
			model.add(Dense(512, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9702 (from val_accuracy = 0.9798)

		test_acc = 0.9756 -- 0.9719

		val_acc = 0.9772 -- 0.9746





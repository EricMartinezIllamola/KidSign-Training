	ASL_global

	Model-02:

		epochs = 125

		monitor = "val_accuracy"

		Leyers = model.add(Flatten())
			
			model.add(Dense(2048, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9752 (from val_accuracy = 0.9637)

		test_acc = 0.9439 -- 0.9311

		val_acc = 0.9513 -- 0.9723





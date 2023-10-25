	ASL_abc

	Model-05:

		epochs = 125

		monitor = "val_accuracy"

		Leyers = model.add(Flatten())
			
			model.add(Dense(512, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9866 (from val_accuracy = 0.9870)

		test_acc = 0.9854 -- 0.9853

		val_acc = 0.9865 -- 0.9852





	ASL_Num

	Model-02:

		epochs = 100

		monitor = "accuracy"

		Leyers = model.add(Flatten())

			model.add(Dropout(0.25))
			
			model.add(Dense(64, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9722

		test_acc = 0.9719 -- 0.9688

		val_acc = 0.9671 -- 0.9671





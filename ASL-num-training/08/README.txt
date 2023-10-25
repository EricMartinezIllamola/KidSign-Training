	ASL_Num

	Model-08:

		epochs = 100

		monitor = "accuracy"

		Leyers = model.add(Flatten())
			
			model.add(Dense(2048, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9903

		test_acc = 0.9781 -- 0.9719

		val_acc = 0.9770 -- 0.9572





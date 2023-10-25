	ASL_Num

	Model-04:

		epochs = 100

		monitor = "accuracy"

		Leyers = model.add(Flatten())
			
			model.add(Dense(512, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9875

		test_acc = 0.9750 -- 0.9781

		val_acc = 0.9704 -- 0.9770





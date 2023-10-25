	ASL_Num

	Model-07:

		epochs = 100

		monitor = "val_accuracy"

		Leyers = model.add(Flatten())
			
			model.add(Dense(512, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9645 (from val_accuracy = 0.9836)

		test_acc = 0.9656 -- 0.9531

		val_acc = 0.9605 -- 0.9704





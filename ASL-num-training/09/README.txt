	ASL_Num

	Model-09:

		epochs = 100

		monitor = "accuracy"

		Leyers = model.add(Flatten())
			
			model.add(Dense(4096, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9896

		test_acc = 0.9781 -- 0.9688

		val_acc = 0.9770 -- 0.9671





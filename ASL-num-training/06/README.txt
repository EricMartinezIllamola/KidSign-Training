	ASL_Num

	Model-06:

		epochs = 100

		monitor = "accuracy"

		Leyers = model.add(Flatten())
			
			model.add(Dense(1024, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9889

		test_acc = 0.9688 -- 0.9719

		val_acc = 0.9836 -- 0.9770





	ASL_abc

	Model-02:

		epochs = 50

		monitor = "accuracy"

		Leyers = model.add(Flatten())
			
			model.add(Dense(512, kernel_regularizer=regularizers.l2(0.01), activation = 'relu'))
			
			model.add(Dropout(0.25))

			model.add(Dense(num_classes, activation = 'softmax'))


	Results:

		train_acc = 0.9766

		test_acc = 0.9682 -- 0.9774

		val_acc = 0.9729 -- 0.9780





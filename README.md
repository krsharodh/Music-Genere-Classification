## Music Genre Prediction Guide:

	### Overview:
		Music Genre Classification is an essential component of the Music Information Retrieval (MIR) system and has been drawing a substantial amount of attention with the advent of online music streaming services. The key objective of this research is to analyse the performance of Audio, Metadata, and Lyrical features individually on different Machine Learning models to classify the genre of music.

	### Requirements:

		- *pandas==0.22.0*
		- *scipy==0.19.0*
		- *numpy==1.12.1*

	**Note:** *The running of the algorithm might take more time as more complex algorithms are run for several times to achieve to acheive optimal results. *
	
	### Time reuired to run:
		- Model + Graph: 40 mins
		- Model: 15 mins
		
		*The tests are performed in a 10th i5 processor with 8gb RAM*

	### Files Required to Run:

		1. Music Genre Prediction.ipynb,
		2. train_features.csv,
		3. train_labels.csv,
		4. valid_features.csv,
		5. valid_labels.csv,
		6. test_features.csv

	### Steps to run the Music Genre Classification:

		1. create instance for Music_Genre_Prediction (already created in notebook)
		2. run Music_Genre_Prediction.main() with created instance

	### Internals

		##### Class Music_Genre_Prediction

			Contains methods used for music genre prediction

		##### Methods:

			1. *main()*
				Runs the music genre prediction classification across all features and models.
				
				Parameters:
				
					- *learning_curves*:
						If true shows learning curves for best predicting features across all models
						
					- *export_test_label*:
						If true exports test labels with best model
						
			2. *train()*
				Accepts train features and labels to create different machine learning models
				
				Parameters:
				
					- *x_train*:
						Training Features
					
					- *y_train*:
						Train Labels
						
					- *mnb*:
						If true performs multinomial naive bayes instead of gaussian naive bayes.
						
			3. *predict()*
				Accepts test features to predict its labels using model created in training phase
				
				Parameters:
				
					- *x_test*:
						Test Features
					
					- *mnb*:
						If true performs multinomial naive bayes instead of gaussian naive bayes.
						
			4. *evaluate()*
				Accepts features and labels of both training and test to evaluate the performance
				
				Parameters:
				
					- *x_train*:
						Training Features
					
					- *y_train*:
						Train Labels
					
					- *x_test*:
						Test Features
					
					- *y_test*:
						Test Labels
					
					- *mnb*:
						If true performs multinomial naive bayes instead of gaussian naive bayes.
						
			5. *train_predict_evaluate()*
				Performs training, prediction, and evaluation of all algorithms.
				
				parameters:
				
					- *x_train*:
						Training Features
					
					- *y_train*:
						Train Labels
					
					- *x_test*:
						Test Features
					
					- *y_test*:
						Test Labels
					
					- *mnb*:
						If true performs multinomial naive bayes instead of gaussian naive bayes.
						
						
			6. *draw_curves()*
				Accepts estimator model, train features, train labels, y axis limits, cross validation settings, number of jobs, and train_sizes to draw the learning curves for best predicting feature across all models
						
				Parameters:
				
					- *estimator*:
						Model
					
					- *X*:
						Training Features
					
					- *y*:
						Train Labels

					- *ylim*:
						Y axes limits

					- *cv*:
						A shuffle split object
									
					- *n_jobs*:
						number of jobs

					- *train_sizes*:
						training sizes
						
			7. *export_test_labels()*
				Exports the labels predicted as *out.csv* for test features in csv format using best model and feature of all 
				
				Parameters:
					Nil
			
			
# Conversion of python keras model to TFJS compatible form
Python is the most preferred language for training models in keras. So, it is obvious that most of the models we find on internet are in .h5 or similar form. So, what if we wanted a model to run on browser? Thankfully, there is a version of Tensorflow for JavaScript a.k.a tensorflow.js. It is important that we change .h5 model to the tfjs compatible form. Let's do it.

## Files in Repo:
1. ModelCreator.ipynb : A python notebook to train and save the keras model in .h5 form. It is a mnist image classifier.
2.ModelConverter.ipynb : A python notebook to convert the .h5 model to tfjs compatible form.
3. Index.html : HTML file to finally load the converted model in browser.

The folders graph_model and layers_model are the folders to save the converted model.

# Difference between tfjs graph model and tfjs layers model
tfjs layers model: This kind of model can be used for both training and predicting. So, using this model would be optimum if you plan to re-train your model in future and also use it for prediction in present time as well.

tfjs graph model: As opposed to tfjs layers model, this kind of model only supports prediction. So, it's best use case would be when you are sure you wouldn't retrain the model in future. It's advantage is it would be light as it wouldn't have to save the configuration for training.

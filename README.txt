1. dplyr is used for cleaning the data. 

2. Steps 

	1) load test data(subject_test.txt,y_test.txt,X_test.txt) into R using read.table
	2) load train data(subject_train.txt,y_train.txt,X_train.txt) into R using read.table
	3) name subject and activity label for both test and train data
	4) merge test and train using cbind 
	5) grepl is used for get the mean and std from merge data
	6) combine mean and std using cbind 
	7) merge activity and label 
	8) label the X data using names from features.txt
	9) group_by used to group subject and label
	10) summarize_each is used to apply mean 
	
3. Varibales 

    testS --- subject for test 
	testY --- label for test
	testX --- data for test 
	
	trainS --- subject for train
	trainY --- label for train 
	trainX --- data for train 
	
	feature --- X colnames loaded from feature.txt 
	
	comS  --- subject for both test and train
	comY  ---  label for both test and train 
	comX  ---  data for both test and train 
	
	com ---  comS + comY + comX  
	
	mean --- select colnames contains "mean" from com
	std  --- select colnames contains "std" from com 
	
	mergems --- mean + std
	
	mergeac --- comY +label(from activity_labels.txt) to get the names for each activity 
	
	merged --- mergems + mergeac 
	
	test   --- group_by applied for both subject and label
	

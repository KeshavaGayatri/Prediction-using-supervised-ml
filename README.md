# Prediction-using-supervised-ml
#Solution OF TASK 1 IN R Programming  only commands
url<-"https://raw.githubusercontent.com/AdiPersonalWorks/Random/master/student_scores%20-%20student_scores.csv"
data<-read.csv(url)
summary(data)
head(data)
str(data)
any(is.na(data))
x<-data$Hours,y<-data$Scores
plot(x~y)
abline(lm(x~y))
model<-lm(y~x)
Score.prediction<-predict(model,data)
print(Score.prediction)
obj<-data.frame(x=9.25)
prediction<-predict(model,obj)
print(prediction)


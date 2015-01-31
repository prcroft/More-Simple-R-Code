# More-Simple-R-Code
another attempt to upload R Code
Simple code to demonstrate the steps required to produce a median using a dataset of heights, as shown in Chapter 2 of Machine Learnign for Hackers
> heights.weights<-read.csv("http://clic.cimec.unitn.it/massimo/Teach/CMDA/Labs/Lab2_Linear_Regression/01_heights_weights_genders.csv", header=TRUE, sep=',')
> heights<-with(heights.weights, Height)
> my.median<-function(x) {
  + sorted.x<-sort(x)
  + if (length(x) %% 2 == 0)
    + {
      + indices<-c(length(x)/2, length(x)/2 +1)
      + return(mean(sorted.x[indices]))
      + }
  + else
    + {}
  + {
    + index<-ceiling(length(x)/2)
    + return(sorted.x[index])
    + }
  + }
> my.median(heights)

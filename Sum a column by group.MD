Using aggregate:

x <- data.frame(Category=factor(c("First", "First", "First", "Second",
                                  "Third", "Third", "Second")), 
                Frequency=c(10,15,5,2,14,20,3))
aggregate(x$Frequency, by=list(Category=x$Category), FUN=sum)
  Category  x
1    First 30
2   Second  5
3    Third 34
or tapply:

tapply(x$Frequency, x$Category, FUN=sum)
 First Second  Third 
    30      5     34
    
    

// group by two vars
aggregate(value ~ x1 + x2, data = dat, FUN = 'sum')

## aggregate two functions
aggregate(. ~ id1+id2,data = x,FUN=function(x) c(mn =mean(x), n=length(x) ) )

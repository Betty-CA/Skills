Use grep() to search for the string you're matching. Here's an example with the mtcars dataset, where we are matching all rows where the row names includes "Merc":

mtcars[grep("Merc", rownames(mtcars)), ]

irisSubset <- iris[grep("osa", iris$Species), ]
head(irisSubset)


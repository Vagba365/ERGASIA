mtcars
dat=mtcars[,2:4]
pmatrxix=scale(dat)
d=dist(pmatrxix)
c=hclust(d,method="ward.D2")
plot(c)
rect.hclust(c,k=3)
groups<-cutree(c,k=3)
table(mtcars$cyl,groups)

# openpgm-masaike
openpgm+masaike

library(pixmap)
#mrsh1 = read.pnm('1.pgm')
#plot(mrsh1)
#locator()

blurpart = function(img, rows, cols, q){
    lrows = length(rows)
    lcols = length(cols)
    newimg = img
    randomnoise = matrix(nrow = lrows, ncol = lcols, runif(lrows*lcols))
    newimg@grey[rows,cols] = (1-q)*img@grey[rows,cols] + q*randomnoise
    return(newimg)
}

#mrsh3 = blurpart(mrsh1, (nrow(mrsh1@grey) - y坐标) = 84:163, x坐标 = 135:177, q = 0.65)
#plot(mrsh3)

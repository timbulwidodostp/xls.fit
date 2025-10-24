# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Fitting an eXtreme Least Squares Model Use xls.fit (XLS) With (In) R Software
install.packages("XLS")
library(XLS)
xls.fit = read.csv("https://raw.githubusercontent.com/timbulwidodostp/xls.fit/main/xls.fit/xls.fit.csv",sep = ";")
# Estimation Fitting an eXtreme Least Squares Model Use xls.fit (XLS) With (In) R Software
ordered_xls.fit <- xls.fit[with(xls.fit, order(Month, Day)), ]
xls.fit <- xls.fit(Ozone ~ Solar.R + Wind + Temp, na.omit(ordered_xls.fit), error_weights = c(0.4,0.3,0.2,0.1), error_ahead_level = 4)
summary(xls.fit)
# Fitting an eXtreme Least Squares Model Use xls.fit (XLS) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished
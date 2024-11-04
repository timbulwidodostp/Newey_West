# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Newey-West HAC Covariance Matrix Estimation Use NeweyWest (sandwich) With (In) R Software
install.packages("sandwich")
install.packages("lm")
library("sandwich")
Newey_West = read.csv("https://raw.githubusercontent.com/timbulwidodostp/Newey_West/main/Newey_West/Newey_West.csv",sep = ";")
# Estimation Newey-West HAC Covariance Matrix Estimation Use NeweyWest With (In) R Software
Newey_West <- lm(RealInv ~ RealGNP + RealInt, data = Newey_West)
## Newey & West (1994) compute this type of estimator
NeweyWest(Newey_West)
## The Newey & West (1987) estimator requires specification
## of the lag and suppression of prewhitening
NeweyWest(Newey_West, lag = 4, prewhite = FALSE)
## bwNeweyWest() can also be passed to kernHAC(), e.g.
## for the quadratic spectral kernel
kernHAC(Newey_West, bw = bwNeweyWest)
# Newey-West HAC Covariance Matrix Estimation Use NeweyWest With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished
```r
library(ggplot2)
library(readxl)
library(plotly)
library(dplyr)
RPNdata <- read_xlsx("/Users/raulgonzalezandreu/Desktop/Rstudio/3P project OOT/ClasificacionRPN.xlsx")
fig <- ggplot(data=RPNdata, aes(x= MODF, y= RPN , fill= TIPO)) + 
  geom_bar(stat="identity", position=position_dodge()) +
  scale_fill_manual(values=c("#E67E22", "#2ECC71"))+
  ggtitle("Categorización del riesgo")+
  xlab("Modo de fallo")+
  ylab("RPN")+
  theme_classic()
fig1 <- ggplotly(fig)
fig1
´´´

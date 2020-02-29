---
name: Time Series
permalink: r/time-series/
description: How to plot date and time in R. An example of a time series plot with the POSIXct and Sys.Date classes.
layout: base
thumbnail: thumbnail/time-series.jpg
language: r
page_type: example_index
display_as: financial
order: 1
output:
  html_document:
    keep_md: true
---


### Dates


```r
library(plotly)
today <- Sys.Date()
tm <- seq(0, 600, by = 10)
x <- today - tm
y <- rnorm(length(x))
fig <- plot_ly(x = ~x, y = ~y, mode = 'lines', text = paste(tm, "days from today"))

fig
```

<div id="htmlwidget-c1e5d7e6d50ee35eadd8" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-c1e5d7e6d50ee35eadd8">{"x":{"visdat":{"1fea38d7375d":["function () ","plotlyVisDat"]},"cur_data":"1fea38d7375d","attrs":{"1fea38d7375d":{"x":{},"y":{},"mode":"lines","text":["0 days from today","10 days from today","20 days from today","30 days from today","40 days from today","50 days from today","60 days from today","70 days from today","80 days from today","90 days from today","100 days from today","110 days from today","120 days from today","130 days from today","140 days from today","150 days from today","160 days from today","170 days from today","180 days from today","190 days from today","200 days from today","210 days from today","220 days from today","230 days from today","240 days from today","250 days from today","260 days from today","270 days from today","280 days from today","290 days from today","300 days from today","310 days from today","320 days from today","330 days from today","340 days from today","350 days from today","360 days from today","370 days from today","380 days from today","390 days from today","400 days from today","410 days from today","420 days from today","430 days from today","440 days from today","450 days from today","460 days from today","470 days from today","480 days from today","490 days from today","500 days from today","510 days from today","520 days from today","530 days from today","540 days from today","550 days from today","560 days from today","570 days from today","580 days from today","590 days from today","600 days from today"],"alpha_stroke":1,"sizes":[10,100],"spans":[1,20]}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"xaxis":{"domain":[0,1],"automargin":true,"title":"x"},"yaxis":{"domain":[0,1],"automargin":true,"title":"y"},"hovermode":"closest","showlegend":false},"source":"A","config":{"showSendToCloud":false},"data":[{"x":["2020-02-29","2020-02-19","2020-02-09","2020-01-30","2020-01-20","2020-01-10","2019-12-31","2019-12-21","2019-12-11","2019-12-01","2019-11-21","2019-11-11","2019-11-01","2019-10-22","2019-10-12","2019-10-02","2019-09-22","2019-09-12","2019-09-02","2019-08-23","2019-08-13","2019-08-03","2019-07-24","2019-07-14","2019-07-04","2019-06-24","2019-06-14","2019-06-04","2019-05-25","2019-05-15","2019-05-05","2019-04-25","2019-04-15","2019-04-05","2019-03-26","2019-03-16","2019-03-06","2019-02-24","2019-02-14","2019-02-04","2019-01-25","2019-01-15","2019-01-05","2018-12-26","2018-12-16","2018-12-06","2018-11-26","2018-11-16","2018-11-06","2018-10-27","2018-10-17","2018-10-07","2018-09-27","2018-09-17","2018-09-07","2018-08-28","2018-08-18","2018-08-08","2018-07-29","2018-07-19","2018-07-09"],"y":[1.09598979326549,-1.21308711209059,3.64979315397556,-1.064009271873,-1.04335891625627,0.778835457151761,-0.318167975162608,0.057415103657444,2.01861742705818,-0.942586945834033,-0.746686486469039,-1.41615671015503,0.596667854902777,-0.382928720126894,-1.08698858788695,-0.520197204348525,0.709310710103139,1.36121498734355,1.10113226630945,-0.0299725769332979,-0.361317428487045,-2.00183618422027,-0.720247662083072,-0.198186752533309,2.1531323108235,0.941753742478901,0.609972418757658,1.61804517879247,-0.680243851408085,1.45864683958929,-0.870424785732979,-0.135533675095085,0.547679069990527,-0.071323866164499,-0.620212849375751,-1.58147801943854,0.32285245075057,0.388651478114908,2.37078402884287,1.6772330995218,-0.835991610276454,-0.32459801606554,-1.21520925698241,-0.708146347055762,1.33751838568085,-1.36425382255853,0.085068502264338,2.32601382751516,-1.73029954259618,0.568124214975552,-1.71647765672798,0.780120211321443,0.500383764079676,-1.77487820319122,0.408058202374812,-1.01883499317122,0.295270166688687,-2.17167481544657,1.43581124376114,0.519202757306014,0.271411414561144],"mode":"lines","text":["0 days from today","10 days from today","20 days from today","30 days from today","40 days from today","50 days from today","60 days from today","70 days from today","80 days from today","90 days from today","100 days from today","110 days from today","120 days from today","130 days from today","140 days from today","150 days from today","160 days from today","170 days from today","180 days from today","190 days from today","200 days from today","210 days from today","220 days from today","230 days from today","240 days from today","250 days from today","260 days from today","270 days from today","280 days from today","290 days from today","300 days from today","310 days from today","320 days from today","330 days from today","340 days from today","350 days from today","360 days from today","370 days from today","380 days from today","390 days from today","400 days from today","410 days from today","420 days from today","430 days from today","440 days from today","450 days from today","460 days from today","470 days from today","480 days from today","490 days from today","500 days from today","510 days from today","520 days from today","530 days from today","540 days from today","550 days from today","560 days from today","570 days from today","580 days from today","590 days from today","600 days from today"],"type":"scatter","marker":{"color":"rgba(31,119,180,1)","line":{"color":"rgba(31,119,180,1)"}},"error_y":{"color":"rgba(31,119,180,1)"},"error_x":{"color":"rgba(31,119,180,1)"},"line":{"color":"rgba(31,119,180,1)"},"xaxis":"x","yaxis":"y","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

### POSIXlt date time class with timezone


```r
library(plotly)
now_lt <- as.POSIXlt(Sys.time(), tz = "GMT")
tm <- seq(0, 600, by = 10)
x <- now_lt - tm
y <- rnorm(length(x))
fig <- plot_ly(x = ~x, y = ~y, mode = 'lines', text = paste(tm, "seconds from now in GMT"))

fig
```

<div id="htmlwidget-b3639a6e03523b4a52c2" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-b3639a6e03523b4a52c2">{"x":{"visdat":{"1fea2f1c27b2":["function () ","plotlyVisDat"]},"cur_data":"1fea2f1c27b2","attrs":{"1fea2f1c27b2":{"x":{},"y":{},"mode":"lines","text":["0 seconds from now in GMT","10 seconds from now in GMT","20 seconds from now in GMT","30 seconds from now in GMT","40 seconds from now in GMT","50 seconds from now in GMT","60 seconds from now in GMT","70 seconds from now in GMT","80 seconds from now in GMT","90 seconds from now in GMT","100 seconds from now in GMT","110 seconds from now in GMT","120 seconds from now in GMT","130 seconds from now in GMT","140 seconds from now in GMT","150 seconds from now in GMT","160 seconds from now in GMT","170 seconds from now in GMT","180 seconds from now in GMT","190 seconds from now in GMT","200 seconds from now in GMT","210 seconds from now in GMT","220 seconds from now in GMT","230 seconds from now in GMT","240 seconds from now in GMT","250 seconds from now in GMT","260 seconds from now in GMT","270 seconds from now in GMT","280 seconds from now in GMT","290 seconds from now in GMT","300 seconds from now in GMT","310 seconds from now in GMT","320 seconds from now in GMT","330 seconds from now in GMT","340 seconds from now in GMT","350 seconds from now in GMT","360 seconds from now in GMT","370 seconds from now in GMT","380 seconds from now in GMT","390 seconds from now in GMT","400 seconds from now in GMT","410 seconds from now in GMT","420 seconds from now in GMT","430 seconds from now in GMT","440 seconds from now in GMT","450 seconds from now in GMT","460 seconds from now in GMT","470 seconds from now in GMT","480 seconds from now in GMT","490 seconds from now in GMT","500 seconds from now in GMT","510 seconds from now in GMT","520 seconds from now in GMT","530 seconds from now in GMT","540 seconds from now in GMT","550 seconds from now in GMT","560 seconds from now in GMT","570 seconds from now in GMT","580 seconds from now in GMT","590 seconds from now in GMT","600 seconds from now in GMT"],"alpha_stroke":1,"sizes":[10,100],"spans":[1,20]}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"xaxis":{"domain":[0,1],"automargin":true,"title":"x"},"yaxis":{"domain":[0,1],"automargin":true,"title":"y"},"hovermode":"closest","showlegend":false},"source":"A","config":{"showSendToCloud":false},"data":[{"x":["2020-02-29 00:29:09","2020-02-29 00:28:59","2020-02-29 00:28:49","2020-02-29 00:28:39","2020-02-29 00:28:29","2020-02-29 00:28:19","2020-02-29 00:28:09","2020-02-29 00:27:59","2020-02-29 00:27:49","2020-02-29 00:27:39","2020-02-29 00:27:29","2020-02-29 00:27:19","2020-02-29 00:27:09","2020-02-29 00:26:59","2020-02-29 00:26:49","2020-02-29 00:26:39","2020-02-29 00:26:29","2020-02-29 00:26:19","2020-02-29 00:26:09","2020-02-29 00:25:59","2020-02-29 00:25:49","2020-02-29 00:25:39","2020-02-29 00:25:29","2020-02-29 00:25:19","2020-02-29 00:25:09","2020-02-29 00:24:59","2020-02-29 00:24:49","2020-02-29 00:24:39","2020-02-29 00:24:29","2020-02-29 00:24:19","2020-02-29 00:24:09","2020-02-29 00:23:59","2020-02-29 00:23:49","2020-02-29 00:23:39","2020-02-29 00:23:29","2020-02-29 00:23:19","2020-02-29 00:23:09","2020-02-29 00:22:59","2020-02-29 00:22:49","2020-02-29 00:22:39","2020-02-29 00:22:29","2020-02-29 00:22:19","2020-02-29 00:22:09","2020-02-29 00:21:59","2020-02-29 00:21:49","2020-02-29 00:21:39","2020-02-29 00:21:29","2020-02-29 00:21:19","2020-02-29 00:21:09","2020-02-29 00:20:59","2020-02-29 00:20:49","2020-02-29 00:20:39","2020-02-29 00:20:29","2020-02-29 00:20:19","2020-02-29 00:20:09","2020-02-29 00:19:59","2020-02-29 00:19:49","2020-02-29 00:19:39","2020-02-29 00:19:29","2020-02-29 00:19:19","2020-02-29 00:19:09"],"y":[-0.629003262527168,-1.60660526718325,-0.299812870184594,-0.00110270610512844,-0.470329851157893,-1.13713046710803,0.253392102741006,-0.662096765422828,-0.974229511298777,-0.897007570586421,0.905599938683448,0.281873169269474,-0.697333361851926,-1.21146194930309,-0.797735474006898,1.16518229179707,-0.0951443394379083,-1.13251986788228,1.38972676896198,-0.434583089754859,0.487967118163356,-1.48812038573872,-0.59324451090425,-0.990533300212156,-1.43001035514892,0.161809509541378,-0.891735896711542,1.89592202153102,-0.276450640555644,0.311052309141649,0.279573075540109,1.16545517695382,2.06475307061621,-0.0296992225223732,-1.43414179115932,-0.492863844156734,-1.58665069834335,0.132950596591119,-0.969986789799892,0.0397097979995617,1.51966627941976,-0.502326843876027,-1.24674724954561,-0.248375448742934,-0.85458402018612,1.37429939751865,-0.287676069662971,0.0258050373343188,-0.803811305053497,0.810461476306412,-0.59458629438646,0.925045502750339,-0.598066614551033,-1.86900972592671,-0.914230808749406,-0.162773543373617,-0.408148853620936,-0.366862252125907,-1.15055273876792,0.225161002896418,0.822687329633492],"mode":"lines","text":["0 seconds from now in GMT","10 seconds from now in GMT","20 seconds from now in GMT","30 seconds from now in GMT","40 seconds from now in GMT","50 seconds from now in GMT","60 seconds from now in GMT","70 seconds from now in GMT","80 seconds from now in GMT","90 seconds from now in GMT","100 seconds from now in GMT","110 seconds from now in GMT","120 seconds from now in GMT","130 seconds from now in GMT","140 seconds from now in GMT","150 seconds from now in GMT","160 seconds from now in GMT","170 seconds from now in GMT","180 seconds from now in GMT","190 seconds from now in GMT","200 seconds from now in GMT","210 seconds from now in GMT","220 seconds from now in GMT","230 seconds from now in GMT","240 seconds from now in GMT","250 seconds from now in GMT","260 seconds from now in GMT","270 seconds from now in GMT","280 seconds from now in GMT","290 seconds from now in GMT","300 seconds from now in GMT","310 seconds from now in GMT","320 seconds from now in GMT","330 seconds from now in GMT","340 seconds from now in GMT","350 seconds from now in GMT","360 seconds from now in GMT","370 seconds from now in GMT","380 seconds from now in GMT","390 seconds from now in GMT","400 seconds from now in GMT","410 seconds from now in GMT","420 seconds from now in GMT","430 seconds from now in GMT","440 seconds from now in GMT","450 seconds from now in GMT","460 seconds from now in GMT","470 seconds from now in GMT","480 seconds from now in GMT","490 seconds from now in GMT","500 seconds from now in GMT","510 seconds from now in GMT","520 seconds from now in GMT","530 seconds from now in GMT","540 seconds from now in GMT","550 seconds from now in GMT","560 seconds from now in GMT","570 seconds from now in GMT","580 seconds from now in GMT","590 seconds from now in GMT","600 seconds from now in GMT"],"type":"scatter","marker":{"color":"rgba(31,119,180,1)","line":{"color":"rgba(31,119,180,1)"}},"error_y":{"color":"rgba(31,119,180,1)"},"error_x":{"color":"rgba(31,119,180,1)"},"line":{"color":"rgba(31,119,180,1)"},"xaxis":"x","yaxis":"y","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

### POSIXct date time class without timezone


```r
library(plotly)
now_ct <- as.POSIXct(Sys.time())
tm <- seq(0, 600, by = 10)
x <- now_ct - tm
y <- rnorm(length(x))
fig <- plot_ly(x = ~x, y = ~y, mode = 'lines', text = paste(tm, "seconds from now in", Sys.timezone()))

fig
```

<div id="htmlwidget-422d6937277be4ba67c6" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-422d6937277be4ba67c6">{"x":{"visdat":{"1fea6b21d7ea":["function () ","plotlyVisDat"]},"cur_data":"1fea6b21d7ea","attrs":{"1fea6b21d7ea":{"x":{},"y":{},"mode":"lines","text":["0 seconds from now in Etc/UTC","10 seconds from now in Etc/UTC","20 seconds from now in Etc/UTC","30 seconds from now in Etc/UTC","40 seconds from now in Etc/UTC","50 seconds from now in Etc/UTC","60 seconds from now in Etc/UTC","70 seconds from now in Etc/UTC","80 seconds from now in Etc/UTC","90 seconds from now in Etc/UTC","100 seconds from now in Etc/UTC","110 seconds from now in Etc/UTC","120 seconds from now in Etc/UTC","130 seconds from now in Etc/UTC","140 seconds from now in Etc/UTC","150 seconds from now in Etc/UTC","160 seconds from now in Etc/UTC","170 seconds from now in Etc/UTC","180 seconds from now in Etc/UTC","190 seconds from now in Etc/UTC","200 seconds from now in Etc/UTC","210 seconds from now in Etc/UTC","220 seconds from now in Etc/UTC","230 seconds from now in Etc/UTC","240 seconds from now in Etc/UTC","250 seconds from now in Etc/UTC","260 seconds from now in Etc/UTC","270 seconds from now in Etc/UTC","280 seconds from now in Etc/UTC","290 seconds from now in Etc/UTC","300 seconds from now in Etc/UTC","310 seconds from now in Etc/UTC","320 seconds from now in Etc/UTC","330 seconds from now in Etc/UTC","340 seconds from now in Etc/UTC","350 seconds from now in Etc/UTC","360 seconds from now in Etc/UTC","370 seconds from now in Etc/UTC","380 seconds from now in Etc/UTC","390 seconds from now in Etc/UTC","400 seconds from now in Etc/UTC","410 seconds from now in Etc/UTC","420 seconds from now in Etc/UTC","430 seconds from now in Etc/UTC","440 seconds from now in Etc/UTC","450 seconds from now in Etc/UTC","460 seconds from now in Etc/UTC","470 seconds from now in Etc/UTC","480 seconds from now in Etc/UTC","490 seconds from now in Etc/UTC","500 seconds from now in Etc/UTC","510 seconds from now in Etc/UTC","520 seconds from now in Etc/UTC","530 seconds from now in Etc/UTC","540 seconds from now in Etc/UTC","550 seconds from now in Etc/UTC","560 seconds from now in Etc/UTC","570 seconds from now in Etc/UTC","580 seconds from now in Etc/UTC","590 seconds from now in Etc/UTC","600 seconds from now in Etc/UTC"],"alpha_stroke":1,"sizes":[10,100],"spans":[1,20]}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"xaxis":{"domain":[0,1],"automargin":true,"title":"x"},"yaxis":{"domain":[0,1],"automargin":true,"title":"y"},"hovermode":"closest","showlegend":false},"source":"A","config":{"showSendToCloud":false},"data":[{"x":["2020-02-29 00:29:09","2020-02-29 00:28:59","2020-02-29 00:28:49","2020-02-29 00:28:39","2020-02-29 00:28:29","2020-02-29 00:28:19","2020-02-29 00:28:09","2020-02-29 00:27:59","2020-02-29 00:27:49","2020-02-29 00:27:39","2020-02-29 00:27:29","2020-02-29 00:27:19","2020-02-29 00:27:09","2020-02-29 00:26:59","2020-02-29 00:26:49","2020-02-29 00:26:39","2020-02-29 00:26:29","2020-02-29 00:26:19","2020-02-29 00:26:09","2020-02-29 00:25:59","2020-02-29 00:25:49","2020-02-29 00:25:39","2020-02-29 00:25:29","2020-02-29 00:25:19","2020-02-29 00:25:09","2020-02-29 00:24:59","2020-02-29 00:24:49","2020-02-29 00:24:39","2020-02-29 00:24:29","2020-02-29 00:24:19","2020-02-29 00:24:09","2020-02-29 00:23:59","2020-02-29 00:23:49","2020-02-29 00:23:39","2020-02-29 00:23:29","2020-02-29 00:23:19","2020-02-29 00:23:09","2020-02-29 00:22:59","2020-02-29 00:22:49","2020-02-29 00:22:39","2020-02-29 00:22:29","2020-02-29 00:22:19","2020-02-29 00:22:09","2020-02-29 00:21:59","2020-02-29 00:21:49","2020-02-29 00:21:39","2020-02-29 00:21:29","2020-02-29 00:21:19","2020-02-29 00:21:09","2020-02-29 00:20:59","2020-02-29 00:20:49","2020-02-29 00:20:39","2020-02-29 00:20:29","2020-02-29 00:20:19","2020-02-29 00:20:09","2020-02-29 00:19:59","2020-02-29 00:19:49","2020-02-29 00:19:39","2020-02-29 00:19:29","2020-02-29 00:19:19","2020-02-29 00:19:09"],"y":[-0.326139193634087,1.16502804160154,-0.88022482519537,-0.315674705552958,0.842303486594071,1.09903955154042,0.540748233941493,1.51139899614583,1.36350442532827,0.154161793141077,1.13999076152457,-0.779734853930428,-1.07846381828743,-1.12467108114587,-0.236224569548931,-2.33260561417797,0.154757875126288,0.317238507057966,1.03692073019076,-0.663712375431012,2.20566871965305,0.14355781782797,-1.53263714970745,0.952798707825504,0.468358662499924,-0.410156427780237,1.89414978127117,-0.532810262141482,-0.0547786588538226,0.291784032045798,0.546861225357349,1.41142865312742,-0.100885218977072,-0.262402426675174,0.597801560866331,0.870577844626476,-0.490619984685138,-1.0993392536512,0.0640973850089791,-0.689808975460108,1.54810479041079,0.506910566513616,-1.32154816801328,-0.740848439665324,-0.339722429578561,-1.23776840283928,0.695136565949988,-1.39059981966593,0.215804558298591,-0.451076162385695,-0.412403018933345,0.365707055696836,2.03296369613066,-0.319214829718196,-0.32293123606366,-0.23514789178571,-0.641313670048667,1.97235436027402,0.265474173424869,-0.606597239109323,0.962348097794468],"mode":"lines","text":["0 seconds from now in Etc/UTC","10 seconds from now in Etc/UTC","20 seconds from now in Etc/UTC","30 seconds from now in Etc/UTC","40 seconds from now in Etc/UTC","50 seconds from now in Etc/UTC","60 seconds from now in Etc/UTC","70 seconds from now in Etc/UTC","80 seconds from now in Etc/UTC","90 seconds from now in Etc/UTC","100 seconds from now in Etc/UTC","110 seconds from now in Etc/UTC","120 seconds from now in Etc/UTC","130 seconds from now in Etc/UTC","140 seconds from now in Etc/UTC","150 seconds from now in Etc/UTC","160 seconds from now in Etc/UTC","170 seconds from now in Etc/UTC","180 seconds from now in Etc/UTC","190 seconds from now in Etc/UTC","200 seconds from now in Etc/UTC","210 seconds from now in Etc/UTC","220 seconds from now in Etc/UTC","230 seconds from now in Etc/UTC","240 seconds from now in Etc/UTC","250 seconds from now in Etc/UTC","260 seconds from now in Etc/UTC","270 seconds from now in Etc/UTC","280 seconds from now in Etc/UTC","290 seconds from now in Etc/UTC","300 seconds from now in Etc/UTC","310 seconds from now in Etc/UTC","320 seconds from now in Etc/UTC","330 seconds from now in Etc/UTC","340 seconds from now in Etc/UTC","350 seconds from now in Etc/UTC","360 seconds from now in Etc/UTC","370 seconds from now in Etc/UTC","380 seconds from now in Etc/UTC","390 seconds from now in Etc/UTC","400 seconds from now in Etc/UTC","410 seconds from now in Etc/UTC","420 seconds from now in Etc/UTC","430 seconds from now in Etc/UTC","440 seconds from now in Etc/UTC","450 seconds from now in Etc/UTC","460 seconds from now in Etc/UTC","470 seconds from now in Etc/UTC","480 seconds from now in Etc/UTC","490 seconds from now in Etc/UTC","500 seconds from now in Etc/UTC","510 seconds from now in Etc/UTC","520 seconds from now in Etc/UTC","530 seconds from now in Etc/UTC","540 seconds from now in Etc/UTC","550 seconds from now in Etc/UTC","560 seconds from now in Etc/UTC","570 seconds from now in Etc/UTC","580 seconds from now in Etc/UTC","590 seconds from now in Etc/UTC","600 seconds from now in Etc/UTC"],"type":"scatter","marker":{"color":"rgba(31,119,180,1)","line":{"color":"rgba(31,119,180,1)"}},"error_y":{"color":"rgba(31,119,180,1)"},"error_x":{"color":"rgba(31,119,180,1)"},"line":{"color":"rgba(31,119,180,1)"},"xaxis":"x","yaxis":"y","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>
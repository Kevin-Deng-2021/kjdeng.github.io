







<img src="https://kjdeng.github.io/assets/professional_photo.jpg" height="330px" width="250px" >  <img src="https://kjdeng.github.io/assets/data_learning_timeline.png" height="520px" width="700px" >
<br>
<br>


## Kevin Deng 

__About Me__


My passion is to innovatively design processes which will generate business intelligence or actionable strategy from data-driven analytical methodology.

With strong experience in Data, I would love to create insightful analysis by using analytical, statistical, visualized, machine learning as tools and weapons. I have developed multiple open source web-based BI and analytical tool to generate business insights with visualization and machine learning. Experience different analytical projects, I excel my Python and R skill, focusing on data analysis (Pandas, Numpy), digital marketing (GA, Adwords, GTM, FB ads), database(SQL, Salesforce SQOL), web-based application(Plotly, Flask), visualization(Tableau, PowerBI, Google Data Studio, D3.js)

<br>
__Data Science Milestone__


+ Predict vehicle sales for clients by using Time Series Model and Machine Learning.+ Establish data-driven KPI and strategy by developing management BI tool.+ Optimize business performance by visualizing campaigns’ quality on websites.

<br>
__Contact Me__

[LinkedIn](https://www.linkedin.com/in/kjdeng/)
<br>
<kjdeng@u.northwestern.edu>
<br>
[GitHub](https://github.com/kjdeng/)
<br>
[Stack Overflow](https://stackoverflow.com/users/7741793/kevin-deng)
<br>
<br>


## Analytics & Data


### 30 Days Predicting Analysis and Visualization

<img src="https://kjdeng.github.io/assets/pandas_logo.png height="30px" width="150px" > <img src="https://kjdeng.github.io/assets/plotly_logo.png height="30px" width="100px" > <img src="https://kjdeng.github.io/assets/pyflux_logo.jpeg height="50px" width="50px" >

<br>
The winter is coming to Chicago, and the Halloween party will be everywhere this weekend. When companies want to evaluate their outcome/performance, the most easy and straightforward method is to quantitatively show the yearly, qualterly, or monthly outcome, which can be sales, revenue, cash flow, expense, etc. In supply chain or manufacturing business, the selling and buyering pattern is strongly related to seasonal trend, so the analysis can focus on, for example, 'Q3' vs 'Q3 last year'. In marketing performance, the pattern has greater fluctuate by natioanl holidays, World Cup, Olympics, even weather. The comparison can be really diversied, and normally we can use montly performance to cover. 

In order to get 30 days period of time, library 'datatime' in Python provides much easy tool to get specific date. 
	
	import datatime
	
	date = datetime.datetime.strptime(start_date, '%Y-%m-%d')
	first_day_of_current_month = date.replace(day=1)
	last_day_of_previous_month = first_day_of_current_month - timedelta(days=1)
	first_day_of_previous_month = last_day_of_previous_month.replace(day=1)
	mid_day_of_previous_month = last_day_of_previous_month.replace(day=16)
	past_30_days = date - timedelta(days=30)
	
	
<br>

By using the time series prediction, Pyflux in Python is very useful tool. For instance, autoregressive integrated moving average (ARIMA) model provides the choice of 'ar' and 'ma', so you can manually or automattically adjust depends on previous data trend. Try to get relatively  as lowest number of AIC as possible.
The prediction will based on the dataframe you insert, which can be any duration of data depends on how is the industry cycle.
In this case, we predict next 31 days to forecast the short-term future's number. 

	import pyflux as pf
	
	model = pf.ARIMA(data=df, ar = ar_num, ma = ma_num, integ=0, target='sold')
	MLE_fit = model.fit("MLE")
	AIC = MLE_fit.aic
	df_predict = model.predict(h=31, intervals=False)

<br>

After we collect current data, previous data, and predicting data, now, we can try to show it logically containing business intelligence and insights for actionalble move.
Plolty.js save us very much time on developing HTML, CSS, Javasacript for ploting analytical time series diagram. Instead, we can import plotly and write in python script to make them render on website. 
	
	import plotly
	from plotly.graph_objs import *
		
	trace_previous_month = {
	"x": df5.index.tolist() , 
	"y": df7['sold'].tolist()[:len(df5.index.tolist())], 
	"mode": "lines", 
	"name": "Previous Month Sales", 
	"type": "scatter", 
	"uid": "e4bdb6",
	"visible": True,
	"line" : {
	"color" : "('rgb(0, 128, 255)')",
	"width" : 3}
	}
	trace_month = {
	  "x": df5.index.tolist() , 
	  "y": df5['sold'].tolist(), 
	  "mode": "lines", 
	  "fill": "tozeroy",
	  "name": "Forecasting", 
	  "type": "scatter", 
	  "uid": "e4bdb6",
	  "visible": True,
	  "line" : {
		"color" : "('rgb(205, 12, 24)')",
		"width" : 4,
		"dash" : 'dash'}
	}
	trace_real = {
	  "x": df6.index.tolist() , 
	  "y": df6['sold'].tolist(), 
	  "mode": "lines", 
	  "fill": "tozeroy",
	  "name": "Current Real Sales", 
	  "type": "scatter", 
	  "uid": "e4bdb6",
	  "visible": True,
	  "line" : {
		"color" : "('rgb(102, 0, 0)')",
		"width" : 4
		}
	}
	trace10 = {
	  "x": df5.index.tolist(), 
	  "y": [max(df5['sold'].tolist())]*len(df5.index.tolist()),
	  "fill": "tozeroy", 
	  "fillcolor": "rgba(208, 241, 244, 0.5)", 
	  "hoverinfo": "none", 
	  "mode": "none", 
	  "name": "Shading", 
	  "opacity": 0.2, 
	  "showlegend": False, 
	  "type": "scatter", 
	  "uid": "122dd9", 
	  "visible": True, 
	  "text" : "Forecast"
	}
	table_chart = ff.create_table(tota_sold_df)
	graphs = [table_chart]
	graphJSON = json.dumps(graphs, cls=plotly.utils.PlotlyJSONEncoder)
	 
<img src="https://kjdeng.github.io/assets/plotly_forecasting_unreal.png" height="330px" width="1000px" >
<br>
As you can see, the forecasting fluctuate greatly and the accumulative number is decreaseing from time to time, which does not make sense in term of business sales. As we know, ARIMA provides statistical model does not limit on positive integer. However, we can still use sorting algorithm to apply the most precise model(lowest AIC number). Now, the 30 days prediction provides very powerful short-term predicting withing a month. It also shows the previous month's data to diffreciate the increase or decrease within days. 

<img src="https://kjdeng.github.io/assets/plotly_forecasting_real.png" height="330px" width="1000px" >















	

















































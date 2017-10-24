







<img src="https://kjdeng.github.io/assets/professional_photo.jpg" height="320px" width="240px" > | <img src="https://kjdeng.github.io/assets/data_learning_timeline.png" height="460px" width="600px" >
## Kevin Deng 
<br><br>

__About Me__


My passion is to innovatively design processes which will generate business intelligence or actionable strategy from data-driven analytical methodology.

With strong experience in Data, I would love to create insightful analysis by using analytical, statistical, visualized, machine learning as tools and weapons. I have developed multiple open source web-based BI and analytical tool to generate business insights with visualization and machine learning. Experience different analytical projects, I excel my Python and R skill, focusing on data analysis (Pandas, Numpy), digital marketing (GA, Adwords, GTM, FB ads), database(SQL, Salesforce SQOL), web-based application(Plotly, Flask), visualization(Tableau, PowerBI, Google Data Studio, D3.js)

<br>
__Data Science Milestone__


+ Predict vehicle sales for clients by using Time Series Model and Machine Learning.+ Establish data-driven KPI and strategy by developing management BI tool.+ Optimize business performance by visualizing campaigns’ quality on websites.

__Contact Me__

[LinkedIn](https://www.linkedin.com/in/kjdeng/)
<br>
[Email](kjdeng@u.northwestern.edu)
<br>
[GitHub](https://github.com/kjdeng/)
<br>
[Stack Overflow](https://stackoverflow.com/users/7741793/kevin-deng)



## Analytics & Data


### 30 Days Predicting Analysis and Visualization

The winter is coming to Chicago, and the Halloween party will be everywhere this weekend. When companies want to evaluate their outcome/performance, the most easy and straightforward method is to quantitatively show the yearly, qualterly, or monthly outcome, which can be sales, revenue, cash flow, expense, etc. In supply chain or manufacturing business, the selling and buyering pattern is strongly related to seasonal trend, so the analysis can focus on, for example, 'Q3' vs 'Q3 last year'. In marketing performance, the pattern has greater fluctuate by natioanl holidays, World Cup, Olympics, even weather. The comparison can be really diversied, and normally we can use montly performance to cover. 

In order to get 30 days period of time, library datatime in python provides much easy tool to get specific date. 
	
	def get_previous_date(start_date):
		date = datetime.datetime.strptime(start_date, '%Y-%m-%d')
		first_day_of_current_month = date.replace(day=1)
		last_day_of_previous_month = first_day_of_current_month - timedelta(days=1)
		first_day_of_previous_month = last_day_of_previous_month.replace(day=1)
		mid_day_of_previous_month = last_day_of_previous_month.replace(day=16)
		past_30_days = date - timedelta(days=30)
		return first_day_of_previous_month.strftime('%Y-%m-%d'),
		mid_day_of_previous_month.strftime('%Y-%m-%d'), past_30_days.strftime('%Y-%m-%d')






















	










































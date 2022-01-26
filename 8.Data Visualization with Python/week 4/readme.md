# WEEK 4
# Creating Dashboards with Plotly and Dash
* Dashboarding Overview
	* Real-time visuals
	* Understand business moving parts
	* Visually track, analyze, and display key performance indicators (KPI)
	* Take informed decisions and improve performance
	* Reduced hours of analyzing
	* Best dashboards answer important business questions.
	* Plotly | Dash | Panel | Voila | Streamlit | bokeh
* Introduction to Ploty
	* Interactive, open-source plotting library
	* Supports over 40 unique chart types
	* Includes chart types like statistical, financial, maps, scientific, and 3-dimensional
	* Visualizations can be displayed in Jupiter notebooks saved to HTML files, or can be used in developing Python-built web applications.
	* Plotly Graph Object: low level interface to figures, traces, and layout<br>
	`plotly.graph_objects.Figure`<br>
	* Plotly Express: High level wrapper
```
#import required packages
import plotly.graph_objects as go
import plotly.express as px
import numpy as np

#Set random seed for reproducibility
np.random.seed(10)
x=np.arrange(12)
#Create random y values
y=np.random.randint(50, 500, size=12)

fig=go.Figure(data=go.Scatter(x=x, y=y))
fig.update_layout(title='Simple Line Plot', xaxis_title='Month', yaxis_title='Sales')
fig.show()
```
```
# Entire line chart can be creted in a single command
fig = px.line(x=x, y=y, title='Simple Line Plot', labels=dict(x='Month', y='Sales'))
fig.show()
```
* Introduction to Dash
	* Open-source User Interface Python library form Plotly
	* Easy to build GUI
	* Declarative and Reactive
	* Rendered in web browser and can be deployed to servers
	* Inherently cross-platform and mobile ready
* make dashboards interactive
	* Callback function is a python function that are automatically called by Dash whenever an input component’s property changes.
```
@app.callback(Output, Input)
def callback_function:
	....
	....
	....
	return some_result
```
*Lesson Summary*
* Best dashboards answer critical business questions. It will help business make informed decisions, thereby improving performance. 
* Dashboards can produce real-time visuals. 
* Plotly is an interactive, open-source plotting library that supports over 40 chart types. 
* The web based visualizations created using Plotly python can be displayed in Jupyter notebook, saved to standalone HTML files, or served as part of pure Python-built web applications using Dash. 
* Plotly Graph Objects is the low-level interface to figures, traces, and layout whereas plotly express is a high-level wrapper for Plotly. 
* Dash is an Open-Source User Interface Python library for creating reactive, web-based applications. It is both enterprise-ready and a first-class member of Plotly’s open-source tools. 
* Core and HTML are the two components of dash. 
* The dash_html_components library has a component for every HTML tag. 
* The dash_core_components describe higher-level components that are interactive and are generated with JavaScript, HTML, and CSS through the React.js library. 
* A callback function is a python function that is automatically called by Dash whenever an input component’s property changes. Callback function is decorated with `@app.callback` decorator. 
* Callback decorator function takes two parameters: Input and Output. Input and Output to the callback function will have component id and component property. Multiple inputs or outputs should be enclosed inside either a list or tuple. 

# Telecom-Churn--Prediction
The customers of "Telecom Industry" are free to select from multiple service providers and actively switch from one operator to another. The industry is highly competitive and faces around 15-25% of churning per year in average. Retaining existing customers is much more important than acquiring new customers as it costs around 5-10 times more to acquire one new customer. So, retaining high profitable customers is the first priority for telecom operators.
### Business Goal:
Analyse Customer level data for a leading telecom firm in the last month using the data from the first three months.
Build predictive models to identify customers at high risk of churn.
Identify the main indicators of churn.
### Data Understanding:
There are two types of telecom customers. Prepaid and postpaid. 
Prepaid is the most common model in India and Southeast Asia, while postpaid is more common in Europe in North America. This project is based on the Indian and Southeast Asian market.

**Postpaid customer**

pay a monthly/annual bill after using the services
when customers want to switch to another operator, they usually inform the existing operator to terminate the services, and you directly know that this is an instance of churn.
**Prepaid customer**

pay/recharge with a certain amount in advance and then use the services
when customers want to switch to another network can simply stop using the services without any notice, and it is hard to know whether someone has actually churned or is simply not using the services temporarily (e.g.travelling ).

### What is churn ?
**Revenue-based churn**: Customers who have not utilised any revenue-generating facilities such as mobile internet, outgoing calls, SMS etc. over a given period of time. One could also use aggregate metrics such as ‘customers who have generated less than INR 4 per month in total/average/median revenue’. The disadvantage of this definition is that there are customers who only receive calls/messages from their wage-earning counterparts, i.e. they don’t generate revenue but use the services. For example, many users in rural areas only receive calls from their wage-earning siblings or family members in urban areas. Usage-based churn: Customers who have not done any usage, either incoming or outgoing - in terms of calls, internet etc. over a period of time. The disadvantage of his definition is that when the customer has stopped using the services for a while, it may be too late to take any corrective actions to retain them. For e.g., if you define churn based on a ‘two-months zero usage’ period, predicting churn could be useless since by that time the customer would have already switched to another operator.

Here, we are dealing with the "Usage Based Churn" type.

**High Value Churn**: In the Indian and the Southeast Asian market, approximately 80% of revenue comes from the top 20% customers (called high-value customers). Thus, if we can reduce churn of the high-value customers, we will be able to reduce significant revenue leakage.

**Customer Behaviour**:
Customers usually decide to switch to another competitor over a period of time (this is especially applicable to high-value customers) and not instantly.

There are three phases of customer lifecycle :

The **‘good’** phase: In this phase, the customer is happy with the service and behaves as usual.

The **‘action’** phase: The customer experience starts to sore in this phase. They receive attractive offers from other operators, faces unjust charges, becomes unhappy with service quality etc. In this phase, the customer usually shows different behaviour. At this stage, it is very essential to identify high-churn-risk customers, since some corrective actions can be taken at this point (such as matching the competitor’s offer/improving the service quality etc.)

The **‘churn’** phase: In this phase, the customer is said to have already churned. We define churn based on this phase. Also, it is important to note that at the time of prediction (i.e. the action months), this data is not available to us for prediction. Thus, after tagging churn as 1/0 based on this phase, we discard all the data corresponding to this phase.

In this case, since we are working over a four-month window, the first two months are the ‘good’ phase, the third month is the ‘action’ phase, while the fourth month is the ‘churn’ phase.

## Step By Step Approach:
Import essential libraries
Data Understanding
Filtering High Value Customers
Data Cleaning
Handling Missing value and Feature Engineering
Derive new features
Data Visualization
Dimension Reduction using PCA
RFE
Model Building
Model Evaluation
Conclusion

# Data Analysis: New Internet Customers in Fort McMurray
## Requirements :			
			
## The tabs 1704 and 1705 are list of internet subscribers in Fort McMurray for the months of April 2017 (1704) and May 2017 (1705). 
### Prepare detailed analysis and presentation on the following:	

```		
1.) New Internet Customers in May 2017.			
2.) Churn in May 2017.			
3.) Customer migration activities in May 2017.			
4.) Compare customers in April and May.
```
					
### Column Definitions :

```
1.) month_id - Defined as last 2 digits of the year and the numeric representation of month to represent snapshot date.			
<> 1704 is April 2017 and 1705 is May 2017			
2.) subscriber_uid - Unique subscriber id, equivalent to the customer's account number		
3.) city - City where service is located. This exercise is only for Fort McMurray			
4.) FSA -  Forward Sortation Area, first 3 characters of the postal code as assigned by Canada Post		
5.) services_subscribed_name - Shaw services that the customer has in his account.			
6.) internet_service_level - The customer's subscribed internet service level			
7.) internet_rgu - Count of internet revenue generating unit (RGU) in the customer's account.			
8.) account_mrr - Monthly Recurring Rate. This is what the customer is paying (internet and all other services and products in the account) before taxes.			
9.) internet_mrr - This is what the customer is paying for his internet service before taxes.			
```
			
### Basic Calculations :

```			
1.) New Internet Customers - customers in the current month with internet_rgu > 0 with conditions below:			
a.) Subscriber_uid is in the current month but not in the previous month OR 			
b.) Subscriber_uid exists in the previous month but internet_rgu in the current month > previous month.			
			
2.) Churn - customers disconnecting service measured by both count of disconnecting RGUs and churn rate defined below:			
a.) Subscriber_uid is in the previous month but not in the current month OR			
b.) Subscriber_uid is in both months but internet_rgu in previous month > current month			
b.) Churn Rate (%) = Disconnects / Average (internet_rgu previous month and internet_rgu current_month)
			
3.) Migration - changes in customer's services. Compare previous month to current month services. This could be any of the following:			
a.) New Service(s) - see #1. customer had no service in April and have service in May OR had less RGUs in April than in May			
b.) No service - see #2. customer had internet service in April but none iin May OR had more RGUs in April than in May.			
c.) Change in service - customer changed internet products in May			
d.) Retain services - customer retained the same internet product in may
```			
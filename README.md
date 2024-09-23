Activity description
The objective of this test is to carry out a Business Case for a fast-food company in which we intend to
understand how the different commercial actions carried out affect it.
Our client has several restaurants in Santiago de Compostela, Barcelona, Madrid and Seville and does not
invest in advertising in any media, but only hires a mascot to hand out advertising leaflets in different
locations. These commercial actions in the street have a duration of one hour and always take place in a
geographical location indicated in a longitude, latitude and latitude type data.

Information sources used
To carry out this exercise, we will have 3 main data sources:
 restaurantes.csv: where we will have the location of all the restaurants
 ventas.csv: in which we will find the information related to the sales made with the amount in
euros
 publicidad.csv: with all commercial actions carried out on the street. Each one of them will
indicate the moment of beginning of the commercial action and the number of distributed
pamphlets
Exercise description
The aim is to find out how these commercial actions may be affecting customer purchases. To do this,
we intend to calculate an indicator that explains the Effectiveness Ef of each of the commercial
actions. To do this, we will consider the following conditions:
 For each sale, all commercial actions that have been made in the last 168 hours, within a
maximum distance of 5 km, are searched.
 For each of them, the effectiveness index is calculated as:

 The effectiveness result for the commercial action will be the sum of the effectiveness of all sales:

![image](https://github.com/user-attachments/assets/1184d3db-8713-4d57-8227-08011020efc8)

![image](https://github.com/user-attachments/assets/2cbccf6d-4e7b-4029-a530-9b6cfd43e0d4)



Where:
 p a = number of pamphlets distributed in the commercial action a
 d a = geographical distance between the restaurant in which the sale v is made and the
commercial action a
 dt a = time elapsed between the commercial action a and the sale v
 d max = maximum distance to consider (5 kilometers)
 dt max = maximum elapsed time to consider (168 hours)
 i = index of each of the commercial actions carried out in the last 168 hours prior to the
sale and a radius of less than 5 kilometers (including commercial action a)
 j = index of each of the sales that have contributed effectiveness to a commercial action
 p i = number of pamphlets distributed in the commercial action i
 d i = geographical distance between the restaurant in which the v sale is made and the
commercial action i
 dt i = time elapsed between the commercial action i and the sale v
 cost = amount in € of the sale v
NOTE: to calculate the time elapsed between the commercial action and the sale, only the start time
of the commercial action (the timestamp of the publicidad.csv file) must be taken into account.
A CSV file must be generated where each row represents a commercial action, and it will contain the
following fields:
![image](https://github.com/user-attachments/assets/d50d19be-b70a-4d29-b008-5f6596b8c3f4)

timestamp lat long Calculated
effectiveness
(long) (double) (double) (double)
Note: Remember that the data of the &quot;Calculated Effectiveness&quot; of the commercial action is calculated as the sum
of the efficiencies produced by each commercial action and sale.
Additional considerations
 The developed process will be executed as a batch process, but it is expected to have a reasonable
performance (minutes rather than hours)
 You will be able to choose the language or tools you prefer for the exercise
 The data is provided in CSV format, but you can choose to work with the provided files or store the
data in other types of storage (relational database, hdfs, NOSQL database, etc...)
 A dedication of a maximum of 12 hours is estimated to carry out the exercise
 You have a maximum of 5 days to deliver the solution to the exercise from the time you receive it

Deliverables
1. Power Point presentation (max 10 slides) with the following contents:
a. Descriptive analysis of the data provided
b. Detailed description of the algorithm, including the rationale for its selection
c. Insights and learnings of the results
2. Source code of the resolution of the exercise
3. CSV file with effectiveness calculation results

Evaluation criteria
The following aspects will be assessed:
• Ability to understand and to analyse the provided data
• Technical proposed solution
• Quality of the documentation

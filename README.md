# Multi-Channel Contacts (Shopee Code League)
## Background
Customer service is an important element of the Shopee business, as providing a good service for our customers end-to-end is critical for business growth and brand image. Our goal is to resolve the customer’s issue within the least amount of time while requiring the least amount of customer effort.

One measure for customer effort is the number of times a customer has to approach customer service over a particular issue, this is also known as the metric “Repeat Contact Rate” or RCR. Shopee is interested in studying the RCR in order to improve the effectiveness of our customer service.

Customers can contact customer service via various channels such as the livechat function, filling up certain forms or calling in for help. Each time a customer contacts us with a new contact method, a new ticket is automatically generated. A complication arises when the same customer contacts us using different phone numbers or email addresses resulting in multiple tickets for the same issue. Hence, our challenge here is to identify how to merge relevant tickets together to create a complete picture of the customer issue and ultimately determine the RCR.

## Task
For each ticket, identify all contacts from each user if they have the same contact information.

For the purpose of this question, assume that all contacts from the same Phone Number / Email are the same user.

## Basic Concepts
Each Order ID represents a transaction in Shopee.
Each Id represents the Ticket Id made to Shopee Customer Service.
All Phone Numbers are stored without the country code and the country code can be ignored.
Contacts represent the number of times a user reached out to us in that particular ticket (Email, Call, Livechat etc.)
If a value is NA means that the system or agent has no record of that value.
Submission Format
Determine how many contacts each user has had across the various tickets.

## Two columns required:

ticket_id
ticket_trace/contact
Format: (tickets in ascending order), (total contact)
| ticket_id | ticket_trace/contact                        |
| ----------|:-------------------------------------------:|
| 0         | 0-1-34567-78999, 14                         |
| 1         | 0-1-34567-78999, 14                         |
| 2         | 2-2456-4323-5343-6789, 13                   |


For each ticket, identify all other ticket_ids that belong to the same user, sorted in ascending order, as well as the total contacts the user had. If two tickets belong to the same user, the value for uid/contact for both tickets should be identical.

Your submission should have 500,000 rows (excluding headers), each with 2 columns.
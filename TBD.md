# _To Infinite and beyond!_

> 

### 19th May 2020 (Day 59 of lockdown)

#### ATTENDEES
> _Nathan, Sam, Alex and Lewis_
#### Your mate was too hungover to attend today, how would you summarise it for them?
* Infinite Day 
    * Pete Cotton spoke on the commerical aspects of IW and the differences between clients
    * Charlotte Goulding introduced us to some new people and spoke about lockdown.
    * Tom Walton spoke on:
        * Being a good consultant. 
        * Developing ones self.
        * How a consultancy firm operates; gathering clients, how to work out how much to charge for work, how to find and retain the best team
        * Career progression.
        * The history of IW; Media Solutions and of course skybet
        * How we benefit from being a consultant.
* Continued with our POC:
    * Wrote 13 functional unittests achieving _**84%**_ coverage.</br>
    <img src="img/cat.jpg" alt="cat" style="width:100px" />
    * Completed and tested the transform. 
    * About to start the Load function. 
        
####  Why did we learn it
* To show us how and where to do get the informaiton for career progression from.
* The fundamentals as to how to do out job the best we can.
* To garner a better understand of IW as a buisness (commerical aspect)
* To complete the steel thread and touch all technologies for our POC.
* How to stand out as a consultant rather than just another engineer. :(
* To stay relevant as we get old :(



#### How would you use it?
* Steel thread in POC to touch on all areas of project while essentially hardcoding some features.
    * For example not splitting drink name and price
    * Didn't split flavours from specialty teas
    * Example test:
```python
@patch("transform.Transform.date_breaker", return_value=unittest.mock)
    @patch("transform.Transform.person_breaker", return_value=unittest.mock)
    @patch("transform.Transform.drink_breaker", return_value=unittest.mock)
    @patch("transform.Transform.pay_method", return_value=unittest.mock)
    @patch("transform.Transform.card_masker", return_value=unittest.mock)
    def test_transform(self, mock_card_masker, mock_pay_method, mock_drink_breaker, mock_person_breaker, mock_date_breaker):
        mock_transformed_data = []
        mock_person_breaker.return_value = "Oscar", "Ohara"
        mock_date_breaker.return_value = datetime.date(2020, 5, 18), datetime.time(15, 46, 1)
        mock_location = "Isle of Wight"
        mock_drink_breaker.return_value = "Frappes - Chocolate Cookie"
        mock_price = "2.75"
        mock_pay_method.return_value = "CASH"
        mock_card_masker.return_value = None
        mock_entry = [(633, datetime.datetime(2020, 5, 18, 15, 46, 1), 'Isle of Wight', 'Oscar Ohara', ' Frappes - Chocolate Cookie', 2.75, 'CASH', None)]
        expected = [[datetime.date(2020, 5, 18), datetime.time(15, 46, 1), 'Isle of Wight', 'Oscar', 'Ohara', 'Frappes - Chocolate Cookie', 2.75, 'CASH', None]]
        actual = self.app.transform(mock_entry)
        self.assertEqual(actual, expected)
```

#### What would you tell yourself when using  it?
* Get 360 feedback in project review (feedback from superiors, peers, customers) perceptions might not fit with reality.
* Get over it being commercial, try your best, don't be an a***, 
* Consultancy is similar to a pyramid scheme. 
* Be client, IW and self focused (3 lenses).

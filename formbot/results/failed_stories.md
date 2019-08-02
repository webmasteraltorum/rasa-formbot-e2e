## happy-path
* greet: hello
    - utter_greet
* request_restaurant: id like a restaurant
    - restaurant_form
    - form{"name": "restaurant_form"}
* form: request_restaurant: {"cuisine": "chinese"}: i am looking for a chinese restaurant
    - form: restaurant_form
* form: inform: {"num_people": "5"}
    - form: restaurant_form
* form: inform: {"outdoor_seating": "false"}: No.   <!-- predicted: deny: {"outdoor_seating": "false"}: No. -->
    - form: restaurant_form
* form: deny: {"preferences": "no additional preferences"}
    - form: restaurant_form
* form: deny: {"feedback": "no feedback"}
    - form: restaurant_form
    - form{"name": null}
    - utter_slots_values
* thankyou: thanks
    - utter_noworries



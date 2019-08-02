## happy-path
* greet: hello
    - utter_greet
* request_restaurant: id like a restaurant
    - restaurant_form
    - form{"name": "restaurant_form"}
* request_restaurant: {"cuisine": "chinese"}: i am looking for a chinese restaurant
    - restaurant_form
* inform: {"num_people": "5"}
    - restaurant_form
* inform: {"outdoor_seating": "false"}: No.
    - restaurant_form
* deny: {"preferences": "no additional preferences"}
    - restaurant_form
* deny: {"feedback": "no feedback"}
    - restaurant_form
    - form{"name": null}
    - utter_slots_values
* thankyou: thanks
    - utter_noworries
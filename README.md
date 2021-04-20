# Python implementation of solution to the multiple traveling salesperson problem using Google's Operations Research tools library (OR-Tools)

- **Functionality**: given a list of physical addresses in CSV format, this code finds an approximate solution to the multiple traveling salesperson problem (mTSP) with a user-specified number of salespeople. The approximate solution is obtained using the vehicle routing  methods in Google's OR-Tools library. The output of the code is a CSV file containing the optimal routes for each salesperson. It uses the Google Maps API to compute the distance matrix using real-time traffic information. 

- [Google OR-Tools Vehicle Routing](https://developers.google.com/optimization/routing/vrp)


## Usage instructions

- If you have never registered for an API key on the Google Maps Platform, follow [this](https://developers.google.com/maps/gmp-get-started) getting started guide. 
- [Create](https://developers.google.com/maps/documentation/distance-matrix/get-api-key?hl=en_US) an API key for the Distance Matrix API and save it somewhere on your local machine.
- [Create](https://www.twilio.com/blog/2017/01/how-to-set-environment-variables.html) an environment variable for this API key. In the code, the environment variable name for this key is `GMAPS_KEY`. This step is not necessary if you never share the code file with anyone that should not see your API key.

- Save a CSV file containing your addresses in a single column with header 'Address' in the working directory. In the `main` method in `main.py` change line 14 to  `addrs_file = 'your_csv_file_name.csv'`. 

- If you don't have a list of addresses and want to generate them randomly, run `rand_addrs_gen.py` and it will produce a CSV file in the working directory with a user-specified number of addresses sampled around the Rothko Chapel in Houston, TX.

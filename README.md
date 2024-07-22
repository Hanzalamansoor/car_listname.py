# car_listname.py
I have created cars  list name where users  will enter 12 car names with their models and prices , after entering the data users can find the data when-ever the user wanted to by just searching it with the correct name of the car , it will pull the model and the price of the car quickoly 
# Initialize an empty list to store cars
cars = []

# Input for the first car
c1_name = input("Enter the first car name: ")
c1_model = input("Enter the model of the first car: ")
c1_price = float(input("Enter the price of the first car: "))
cars.append({"name": c1_name, "model": c1_model, "price": c1_price})

# Input for the second car
c2_name = input("Enter the second car name: ")
c2_model = input("Enter the model of the second car: ")
c2_price = float(input("Enter the price of the second car: "))
cars.append({"name": c2_name, "model": c2_model, "price": c2_price})

# Input for the third car
c3_name = input("Enter the third car name: ")
c3_model = input("Enter the model of the third car: ")
c3_price = float(input("Enter the price of the third car: "))
cars.append({"name": c3_name, "model": c3_model, "price": c3_price})

# Input for the fourth car
c4_name = input("Enter the fourth car name: ")
c4_model = input("Enter the model of the fourth car: ")
c4_price = float(input("Enter the price of the fourth car: "))
cars.append({"name": c4_name, "model": c4_model, "price": c4_price})

# Input for the fifth car
c5_name = input("Enter the fifth car name: ")
c5_model = input("Enter the model of the fifth car: ")
c5_price = float(input("Enter the price of the fifth car: "))
cars.append({"name": c5_name, "model": c5_model, "price": c5_price})

# Sort cars alphabetically by name
cars.sort(key=lambda car: car["name"])

# Print sorted list of cars
print("\nSorted List of Cars:")
for car in cars:
    print(f"{car['name']} - Model: {car['model']}, Price: {car['price']}")

# Search for a car by name
search_name = input("\nEnter a car name to search for: ")
found = False
for car in cars:
    if car["name"].lower() == search_name.lower():
        print(f"{search_name} found in the list - Model: {car['model']}, Price: {car['price']}")
        found = True
        break
if not found:
    print(f"{search_name} not found in the list.")

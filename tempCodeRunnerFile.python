class Flight:
    def __init__(self, f_id, scity, dest, price):
        self.f_id = f_id
        self.scity = scity
        self.dest = dest
        self.price = price

class FlightTable:
    def __init__(self):
        self.flights = []
    
    def add_flight(self, flight):
        self.flights.append(flight)
    
    def search_by_id(self, f_id):
        for flight in self.flights:
            if flight.f_id == f_id:
                return flight
        return None
    
    def search_by_source(self, scity):
        result = []
        for flight in self.flights:
            if flight.scity == scity:
                result.append(flight)
        return result
    
    def search_by_destination(self, dest):
        result = []
        for flight in self.flights:
            if flight.dest == dest:
                result.append(flight)
        return result

def main():
    table = FlightTable()
    table.add_flight(Flight("AI161E90", "BLR", "BOM", 5600))
    table.add_flight(Flight("BR161F91", "BOM", "BBI", 6750))
    table.add_flight(Flight("AI161F99", "BBI", "BLR", 8210))
    table.add_flight(Flight("VS171E20", "JLR", "BBI", 5500))
    table.add_flight(Flight("AS171G30", "HYD", "JLR", 4400))
    table.add_flight(Flight("AI131F49", "HYD", "BOM", 3499))
    
    user_input = input("Enter 1) Flight ID, 2) Source city, or 3) Destination city: ")
    
    if user_input == "1":
        f_id = input("Enter Flight ID: ")
        flight = table.search_by_id(f_id)
        if flight:
            print(f"Flight ID: {flight.f_id}, From: {flight.scity}, To: {flight.dest}, Price: {flight.price}")
        else:
            print("Flight not found.")
    elif user_input == "2":
        scity = input("Enter Source city: ")
        flights = table.search_by_source(scity)
        if flights:
            print("Flights from", scity)
            for flight in flights:
                print(f"Flight ID: {flight.f_id}, From: {flight.scity}, To: {flight.dest}, Price: {flight.price}")
        else:
            print("No flights found from", scity)
    elif user_input == "3":
        dest = input("Enter Destination city: ")
        flights = table.search_by_destination(dest)
        if flights:
            print("Flights to", dest)
            for flight in flights:
                print(f"Flight ID: {flight.f_id}, From: {flight.scity}, To: {flight.dest}, Price: {flight.price}")
        else:
            print("No flights found to", dest)
    else:
        print("Invalid input. Please enter 1, 2, or 3.")

if __name__ == "__main__":
    main()

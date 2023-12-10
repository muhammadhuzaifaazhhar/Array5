# Array5
def display_names_and_averages(names, averages):
    for i in range(len(names)):
        print(f"{names[i]} - Batting Average: {averages[i]}")

def search_and_display(name, names, averages):
    for i in range(len(names)):
        if names[i] == name:
            print(f"Name: {name} - Batting Average: {averages[i]}")
            return
    print("Name not found")

# Read data from a file (assuming the file has format: lastname,average)
file_path = 'player_data.txt'
player_names, batting_averages = read_data_from_file(file_path)

# Display names and batting averages
print("Player Names and Batting Averages:")
display_names_and_averages(player_names, batting_averages)

# Use a while loop to repeatedly ask the user for a last name
while True:
    name_to_search = input("\nEnter a last name to search (or 'exit' to quit): ")
    if name_to_search.lower() == 'exit':
        break
    search_and_display(name_to_search, player_names, batting_averages)

# Function to read a file, modify its content, and write to a new file
def read_and_write_file(input_filename, output_filename):
    try:
        # Open the input file for reading
        with open(input_filename, "r") as input_file:
            content = input_file.read()

        # Modify the content (example: convert to uppercase)
        modified_content = content.upper()

        # Write the modified content to the output file
        with open(output_filename, "w") as output_file:
            output_file.write(modified_content)

        print(f"File '{input_filename}' read successfully, and modified content written to '{output_filename}'.")

    except FileNotFoundError:
        print(f"Error: The file '{input_filename}' does not exist.")
    except IOError:
        print(f"Error: Could not read the file '{input_filename}' or write to '{output_filename}'.")

# Error handling for user input
def handle_file_input():
    filename = input("Enter the filename to read: ")
    output_filename = input("Enter the output filename to write: ")

    # Call the function to read and write the file with error handling
    read_and_write_file(filename, output_filename)

# Call the error handling function
handle_file_input()
# file-handling-exception-handling

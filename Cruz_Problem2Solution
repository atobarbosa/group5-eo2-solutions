def navigate_file_lines():
    """
    A function to navigate through lines of a file based on user input.
    Prompts the user for a filename and allows them to select specific lines to view.
    """
    try:
        filename = input("Enter the filename: ").strip()
        
        # Open and read the file lines safely
        with open(filename, 'r') as file:
            lines = file.readlines()

        print(f"The file '{filename}' has {len(lines)} lines.")

        while True:
            line_number = input("Enter a line number to view (or 0 to quit): ").strip()

            if not line_number.isdigit():
                print("Invalid input. Please enter a numeric value.")
                continue

            line_number = int(line_number)

            if line_number == 0:
                print("Exiting program. Goodbye!")
                break

            if 1 <= line_number <= len(lines):
                print(f"Line {line_number}: {lines[line_number - 1].strip()}")
            else:
                print(f"Line number out of range. Please enter a number between 1 and {len(lines)}.")

    except FileNotFoundError:
        print("Error: File not found. Please check the filename and try again.")
    except Exception as e:
        print(f"An unexpected error occurred: {e}")

# Run the function
navigate_file_lines()

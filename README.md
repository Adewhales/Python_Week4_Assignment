# Python_Week4_Assignment (Submission)

#File Read & Write Challenge: Create a program that reads a file and writes a modified version to a new file.

# File Read and Write Challenge


try:
     
     # Read file
     with open("readme.txt", "r") as infile:
        content = infile.read()

    # Modify content
    modified_content = content.upper()

    # Write modified content to a new file
    with open("newtext.txt", "w") as outfile:
        outfile.write(modified_content)
     print("File read, modified, and written to 'newtext.txt'.")
except FileNotFoundError:
    print("Error: The file 'readme.txt' does not exist.")
except Exception as e:
    print(f"An error occurred: {e}")


# Error Handling Lab: Ask the user for a filename and handle errors if it doesn’t exist or can’t be read.

# Error Handling 

while True:
   
    try:
        filename = input("Enter the name of the file to read: ")

        # Attempt to open the file
        with open(filename, "r") as file:
            content = file.read()
            print("File content successfully read!")
            break

    except FileNotFoundError:
        print(f"Error: The file '{filename}' does not exist. Please try again.")
        break

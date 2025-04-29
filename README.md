def main():
    filename = input("Enter file name: ")
    try:
        f = open(filename, "r")
        data = f.read()
        f.close()

        new_data = data.upper()

        new_file = open("new", "w")
        new_file.write(new_data)
        new_file.close()

        print("File saved.txt")

    except FileNotFoundError:
        print("File not found")
    except:
        print("Something went wrong")

main()

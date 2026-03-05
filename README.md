# temperature_converter
Simple python CLI tool for converting temperatures between Fahrenheit and Celsius
def fahrenheit_to_celsius(f):
    return (f - 32) * 5 / 9


def celsius_to_fahrenheit(c):
    return (c * 9 / 5) + 32


print("Temperature Converter")
print("1. Fahrenheit to Celsius")
print("2. Celsius to Fahrenheit")

choice = input("Choose an option (1 or 2): ")

try:
    temp = float(input("Enter the temperature: "))
except ValueError:
    print("Invalid number.")
    exit()

if choice == "1":
    result = fahrenheit_to_celsius(temp)
    print(f"{temp}°F = {round(result,2)}°C")

elif choice == "2":
    result = celsius_to_fahrenheit(temp)
    print(f"{temp}°C = {round(result,2)}°F")

else:
    print("Invalid option selected.")

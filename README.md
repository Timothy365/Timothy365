def weight_converter():
    print('Welcome To Easy weight converter!')
    print("Units supported: kilograms (kg), pounds (lbs), ounces (oz), grams (g)\n")

    weight = float(input('Enter the weight value: ').strip())
    from_unit = input("Enter the current unit (kg, lbs, oz, g): ").strip().lower()
    to_unit = input("Enter the unit to convert to (kg, lbs, oz, g): ").strip().lower()

    to_kg = {
        'kg': 1,
        'ibs': 0.453592,
        "oz": 0.0283495,
        "g": 0.001
    }

    from_kg = {
        'kg': 1,
        'ibs': 2.20462,
        "oz": 35.274,
        "g": 1000
    }

    if from_unit not in to_kg or to_unit not in from_kg:
        print("Invalid unit. Please enter valid units: kg, lbs, oz, g")
        return

    weight_in_kg = weight * to_kg[from_unit]
    converted_weight = weight_in_kg * from_kg[to_unit]

    print(f"\n{weight} {from_unit} is equal to {converted_weight:.2f} {to_unit}")


weight_converter()

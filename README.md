import datetime

def happy_birthday(lykha, 2006, nov, 21):
    """
    Generates a personalized happy birthday greeting.

    Args:
        name: The perso
        year: The year of their birth.
        month: The month of their birth (1-12).
        day: The day of their birth (1-31).

    Returns:
        A string containing the personalized greeting.
    """

    today = datetime.date.today()
    birthday = datetime.date(today.year, month, day)

    if today == birthday:
        return f"Happy Birthday, {name}! 🎉🎂"
    elif today > birthday:
        next_birthday = datetime.date(today.year + 1, month, day)
        days_until_birthday = (next_birthday - today).days
        return f"Happy almost birthday, {name}! You're {days_until_birthday} days away from your special day. 🥳"
    else:
        days_until_birthday = (birthday - today).days
        return f"Happy early birthday, {name}! Just {days_until_birthday} days left until your birthday! 🥳"

# Get user input
name = input("Enter the name of the person: ")
year = int(input("Enter the year of birth: "))
month = int(input("Enter the month of birth (1-12): "))
day = int(input("Enter the day of birth (1-31): "))

# Generate the greeting
greeting = happy_birthday(name, year, month, day)
print(greeting)

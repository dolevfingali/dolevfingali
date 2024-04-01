def exercise_plan(interpretation):
    """
    פונקציה זו מחזירה תוכנית אימונים בהתאם לקטגוריה הגופנית של האדם.
    פרמטרים:
    - interpretation: תוצאת קטגורית BMI
    """
    if interpretation == "תת משקל":
        return "תוכנית אימונים לבניית שרירים והגנה על משקל."
    elif interpretation == "בריא":
        return "תוכנית אימונים לשיפור הכושר הגופני הכללי."
    elif interpretation == "משקל יתר":
        return "תוכנית אימונים לשמירה על משקל תקין והפחתת שומנים."
    else:
        return "תוכנית אימונים להפחתת משקל והגברת כושר הלב."

def main():
    weight = float(input("הזן משקל בק"ג: "))
    height = float(input("הזן גובה במטרים: "))
    
    bmi = calculate_bmi(weight, height)
    interpretation = interpret_bmi(bmi)
    
    print("מדד הBMI שלך הוא: {:.2f}".format(bmi))
    print("המצב הגופני שלך הוא: ", interpretation)
    
    plan = exercise_plan(interpretation)
    print("הנה ההמלצה על תוכנית האימונים המותאמת אישית שלך:")
    print(plan)

if __name__ == "__main__":
    main()

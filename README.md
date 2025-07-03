def contact_book():
    contacts = {}

    while True:
        print("\n1.Add 2.Update 3.Retrieve 4.View 5.Exit")
        c = input("Choose: ")

        if c == "1":
            n = input("Name: ").title()
            if n in contacts:
                continue
            p = input("Phone: ")
            e = input("Email: ")
            if "@" in e and "." in e:
                contacts[n] = {"phone": p, "email": e}

        elif c == "2":
            n = input("Name: ").title()
            if n in contacts:
                p = input("Phone: ")
                e = input("Email: ")
                if "@" in e and "." in e:
                    contacts[n] = {"phone": p, "email": e}

        elif c == "3":
            n = input("Name: ").title()
            if n in contacts:
                print(contacts[n])

        elif c == "4":
            for n, d in contacts.items():
                print(n, "-", d)

        elif c == "5":
            break

contact_book()

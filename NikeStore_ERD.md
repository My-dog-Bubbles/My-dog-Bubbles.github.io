# Coff cafe

## Documentation
 #### I have to put it above because it won't let me put it below
### Product:
- The Product group has the price, name, powerup and wither if the item is in specialty week.
- The ProductID is the pruduct number. 

### Customer:
- The Customer group has the name, email, phone number, and wither if the cutomer is a member of a customer.
- The CustomerID is the customer number(not phone number)

### Order:
- The Order group has the order destination, Payment type, and what type of recipt the customer wants.
- It pulls the CustomerID to see who is ordering.
- It pulls the Specialty_WeekID to see what is being ordered. Depending on the week different things will be ordered.

### Inventory:
- The Invertory group has wether if the item is in or out of stockand the amount of items in stock.

### Specialty week:
- Specialty week is where specific items show on different days.

```mermaid 
erDiagram 

PRODUCT { 
    int ProductID PK
    int Price
    str Product_Name
    int Specialty_week
    str PowerUps
} 

CUSTOMER { 
    int CustomerID PK
    str Name
    str Email
    int Phone_number
    str Member
}

ORDER ||--|{ CUSTOMER : has
ORDER ||--|{ PRODUCT : has
ORDER ||--|| Specialty_Week : for
ORDER { 
    int OrderID PK
    int CustomerID FK
    int Specialty_WeekID FK
    str Destination
    str Payment_Type
    str Receipt_Type
} 

INVENTORY ||--|| PRODUCT : has
INVENTORY {
    int ProductID FK
    str In_or_out
    int Amount_instock
}

Specialty_Week ||--|{ PRODUCT : has
Specialty_Week {
    int Specialty_WeekID PK
    int ProductID FK
}

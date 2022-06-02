# REACT CRASH COURSE - UDEMY

---

it is created for future reference

## How REACT works

- React is all about "Components". React allows you to create re-usable and reactive components consisting of HTML and JS (and CSS)

- Define the target state and let React figure out the actual JS DOm instructions

### Why Components? 
 
- Reusability (don't repeat yourself)

- Seperation of concerns (don't do too many things in one and the same place)

- -> Split big chunks of code into multiple smaller functions

## props

- props: stands for property. We can set props of our own components

- components can't use data stored in other components, only parents components can

## Use normal JavaScript logic to Components

```
function ExpensesItem (props) {
 const month = props.date.toLocaleString("en-US", { month: "long" });
  const day = props.date.toLocaleString("en-US", { day: "2-digit" });
  const year = props.date.getFullYear(); //JS method to get date
}

return(
    <div className="expense-item">
      <div>
        <div>{month}</div>
        <div>{year}</div>
        <div>{day}</div>
      </div>
    </div> 
    //August  2020  14
)
 
```

## Splitting components into multiple components

- We can split components into another file which is a child of current child

-ie:                        App.js ( parent's file)
                                  /     \
                                 /       \
                          ExpenseItem    
                              |
                              |
                         ExpenseDate

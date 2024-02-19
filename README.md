# Product Grid Viewer Development Overview

### Task
Implement a web page using OOP (Object-Oriented Programming) principles to 
manipulate the DOM, creating three main objects: a Grid, Nav, and Product.

### User story
- As a user, they can view the products on the page, with certain items marked as on sale.
- The user can sort the products based on price or name by selecting the corresponding option in the nav.
- The sorting operation will not trigger a whole page refresh.

## Development Approach

### Object-Oriented JavaScript

The application is structured around three main classes: 
Product, Nav, and Grid, each responsible for a distinct aspect of the 
application's functionality:

- Product Class: Manages individual product details and rendering. 
  It initializes from a JSON object containing product attributes 
  (title, desc, price, sale) and generates a DOM node for display.
    
- Nav Class: Handles the navigation system, allowing users to sort 
  products based on selected criteria. It leverages custom events 
  to communicate sorting attributes (attr) to the Grid class.
    
- Grid Class: Orchestrates the overall layout, rendering products 
  and navigation elements based on data provided. It listens for 
  custom events from Nav instances to sort products dynamically.

### Data Management

One of the key challenges was managing product data efficiently, 
especially maintaining the state post-initial fetch. To address this:

- Static Class Field: A static field within the Grid class was implemented 
  to store the initial fetch data. This approach ensured that the original 
  data set was readily available for re-rendering or sorting operations 
  without requiring additional fetch requests, thus optimizing performance 
  and resource usage.
    
### Styling 

This project showcases a dynamic and responsive web page designed to display 
a collection of products.

### Key Features 

- Global Reset and Box Sizing: Resets default margins to ensure a consistent 
experience across multiple browsers.
- Responsive Layout: The application adapts to various screen sizes.
- Product Cards: Items are presented in a simple format, allowing users to easily 
absorb the key information. Cards are designed to respond to user actions.

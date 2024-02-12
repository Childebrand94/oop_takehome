#Product Grid Viewer Development Overview

##Introduction

This document provides an in-depth look at the development process, 
architectural decisions, and challenges encountered during the creation of the 
Product Grid Viewer, a web application designed to display and sort a collection 
of products in a grid layout. The application emphasizes interactive features 
such as sorting products based on attributes and highlighting sale items, all 
realized through vanilla JavaScript, HTML, and CSS.

##Development Approach

###Object-Oriented JavaScript

The application is structured around three main classes: 
Product, Nav, and Grid, each responsible for a distinct aspect of the 
application's functionality:

    Product Class: Manages individual product details and rendering. 
    It initializes from a JSON object containing product attributes 
    (title, desc, price, sale) and generates a DOM node for display.
    
    Nav Class: Handles the navigation system, allowing users to sort 
    products based on selected criteria. It leverages custom events 
    to communicate sorting attributes (attr) to the Grid class.
    
    Grid Class: Orchestrates the overall layout, rendering products 
    and navigation elements based on data provided. It listens for 
    custom events from Nav instances to sort products dynamically.

###Data Management

One of the key challenges was managing product data efficiently, 
especially maintaining the state post-initial fetch. To address this:

    Static Class Field: A static field within the Grid class was implemented 
    to store the initial fetch data. This approach ensured that the original 
    data set was readily available for re-rendering or sorting operations 
    without requiring additional fetch requests, thus optimizing performance 
    and resource usage.

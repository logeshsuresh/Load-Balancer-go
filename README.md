# Go Load Balancer

This is a simple Go-based load balancer that distributes incoming HTTP requests among multiple backend servers. It uses a round-robin algorithm to evenly distribute requests among the available servers.

## Features

- Round-robin load balancing algorithm.
- Supports multiple backend servers.
- Easy-to-use and extendable.

## Prerequisites

- Go (Golang) installed on your machine.

## Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/logeshsuresh/Load-Balancer-go.git
   


2. Run 
   
   ```bash 
   go run main.go

The load balancer will start serving requests on localhost:8000

## Configuration 

You can configure the backend servers by modifying the servers slice in the main function of the main.go file. Simply add or remove instances of the newSimpleServer function to specify your backend servers.

```
    servers := []Server {
        newSimpleServer("https://www.example.com"),
        newSimpleServer("https://www.anotherexample.com"),
        // Add more backend servers here as needed
    }

```

## Usage

The load balancer will distribute incoming requests among the configured backend servers using a round-robin approach. Requests can be made to the load balancer's address (e.g., http://localhost:8000) to have them proxied to one of the backend servers.

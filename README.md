# Go Proof of Work Blockchain

This project implements a simple proof-of-work blockchain in Go. It allows users to create and retrieve blocks in a blockchain through a web server.

## Features

- **Blockchain Structure**: Each block contains an index, timestamp, data, hash, previous hash, difficulty, and nonce.
- **Proof of Work**: The blockchain uses a proof-of-work mechanism to validate new blocks.
- **HTTP API**: The application exposes an HTTP API to interact with the blockchain.

## Getting Started

### Prerequisites

- Go 1.22 or later
- Go modules enabled

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/pri-3x/Go-POW
   cd go-pow
   ```

2. Install dependencies:
   ```bash
   go mod tidy
   ```

3. Create a `.env` file in the root directory and specify the port:
   ```
   PORT=8080
   ```

### Running the Application

To start the server, run the following command:
```bash
go run .
```

The server will start on the specified port (default is 8080).

### Add a new block

To add a new block to the blockchain, send a POST request to the `/` endpoint with the desired data in JSON format:
```bash
curl -X POST http://localhost:8080 -H "Content-Type: application/json" -d '{"data": 75}'
```


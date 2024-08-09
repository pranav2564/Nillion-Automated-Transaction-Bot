# Winnode Project Bot

## Description

This project is a bot for the Winnode project that periodically sends $NIL tokens to generated Nillion addresses.

## Setup Instructions

### Prerequisites

- Node.js and npm installed on your machine. You can download and install them from [Node.js official website](https://nodejs.org/).

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/Winnode/nillion.git
    ```

2. Navigate to the project directory:

    ```bash
    cd nillion
    ```

3. Initialize a new npm project if you haven't already:

    ```bash
    npm init -y
    ```

4. Install the required packages:

    ```bash
    npm install dotenv bip39 @cosmjs/proto-signing @cosmjs/stargate
    ```

5. If you don't have `ts-node` and `typescript` installed, you can install them globally:

    ```bash
    npm install -g ts-node typescript
    ```

    Or as dev dependencies in your project:

    ```bash
    npm install --save-dev ts-node typescript
    ```

### Configuration

1. Create a `.env` file in the root directory of your project:

    ```bash
    touch .env
    ```

2. Add your mnemonic phrases to the `.env` file. Example:

    ```plaintext
    MNEMONIC1="your mnemonic phrase 1"
    MNEMONIC2="your mnemonic phrase 2"
    MNEMONIC3="your mnemonic phrase 3"
    # Add more mnemonics as needed
    ```

3. Create a `recipients.txt` file in the root directory of your project:

    ```bash
    touch recipients.txt
    ```

4. Add recipient addresses to the `recipients.txt` file, one per line. Example:

    ```plaintext
    nillion1fjg703wl2hzfyp0qhums37melfdrcut4wc24ze
    nillion1xeg9pupt2qpgmyx5wn8awzul0k4p3l7wpu06zc
    ```

### Running the Script

You can run the TypeScript script using `ts-node`:

```bash
ts-node src/index.ts

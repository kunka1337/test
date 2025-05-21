# INFINITY Miner v2

[More info about INFINITY Token](https://8finity.xyz)

## Prerequisites

- Python 3.10 or higher
- pip (Python package manager)
- OpenCL support
- Docker (optional for Docker installation)

## Quick Start with Docker

The easiest way to run the miner is using Docker:

```bash
# Clone the repository
git clone https://github.com/yourusername/infinity-miner.git
cd infinity-miner

# Create .env file
echo "INFINITY_MINER_PRIVATE_KEY=your_private_key_here" > .env

# Run with Docker
docker build -t infinity-miner .
docker run --env-file .env infinity-miner
```

## Manual Installation

### Installation Steps

1. **Install Python and pip**
   - Download and install from [python.org](https://www.python.org/downloads/)

2. **Install OpenCL**
   **For Linux** 
   ```bash
   sudo apt update && sudo apt install -y \
       ocl-icd-opencl-dev \
       opencl-headers \
       python3-pip
   ```

   **For macOS**
   - OpenCL is included with macOS

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure Environment**
   Create a `.env` file in the project root:
   ```bash
   # Required: Your private key for mining (64 characters after 0x). You need to have some Sonic (S) balance to start mining.
   INFINITY_MINER_PRIVATE_KEY=your_private_key_here

   # Optional: RPC and WebSocket endpoints
   # INFINITY_RPC=https://rpc.soniclabs.com
   # INFINITY_WS=wss://rpc.soniclabs.com

   # Optional: Mining rewards recipient
   # INFINITY_REWARDS_RECIPIENT_ADDRESS=your_address_here

   # Optional: Logging level 
   # LOGLEVEL=DEBUG
   ```

5. **Run the Miner**
   ```bash
   python3 src/main.py
   ```

## Configuration Options

- `INFINITY_MINER_PRIVATE_KEY`: Your private key for mining (required) 
- `INFINITY_RPC`: Custom RPC endpoint (optional)
- `INFINITY_WS`: Custom WebSocket endpoint (optional)
- `INFINITY_REWARDS_RECIPIENT_ADDRESS`: Address to receive mining rewards (optional)
- `LOGLEVEL`: Set logging verbosity (optional)

## Support

For issues and feature requests, please open an issue on GitHub. We also welcome pull requests for improvements and bug fixes. 

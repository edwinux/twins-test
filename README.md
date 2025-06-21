# TWINS Cryptocurrency

A proof-of-stake cryptocurrency based on PIVX with privacy features through Zerocoin protocol integration.

## About TWINS

TWINS is a decentralized cryptocurrency that implements proof-of-stake consensus with masternode functionality and privacy features. The network supports both regular transactions and privacy-enhanced transactions through the Zerocoin protocol.

## Key Features

- **Proof of Stake Consensus**: Energy-efficient consensus mechanism after initial PoW phase
- **Masternode Network**: Multi-tier masternode system providing network services
- **Privacy Features**: Zerocoin protocol integration for enhanced transaction privacy  
- **Fast Transactions**: 2-minute block times for quick transaction confirmation
- **Tiered Rewards**: Dynamic block reward schedule with inflation reduction over time

## Technical Specifications

### Network Parameters
- **Block Time**: 2 minutes (120 seconds)
- **Consensus**: Proof of Work (blocks 1-400), then Proof of Stake
- **Default Port**: 37817
- **RPC Port**: 37818
- **Maturity**: 60 blocks for coinbase/coinstake
- **Staking Age**: 3 hours minimum
- **Maximum Supply**: 10,000,000,000 TWINS (10 billion)

### Block Rewards Schedule

The block reward follows a structured reduction schedule:

- **Block 1**: 6,000,000 TWINS (initial pre-mine)
- **Blocks 2-711,110**: 15,220.70 TWINS per block
- **Blocks 711,111-716,665**: 8,000 TWINS per block
- **Blocks 716,666-722,221**: 4,000 TWINS per block  
- **Blocks 722,222-727,776**: 2,000 TWINS per block
- **Blocks 727,777-733,332**: 1,000 TWINS per block
- **Blocks 733,333-738,887**: 500 TWINS per block
- **Blocks 738,888-744,443**: 250 TWINS per block
- **Blocks 744,444-749,999**: 125 TWINS per block
- **Blocks 750,000-755,554**: 60 TWINS per block
- **Blocks 755,555-761,110**: 30 TWINS per block
- **Blocks 761,111-766,665**: 15 TWINS per block
- **Blocks 766,666-772,221**: 8 TWINS per block
- **Blocks 772,222-777,776**: 4 TWINS per block
- **Blocks 777,777-909,999**: 2 TWINS per block
- **Blocks 910,000-6,569,604**: 100 TWINS per block
- **Block 6,569,605+**: 0 TWINS (no new coins)

### Masternode System

TWINS implements a multi-tier masternode system:

- **Tier 1**: 1,000,000 TWINS collateral
- **Tier 2**: 5,000,000 TWINS collateral  
- **Tier 3**: 20,000,000 TWINS collateral
- **Tier 4**: 100,000,000 TWINS collateral

**Reward Distribution:**
- 80% of block rewards go to masternodes
- 20% of block rewards go to stakers
- Development fund receives dedicated allocation from specific reward pools

### Staking Parameters

- **Minimum Stake**: 12,000 TWINS
- **Staking Age**: 3 hours minimum before coins can stake
- **Maturity**: 60 confirmations for newly minted coins

## Building and Installation

### Dependencies

Ensure you have the required dependencies installed before building:

- GCC 4.8+ or Clang 3.3+
- Boost 1.55+
- OpenSSL 1.0.x
- Berkeley DB 4.8+
- Qt 5.x (for GUI wallet)

### Build Instructions

```bash
# Clone the repository
git clone https://github.com/edwinux/twins-test.git
cd twins-test

# Generate build files
./autogen.sh

# Configure build
./configure

# Build the project
make

# Optional: Install system-wide
sudo make install
```

## Usage

### Running the Daemon

```bash
# Start the TWINS daemon
./src/twinsd -daemon

# Check status
./src/twins-cli getinfo
```

### Command Line Interface

```bash
# Get blockchain information
./src/twins-cli getblockchaininfo

# Get wallet balance
./src/twins-cli getbalance

# Send transaction
./src/twins-cli sendtoaddress <address> <amount>
```

## Network Seed Nodes

The network includes multiple seed nodes for initial peer discovery across different geographical locations.

## Development

TWINS is actively developed and maintained. The codebase is based on PIVX with custom modifications for the TWINS-specific features and economic model.

## License

TWINS is released under the MIT License. See the [COPYING](COPYING) file for details.

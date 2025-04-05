# XixuAI NFT Module

A comprehensive NFT (Non-Fungible Token) module for the XixuAI platform, allowing users to mint, buy, sell, and transfer NFTs.

## Features

- **NFT Minting**: Create new NFTs with custom metadata, attributes, and rarity levels
- **NFT Marketplace**: Browse and purchase NFTs listed for sale
- **NFT Management**: List your NFTs for sale, transfer them to other addresses, or cancel listings
- **Wallet Integration**: Seamless connection with MetaMask and other Web3 wallets
- **Multi-language Support**: Internationalized interface with English and other languages
- **Responsive Design**: Works on desktop and mobile devices

## Technical Stack

### Backend
- Node.js with Express
- MongoDB for storing NFT metadata and listings
- Ethers.js for blockchain interactions
- Solidity smart contracts (ERC721 standard)

### Frontend
- React with TypeScript
- Material-UI for components
- i18next for internationalization
- Ethers.js for wallet integration

## Setup

### Prerequisites
- Node.js (v14+)
- MongoDB
- MetaMask or another Web3 wallet
- Ethereum account with test ETH (for Goerli testnet)

### Installation

1. Clone the repository
2. Install dependencies:
   ```
   cd backend
   npm install
   
   cd ../frontend
   npm install
   
   cd ../contracts
   npm install
   ```

3. Configure environment variables:
   - Copy `.env.example` to `.env` in each directory
   - Fill in the required values

4. Deploy the smart contract:
   ```
   cd contracts
   npx hardhat run scripts/deploy.js --network goerli
   ```

5. Update the contract address in the backend configuration

6. Start the servers:
   ```
   # Start backend
   cd backend
   npm start
   
   # Start frontend
   cd frontend
   npm start
   ```

## Usage

1. Connect your wallet using the "Connect Wallet" button
2. Navigate to the NFT page
3. Use the tabs to switch between the marketplace and minting
4. To mint an NFT:
   - Fill in the name, description, and image URL
   - Add attributes (optional)
   - Select rarity level
   - Click "Mint"
5. To list an NFT for sale:
   - Find your NFT in the marketplace
   - Click "List for Sale"
   - Enter the price in ETH
   - Confirm the listing
6. To buy an NFT:
   - Find an NFT in the marketplace
   - Click "Buy"
   - Confirm the transaction in your wallet
7. To transfer an NFT:
   - Find your NFT in the marketplace
   - Click "Transfer"
   - Enter the recipient's address
   - Confirm the transfer

## API Endpoints

### NFT Metadata
- `GET /api/nft/metadata/:tokenId` - Get NFT metadata by token ID
- `GET /api/nft/owner/:address` - Get all NFTs owned by an address

### NFT Operations
- `POST /api/nft/mint` - Mint a new NFT
- `POST /api/nft/list` - List an NFT for sale
- `POST /api/nft/buy` - Buy an NFT
- `POST /api/nft/transfer` - Transfer an NFT
- `POST /api/nft/cancel-listing` - Cancel a listing

### Marketplace
- `GET /api/nft/listings` - Get all active listings

## Security

- All blockchain transactions require wallet signature
- Input validation on both frontend and backend
- Rate limiting on API endpoints
- Secure storage of private keys and sensitive data

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details. 
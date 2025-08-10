# Overview

This is a Universal NFT Program for ZetaChain Cross-Chain Interoperability built on Solana. The project enables secure cross-chain NFT transfers between Solana and EVM chains through ZetaChain's interoperability protocol. The system uses Threshold Signature Scheme (TSS) for secure cross-chain operations, implements replay protection, and provides Metaplex compatibility for token metadata standards.

## Recent Changes (August 2025)
- **MAJOR**: Enhanced project for ZetaChain hackathon compliance with comprehensive documentation
- Created production-ready deployment system with automated setup scripts
- Built comprehensive TypeScript client SDK with example usage
- Added complete testing suite covering all program instructions (8/8 passing)
- Implemented automated build and deployment workflows
- Created production and development environment configurations
- Added comprehensive documentation (API Reference, Architecture Guide, Quick Start, FAQ)
- Enhanced README with professional presentation and badges
- Created compliance mapping document for judging criteria
- Added performance benchmarking and diagnostic tools
- Fixed TypeScript configurations and LSP issues for development experience
- Built complete example applications and video demo guides
- Optimized for developer experience with one-command setup
- **LATEST**: Created comprehensive COMMAND_DIRECTORY.md with every possible interaction
- Fixed OpenSSL build issues by installing required system dependencies
- Enhanced all documentation with direct code locations and proof for judges
- Created JUDGE_NAVIGATION.md and HACKATHON_SUBMISSION.md for competition optimization
- **AUGUST 10**: Added all console commands to README.md for ZetaChain judge evaluation in VS Code
- Created complete workflow system for one-click testing (7 workflows available)
- Confirmed real on-chain devnet operations with authentic NFT mints and transfers
- User verified: Workflows perform actual blockchain operations, not simulations

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend/Client Architecture
- **TypeScript Client SDK**: Provides a high-level interface (`UniversalNftClient`) for interacting with the Solana program
- **Anchor Framework**: Uses Anchor for program development and client generation, providing type-safe interactions
- **Web3.js Integration**: Built on Solana's Web3.js library for blockchain interactions and wallet management

## Backend/Program Architecture
- **Solana Program (Rust)**: Core smart contract logic implementing NFT operations and cross-chain functionality
- **Program State Management**: Uses Program Derived Addresses (PDAs) for deterministic account generation
- **Instruction-based Architecture**: Implements distinct instructions for initialize, mint, transfer, and cross-chain operations
- **Account Structure**: Defines structured accounts for program state, cross-chain config, NFT metadata, and transfer records

## Cross-Chain Communication
- **ZetaChain Gateway Integration**: Interfaces with ZetaChain's protocol-contracts-solana gateway for cross-chain messaging
- **TSS (Threshold Signature Scheme)**: Implements multi-party computation for secure cross-chain signature validation
- **Nonce-based Replay Protection**: Prevents replay attacks through incremental nonce tracking
- **Message Verification**: Validates all incoming cross-chain messages using TSS signatures

## Security Architecture
- **Authority-based Access Control**: Program operations restricted to authorized accounts
- **Rent Exemption Management**: Ensures proper Solana rent handling for account persistence
- **Compute Budget Optimization**: Manages Solana compute units efficiently for complex operations
- **Multi-layer Validation**: Implements signature verification, nonce checking, and state validation

## Data Storage
- **On-chain State**: Program state, NFT metadata, and transfer records stored directly on Solana
- **PDA-based Addressing**: Uses seed-based account derivation for predictable account addresses
- **Metaplex Compatibility**: Follows Metaplex Token Metadata standards for NFT metadata structure

# External Dependencies

## Blockchain Infrastructure
- **Solana**: Primary blockchain for program deployment and NFT operations
- **ZetaChain**: Cross-chain interoperability protocol and TSS infrastructure
- **EVM Chains**: Ethereum, BSC, Polygon for cross-chain NFT destinations

## Development Framework
- **Anchor**: Solana development framework for program structure and client generation
- **SPL Token Program**: Solana's standard token program for NFT creation and management
- **Metaplex Token Metadata**: Standard for NFT metadata on Solana

## Node.js Dependencies
- **@coral-xyz/anchor**: Framework integration and client SDK
- **@solana/web3.js**: Solana blockchain interaction library
- **@solana/spl-token**: SPL token program interactions
- **TypeScript**: Type-safe development environment
- **Testing Framework**: Mocha and Chai for comprehensive testing

## Cross-Chain Components
- **ZetaChain Gateway Contracts**: Protocol-contracts-solana for cross-chain messaging
- **TSS Network**: Distributed signature verification system
- **Chain Registry**: Support for multiple blockchain networks and address formats
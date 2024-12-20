# Chess AI Implementation Project

![Chess Board](https://raw.githubusercontent.com/zaphodgjd/class-chess-123/main/chess/w_king.png)

## 🎯 Project Overview

This repository contains a skeleton implementation of a Chess AI engine written in C++. The project is designed to teach fundamental concepts of game AI, including board representation, move generation, and basic game tree search algorithms.

### 🎓 Educational Purpose

This project serves as a teaching tool for computer science students to understand:

- Game state representation
- Object-oriented design in C++
- Basic AI concepts in game playing
- Bitboard operations and chess piece movement
- FEN (Forsyth–Edwards Notation) for chess position representation

## 🔧 Technical Architecture

### Key Components

1. **Chess Class**: Core game logic implementation

   - Board state management
   - Move validation
   - Game state evaluation
   - AI player implementation

2. **Piece Representation**

   - Unique identifiers for each piece type
   - Sprite loading and rendering
   - Movement pattern definitions

3. **Board Management**
   - 8x8 grid representation
   - Piece positioning
   - Move history tracking
   - FEN notation support

## 🚀 Getting Started

### Prerequisites

- C++ compiler with C++11 support or higher
- Image loading library for piece sprites
- CMake 3.10 or higher

### Building the Project

```bash
mkdir build
cd build
cmake ..
make
```

### Running Tests

```bash
./chess_tests
```

## 📝 Implementation Details

### Current Features

- Basic board setup and initialization
- Piece movement validation framework
- FEN notation parsing and generation
- Sprite loading for chess pieces
- Player turn management

### Planned Features

- [ ] AI move generation
- [ ] Position evaluation
- [ ] Opening book integration
- [ ] Advanced search algorithms
- [ ] Game state persistence

## 🔍 Code Examples

### Piece Movement Validation

```cpp
bool Chess::canBitMoveFromTo(Bit& bit, BitHolder& src, BitHolder& dst) {
    // TODO: Implement piece-specific movement rules
    return false;
}
```

### FEN Notation Generation

```cpp
const char Chess::bitToPieceNotation(int row, int column) const {
    if (row < 0 || row >= 8 || column < 0 || column >= 8) {
        return '0';
    }
    // Implementation details for FEN notation
}
```

## 📚 Class Assignment Structure

### Phase 1: Board Setup

- Implement piece placement
- Setup initial board state
- Validate board representation

### Phase 2: Move Generation

- Implement basic piece movements
- Add move validation
- Implement special moves (castling, en passant)

### Phase 3: AI Implementation

- Develop position evaluation
- Implement minimax algorithm
- Add alpha-beta pruning
- Basic opening book

## 🤝 Contributing

Students are encouraged to:

1. Fork the repository
2. Create a feature branch
3. Implement assigned components
4. Submit their fork for review

## 🔒 Code Style and Standards

- Use consistent indentation (4 spaces)
- Follow C++ naming conventions
- Document all public methods
- Include unit tests for new features

## 📄 License

This project is licensed under the MIT License.

## 👥 Contributors

- [Your Name] - Initial work
- [Student Names] - Implementation and testing

## 🙏 Acknowledgments

- Chess piece sprites from [Wikipedia](https://en.wikipedia.org/wiki/Chess_piece)
- Original game engine framework by [ocornut](https://github.com/ocornut/imgui)

## Screenshots

[Complete Board](https://raw.githubusercontent.com/jchen577/class-chess-123/main/board.png)
[Moves](https://raw.githubusercontent.com/jchen577/class-chess-123/main/moves.png)

## Changes added

### Added a moves generator that is called
### Moves generator takes 0 arguments and is called when the player clicks on a piece and moves to another spot
### Checks all possible spots for each piece to move, and adds it to a list to be searched
### King moves are generated after calling a kingMoveGenerator() that searches for all the moves from enemy player that puts the current king in danger

## FEN, Castling, and EnPassant
### Added code that reads a FEN string in setupBoard(). Reads the string and places pieces accordingly
### Castling added by adding new booleans to bits to see if they have moved yet. If the king hovers over and open rook, then spawn new piece and delete the old piece
### EnPassant added by adding new bit holders and booleans in chess.h. It checks which direction the enpassant is going, and if the pawn that is being eaten had just last moved and did a 2 move jump

_This README is part of an educational project and is intended to serve as an example of good documentation practices._

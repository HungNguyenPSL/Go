# Go
# Deep Learning Project - IASD Master

This project is part of the [IASD Master Deep Learning Project](https://www.lamsade.dauphine.fr/~cazenave/DeepLearningProject.html). The aim of this project is to train a neural network to play the game of Go.

## Project Overview

The model is trained using self-play data from the Katago Go program. The training set consists of 1,000,000 different games, providing a rich dataset for learning.

### Input Data
The input data consists of 31 planes of size 19x19, representing various aspects of the game:
- Color to play
- Ladder states
- Current board state (on two planes)
- Two previous board states (on four planes)

### Targets
The network is trained to predict two outputs:
- **Policy**: A vector of size 361 (one value for each position on the board), with `1.0` indicating the move played and `0.0` for the other moves.
- **Value**: A scalar indicating the winner, close to `1.0` if White wins and close to `0.0` if Black wins.

### Approaches
The following models were implemented in this project:
- Convolutional Neural Network (CNN)
- ResNet
- MobileNet
- ConvNext Version 1
- ConvNext Version 2
- EfficientFormer (Vision Transformer)

## Contributors

- [@HungNguyen](https://github.com/HungNguyenPSL)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Special thanks to Professor [Tristan Cazenave](https://www.lamsade.dauphine.fr/~cazenave/index.php) for his guidance and support throughout this project.
- Thanks to the [Katago Go](https://katagotools.org/) program for providing the self-play dataset that enabled the training of the model.

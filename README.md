# Neural Complexity tutorial

## Setup Neural Network

Download neural-complexity

    git clone https://github.com/vansky/neural-complexity  

Follow the instructions in that repository for getting `neural-complexity` setup.

Download Gulordava et al., (2018) model  
[GRNN model weights](https://s3.amazonaws.com/colorless-green-rnns/best-models/English/hidden650_batch128_dropout0.2_lr20.0.pt)
    
[GRNN vocab](https://s3.amazonaws.com/colorless-green-rnns/training-data/English/vocab.txt)

Or train a model:

    time python main.py --model_file 'wiki_2_model.pt' --vocab_file 'wiki_2_vocab.txt' --tied \  
    --data_dir './data/wikitext-2/' --trainfname 'train.txt' --validfname 'valid.txt'  

For this tutorial, our model is the Gulordava et al (2018) model.

I've renamed the \*.pt file `grnn.model` and I've renamed the vocab file `grnn.vocab`.

Place the `rrc` and `keys` directories in the `neural-complexity/data` directory.

### Try out the system interactively

    time python main.py --model_file 'grnn.model' --vocab_file 'grnn.vocab' --interact  

### Analyze top-N guesses of the system

    time python main.py --model_file 'grnn.model' --vocab_file 'grnn.vocab' --interact\
    --guess --guessn 3  
    # Add --guessprob to see the probabilities associated with the guesses  

## Check out the python notebook in this directory for additional analyses

Move the python notebook to the `neural-complexity` directory

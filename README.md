# santa-nlp

## Competition Overview
[Santa 2024](https://www.kaggle.com/competitions/santa-2024) is a Kaggle competition where participants are challenged to unscramble words in classic Christmas tales. The goal is to rearrange scrambled word sequences to minimize perplexity and make the stories flow naturally.

## My Approach

### Data Processing
- Used pandas to handle the CSV file containing scrambled text sequences
- Each row contains exactly 6 words that need to be reordered
- Built a bigram language model to understand word relationships

### Language Model Implementation
- Created a bigram model using defaultdict to store word transition probabilities
- Calculated frequencies of word pairs in the training data
- Normalized frequencies to get transition probabilities
- Added smoothing to handle unseen word pairs

### Optimization Strategy
- Implemented a greedy optimization algorithm:
  - Start with initial word sequence
  - Try swapping pairs of words
  - Calculate sequence probability using bigram model
  - Keep swaps that improve probability
  - Continue until no more improvements found
- Used probability scores to evaluate sequence quality

### Key Features
- Row-by-row processing to maintain data integrity
- Direct DataFrame updates for efficient memory usage
- Verification steps to ensure 6-word sequence constraint
- Smoothing to handle zero probabilities

## Skills Practiced

### Natural Language Processing
- Bigram language modeling
- Text sequence probability calculation
- Word tokenization and sequence manipulation

### Python Programming
- Pandas DataFrame operations
- Dictionary and defaultdict usage
- Probability calculations
- Greedy optimization algorithms

### Data Structure Handling
- CSV file I/O
- Text sequence manipulation
- Efficient data updates

### Code Organization
- Clean code practices
- Error handling
- Performance optimization
- Data validation

## Dependencies
- numpy
- pandas
- nltk
- collections (defaultdict)

## Running the Code
1. Download the competition data from Kaggle
2. Ensure all dependencies are installed
3. Run the main script to generate submission file
4. Submission file will maintain original format with reordered words

## Competition Results
Ranked #1027 as an individual out of approximately 2000 individuals/teams.

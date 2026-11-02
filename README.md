# MediQueue: Plain BST vs AVL Tree

## 1. Overview

This lab compares a Plain Binary Search Tree (BST) and an AVL Tree for managing records in the MediQueue system. The experiment evaluates their performance using different input datasets and compares tree height, insertion time, search cost, and rotations.

A Treap is also implemented as a self-learning extension.

## 2. Objectives

- Implement insertion, searching, deletion, and inorder traversal for a Plain BST.
- Implement an AVL Tree with rotations to maintain balance.
- Compare both trees using sequential, random, and nearly sorted datasets.
- Measure insertion time, tree height, average search comparisons, and rotations.
- Visualize and analyze the experimental results.
- Explore a Treap as an additional self-learning activity.

## 3. Technologies Used

- Python
- Google Colab
- Pandas
- Matplotlib

## 4. Dataset and Experimental Setup

The experiment uses three types of datasets:

- **Sequential:** Values are inserted in sorted order.
- **Random:** Values are inserted in a shuffled order.
- **Nearly sorted:** Values are mostly sorted, with a small number of positions swapped.

The dataset sizes used are 1,000, 5,000, and 10,000 records.

## 5. Performance Metrics

- **Insertion Time:** Time taken to insert all records, measured in milliseconds.
- **Tree Height:** Height of the tree after insertion.
- **Average Search Comparisons:** Average number of comparisons required for successful searches.
- **Insertion Rotations:** Number of rotations performed during AVL insertion.
- **Deletion Rotations:** Number of rotations performed during AVL deletion.
- **Height After Deletion:** Tree height after deleting 20% of the records.

## 6. Key Experimental Results

For the dataset containing 10,000 records:

| Dataset | Tree | Height | Average Search Comparisons |
|---|---|---:|---:|
| Sequential | Plain BST | 10,000 | 5,057.190 |
| Sequential | AVL | 14 | 12.463 |
| Random | Plain BST | 31 | 16.565 |
| Random | AVL | 16 | 12.486 |
| Nearly sorted | Plain BST | 545 | 133.681 |
| Nearly sorted | AVL | 15 | 12.552 |

These results show that the Plain BST can become highly unbalanced when values are inserted in sorted or nearly sorted order. The AVL Tree maintains a much smaller height and lower search cost.

## 7. How to Run the Project

1. Open the Jupyter Notebook (`.ipynb`) in Google Colab.
2. Execute all cells in order.
3. Review the comparison table and generated graphs.
4. Check the CSV files and Markdown reports produced by the notebook.
5. Download the notebook and output files for submission.

If required, install the libraries using:

```python
!pip install pandas matplotlib
```

## 8. Self-Learning Extension: Treap

A Treap combines the Binary Search Tree property with randomized priorities. The extension explores its behaviour on sequential input and compares its performance with other tree structures.

## 9. Conclusion

The experiment shows that the Plain BST performs poorly when input values are inserted in sorted order, potentially resulting in a height of 10,000 for 10,000 records. The AVL Tree uses rotations and additional height bookkeeping to maintain balance, reducing search costs significantly.

Although AVL Trees require additional processing during insertion and deletion, they provide more predictable search performance. Therefore, an AVL Tree is recommended for MediQueue when efficient and consistent record searching is important.

## 10. Output Files

Depending on the notebook cells executed, the project may generate:

- `comparison_results.csv`
- `treap_sequential_results.csv`
- `analysis.md`
- `self_learning.md`
- Graph images in `results/graphs/`
- A ZIP archive containing the deliverables


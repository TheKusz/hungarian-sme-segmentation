# Hungarian SME segmentation

Unsupervised and supervised learning on official statistics for Hungarian small and medium enterprises, with a section on what the results mean for SME consultants and support programs. MSc Data Science coursework (Machine Learning)

## Data

KSH (Hungarian Central Statistical Office) table [gsz0018](https://www.ksh.hu/stadat_files/gsz/hu/gsz0018.html): enterprise performance by SME size category, 2013-2023. Indicators are number of enterprises, employees, revenue per employee, net sales, value added, export sales and investment. The file is in [`resources/`](resources)

## Models

- PCA - main axes of variation, PC1 blends value added, revenue, investment and headcount
- K-means, also on the 2 PCA components, evaluated with silhouette scores
- Isolation Forest, also on PCA, to flag unusual SME profiles
- Shallow neural network (MLP classifier)

Each model has results and analysis, and part 4 turns them into business uses such as segmentation, targeted support and early risk detection

## Run

```bash
pip install pandas scikit-learn matplotlib seaborn openpyxl jupyter
jupyter lab hungarian-sme-segmentation.ipynb
```

## Notes

The sample is small, so read it as exploration, not as a prediction model

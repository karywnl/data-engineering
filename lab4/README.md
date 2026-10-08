# Lab 4

Run `lab4.ipynb` from this folder with the **data-engineering** kernel.
It uses `findspark` and the existing PySpark installation. No new packages are needed.

Spark shell check, from the repository root:

```sh
source .venv/bin/activate
spark-shell --master 'local[2]'
```

```scala
sc.parallelize(Seq(1, 2, 3)).sum()
:quit
```

Verified: Spark 4.2.0, Java 21, shell sum `6.0`.

Inputs are in `data/`. `wordcount.txt` is a sample; replace it with your Hadoop
input. MovieLens 100K is from [GroupLens](https://grouplens.org/datasets/movielens/100k/);
the local `u.data` was downloaded from a [mirror](https://github.com/jsnowacki/SPARK/blob/master/data/ml-100k/u.data)
because the official server was unreachable. Raw MovieLens data is excluded from Git.
See the [dataset README](https://files.grouplens.org/datasets/movielens/ml-100k-README.txt)
for attribution and usage terms.

The temperature results follow the CSV's headers and preserve its numeric units.
`stationID` contains date-like values. Full results remain in the notebook's
variables; only the movie output is limited to a ten-row preview.

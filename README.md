# Data engineering practice

## PySpark in VS Code

Run `uv sync`, open `pyspark_getting_started.ipynb`, and choose the
**data-engineering** kernel at the top right. Run the cells from top to bottom.
The notebook sets Java and its Spark worker to the matching Python interpreter.

Use a notebook while exploring data or learning Spark. For repeatable programs,
put the same PySpark code in a `.py` file and run it with `uv run python file.py`
from this folder. Both use the same Spark DataFrame API.

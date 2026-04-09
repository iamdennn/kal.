# SISTEM PERSAMAAN LINIER

Whether you write your book's content in Jupyter Notebooks (`.ipynb`) or
in regular markdown files (`.md`), you'll write in the same flavor of markdown
called **MyST Markdown**.
This is a simple file to help you get started and show off some syntax.

## Mencari A invesrt Pada Matrix 4x4

1. Matriks Awal
Misalkan matriks tersebut adalah A :
$$
\left[\begin{array}{cccc|cccc} 
1 & 1 & 1 & 1 & 1 & 0 & 0 & 0 \\ 
2 & -1 & 1 & -1 & 0 & 1 & 0 & 0 \\ 
1 & 2 & -1 & 1 & 0 & 0 & 1 & 0 \\ 
3 & -1 & 2 & 1 & 0 & 0 & 0 & 1 
\end{array}\right]
$$

2. Proses Eliminasi Gauss-Jordan
Kita sandingkan matriks 
 dengan matriks identitas 
, lalu lakukan operasi baris dasar untuk mengubah sisi kiri menjadi matriks identitas.
Setelah melalui serangkaian operasi baris (eliminasi), kita mendapatkan nilai determinan matriks ini adalah 13.

3. Invers dari matriks 
 adalah:
$$
A^{-1} = \frac{1}{13} \begin{bmatrix} 
-3 & 3 & 4 & 2 \\ 
9 & 4 & 1 & -6 \\ 
11 & 2 & -6 & -3 \\ 
-4 & -9 & 1 & 7 
\end{bmatrix}
$$

atau dalam bentuk desimal

$$
A^{-1} \approx \begin{bmatrix} 
-0,23 & 0,23 & 0,31 & 0,15 \\ 
0,69 & 0,31 & 0,08 & -0,46 \\ 
0,85 & 0,15 & -0,46 & -0,23 \\ 
-0,31 & -0,69 & 0,08 & 0,54 
\end{bmatrix}
$$

## Sample Roles and Directives

Roles and directives are two of the most powerful tools in Jupyter Book. They
are like functions, but written in a markup language. They both
serve a similar purpose, but **roles are written in one line**, whereas
**directives span many lines**. They both accept different kinds of inputs,
and what they do with those inputs depends on the specific role or directive
that is being called.

Here is a "note" directive:

```{note}
Here is a note
```

It will be rendered in a special box when you build your book.

Here is an inline directive to refer to a document: {doc}`markdown-notebooks`.


## Citations

You can also cite references that are stored in a `bibtex` file. For example,
the following syntax: `` {cite}`holdgraf_evidence_2014` `` will render like
this: {cite}`holdgraf_evidence_2014`.

Moreover, you can insert a bibliography into your page with this syntax:
The `{bibliography}` directive must be used for all the `{cite}` roles to
render properly.
For example, if the references for your book are stored in `references.bib`,
then the bibliography is inserted with:

```{bibliography}
```

## Learn more

This is just a simple starter to get you started.
You can learn a lot more at [jupyterbook.org](https://jupyterbook.org).

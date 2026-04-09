{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "from matplotlib import rcParams, cycler\n",
    "import matplotlib.pyplot as plt\n",
    "import numpy as np\n",
    "plt.ion()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Fixing random state for reproducibility\n",
    "np.random.seed(19680801)\n",
    "\n",
    "N = 10\n",
    "data = [np.logspace(0, 1, 100) + np.random.randn(100) + ii for ii in range(N)]\n",
    "data = np.array(data).T\n",
    "cmap = plt.cm.coolwarm\n",
    "rcParams['axes.prop_cycle'] = cycler(color=cmap(np.linspace(0, 1, N)))\n",
    "\n",
    "\n",
    "from matplotlib.lines import Line2D\n",
    "custom_lines = [Line2D([0], [0], color=cmap(0.), lw=4),\n",
    "                Line2D([0], [0], color=cmap(.5), lw=4),\n",
    "                Line2D([0], [0], color=cmap(1.), lw=4)]\n",
    "\n",
    "fig, ax = plt.subplots(figsize=(10, 5))\n",
    "lines = ax.plot(data)\n",
    "ax.legend(custom_lines, ['Cold', 'Medium', 'Hot']);"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {
    "editable": true,
    "slideshow": {
     "slide_type": ""
    },
    "tags": []
   },
   "source": [
    "**SISTEM PERSAMAAN LINIER**"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "There is a lot more that you can do with outputs (such as including interactive outputs)\n",
    "with your book. For more information about this, see [the Jupyter Book documentation](https://jupyterbook.org)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "1.1 Sistem Persamaan Linear\n",
    "Menghitung dan mempelajari solusi dari persamaan, serta sistem persamaan, pastinya memainkan peran penting dalam matematika; meskipun kami perlu segera menambahkan bahwa ini bukanlah satu-satunya hal yang dilakukan matematikawan! Dalam bab ini, kita akan mengembangkan teori yang pada dasarnya lengkap tentang keluarga persamaan matematika yang sangat sederhana: yaitu, persamaan linear. Ini akan berfungsi sebagai pengantar tidak langsung bagi studi aljabar linear kita, karena di balik deskripsi parametrik dari solusi sistem linear terdapat konsep-konsep ruang vektor seperti subruang (subspace), rentang (span), dan kebebasan linear (linear independence). Selanjutnya, kita akan bertemu dengan salah satu alat komputasi terpenting dalam aljabar linear: eliminasi Gauss.\n",
    "\n",
    "\n",
    "Definisi 1.1.1. Persamaan linear. Sebuah ekspresi linear dalam \n",
    " variabel yang tidak diketahui (atau peubah) \n",
    " adalah ekspresi dalam bentuk\n",
    "\n",
    "di mana \n",
    " adalah bilangan real tetap.\n",
    "Sebuah persamaan linear dalam variabel \n",
    " adalah persamaan yang dapat disederhanakan, hanya dengan menggunakan penjumlahan dan pengurangan, menjadi persamaan dalam bentuk\n",
    "\n",
    "yang kita sebut sebagai bentuk standar. Sebuah persamaan dalam variabel \n",
    " dikatakan non-linear jika tidak dapat disederhanakan ke bentuk (1.1.1) hanya dengan menggunakan penjumlahan dan pengurangan.\n",
    "Diberikan sebuah persamaan linear dengan bentuk standar (1.1.1), persamaan tersebut disebut homogen jika \n",
    ", dan non-homogen jika \n",
    ".\n",
    "Contoh 1.1.2. Persamaan linear dan non-linear.\n",
    "Perhatikan \n",
    ". Ini adalah persamaan linear dalam variabel \n",
    ". Bentuk standarnya adalah \n",
    ". Karena ruas kanan tidak bernilai nol, kita dapat melihat bahwa persamaan tersebut adalah non-homogen.\n",
    "Persamaan \n",
    " adalah persamaan non-linear dalam variabel \n",
    " dan \n",
    ".\n",
    "\n",
    "Definisi 1.1.3. Sistem persamaan linear. Sebuah sistem persamaan linear (atau sistem linear) adalah sekumpulan persamaan linear.\n",
    "Sebuah sistem linear homogen adalah sekumpulan persamaan linear homogen.\n",
    "Saat menampilkan sistem yang terdiri dari \n",
    " persamaan dengan \n",
    " variabel tidak diketahui \n",
    ", kita biasanya menulis setiap persamaan dalam bentuk standar dan menyejajarkan suku-suku yang bersesuaian dari setiap persamaan ke dalam kolom-kolom:\n",
    "\n",
    "Dengan demikian, sistem homogen biasanya ditulis sebagai:\n",
    "\n",
    "\n",
    "Catatan 1.1.4. Anda sebaiknya membiasakan diri dengan penggunaan indeks ganda (double-indexing) untuk menampilkan sistem linear sesegera mungkin. Berikut adalah cara yang baik untuk memahaminya:\n",
    "Indeks \n",
    " yang muncul pada \n",
    " dan \n",
    " menunjukkan baris ke-\n",
    " dalam sistem yang ditampilkan, atau secara ekuivalen, persamaan ke-\n",
    ".\n",
    "Indeks \n",
    " yang muncul pada \n",
    " menunjukkan kolom ke-\n",
    " dalam sistem yang ditampilkan, yang dikaitkan dengan variabel ke-\n",
    ", untuk \n",
    ".\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.14.3"
  },
  "widgets": {
   "application/vnd.jupyter.widget-state+json": {
    "state": {},
    "version_major": 2,
    "version_minor": 0
   }
  }
 },
 "nbformat": 4,
 "nbformat_minor": 4
}

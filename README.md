# **GSEA Analyses**

This section outlines advanced RNA-Seq analysis steps, including adding gene symbols and Entrez IDs to results, performing Gene Set Enrichment Analysis (GSEA), and visualizing significant pathways.

## **Part 2: Adding Gene Symbols and Entrez IDs**

We begin by enhancing the results by adding gene symbols and Entrez IDs using the `org.Hs.eg.db` library from Bioconductor.

### **Step 1: Install Required Libraries**

Ensure that the necessary libraries like `org.Hs.eg.db` and `AnnotationDbi` are installed, as they allow conversion between various gene ID types.

### **Step 2: Mapping Gene Symbols and Entrez IDs**

After loading the required libraries, you will use the `mapIds` function to map Ensembl IDs to gene symbols and Entrez IDs. The resulting data can then be ordered by adjusted p-values for clarity. Finally, save the modified results to a file.

## **Gene Set Enrichment Analysis (GSEA)**

This section explains how to perform GSEA using the `clusterProfiler` and `msigdbr` packages to find enriched biological pathways.

### **Step 1: Install GSEA-related Libraries**

Make sure the `clusterProfiler` and `msigdbr` libraries are installed to perform GSEA and access gene sets for enrichment analysis.

### **Step 2: Set Up GSEA**

Prepare your working directory by creating a folder for GSEA results. Ensure the dataset is formatted correctly, particularly by organizing genes and expression data.

### **Step 3: Mapping Ensembl IDs to Gene Symbols**

Convert Ensembl gene IDs to gene symbols using the same method as in the previous step. Clean the data by filtering out any unmapped or duplicated entries.

### **Step 4: Remove Duplicate Gene Symbols**

Check for and remove duplicate gene symbols to prevent errors in enrichment analysis. Duplicates are often removed by sorting the gene list based on the absolute log2 fold change values.

### **Step 5: Perform GSEA**

Rank the gene list by log2 fold change values, and run GSEA using the Hallmark gene sets from the `msigdbr` package. Hallmark gene sets are collections of genes grouped by biological functions.

### **Step 6: Visualize GSEA Results**

The most significant pathways can be visualized using plots. For instance, you can generate GSEA plots for the top positively and negatively enriched pathways.

### **Step 7: Save GSEA Results**

After completing the GSEA, export the results to a file for future reference and further analysis.

## **License**

This project is licensed under the MIT License.

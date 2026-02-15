# Graph Files

This directory contains the graph data files used by the GLaDiGAtor project. Some files are compressed due to their large size (over 100MB) to optimize storage and transfer efficiency.

## Important: Unzip Files First

Before running any project, you must unzip the compressed files in this directory:

### Compressed Files
- `Graph_Own_0.5.pt.7z`
- `Graph_Own_0.05.pt.7z`
- `Graph_Own_0.1.pt.7z`
- `Graph_Comparison_SkipGNN.7z`
- `Graph_Comparison_OGB.7z`

### Unzip Commands

#### Linux/Mac
```bash
# Install p7zip-full package
sudo apt install p7zip-full

# Extract the compressed files
7z e Graph_Own_0.5.pt.7z
7z e Graph_Own_0.05.pt.7z
7z e Graph_Own_0.1.pt.7z
7z e Graph_Comparison_SkipGNN.7z
7z e Graph_Comparison_OGB.7z
```

#### Windows
Use 7-Zip application to extract all .7z files

## File Descriptions

### Graph_Own_*.pt
Graph files created by the GLaDiGAtor model with different gene-disease score thresholds:

- `Graph_Own_0.5.pt`: DisGeNET graph with gene-disease score threshold ≥ 0.5 (Graph 2)
- `Graph_Own_0.1.pt`: DisGeNET graph with gene-disease score threshold ≥ 0.1 (Graph 3)
- `Graph_Own_0.05.pt`: DisGeNET graph with gene-disease score threshold ≥ 0.05 (Graph 4)

### Graph_Comparison_*.7z
Graph files used for comparison with other methods:

- `Graph_Comparison_SkipGNN.7z`: DisGeNET graph (curated gene-disease associations) for comparison with baseline methods (Graph 5)
- `Graph_Comparison_OGB.7z`: Open Graph Benchmark (OGB) protein-disease associations (ogbl-biokg) dataset (Graph 6)

### GeneFeatures_Uniref50.csv
Gene features extracted using UniRef50 clustering.

## Generated Files

### generated-negative-egdes/
Directory containing generated negative edge files for different graph versions:
- `generatedNegativeEdges_Graph_Comparison_OGB.pt`
- `generatedNegativeEdges_Graph_Comparison_SkipGNN.pt`
- `generatedNegativeEdges_Graph_Own_0.1.pt`
- `generatedNegativeEdges_Graph_Own_0.05.pt`
- `generatedNegativeEdges_Graph_Own_0.5_x.pt`
- `generatedNegativeEdges_Graph_Own_0.5.pt`
- `generatedNegativeEdges_Graph_Own_0.9.pt`

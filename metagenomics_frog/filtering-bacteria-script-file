qiime taxa filter-table \
  --i-table filtered_seqs/feature-frequency-filtered-table.qza \
  --i-taxonomy taxonomy/taxonomy.qza \
  --p-include p__ \
  --p-exclude mitochondria,chloroplast \
  --o-filtered-table filtered_seqs/table-no-mitochondria-chloroplast.qza

qiime taxa filter-table \
  --i-table filtered_seqs/table-no-mitochondria-chloroplast.qza \
  --i-taxonomy taxonomy/taxonomy.qza \
  --p-exclude "k__Archaea" \
  --o-filtered-table filtered_seqs/table-no-mitochondria-chloroplast-archaea.qza

qiime taxa filter-table \
  --i-table filtered_seqs/table-no-mitochondria-chloroplast-archaea.qza \
  --i-taxonomy taxonomy/taxonomy.qza \
  --p-exclude "k__Eukaryota" \
  --o-filtered-table filtered_seqs/filtered-table.qza

qiime taxa filter-seqs \
  --i-sequences denoised_data/rep-seqs.qza \
  --i-taxonomy taxonomy/taxonomy.qza \
  --p-include p__ \
  --p-exclude mitochondria,chloroplast \
  --o-filtered-sequences filtered_seqs/rep-seqs-no-mitochondria-chloroplast.qza

qiime taxa filter-seqs \
  --i-sequences filtered_seqs/rep-seqs-no-mitochondria-chloroplast.qza \
  --i-taxonomy taxonomy/taxonomy.qza \
  --p-exclude "k__Archaea" \
  --o-filtered-sequences filtered_seqs/rep-seqs-no-mitochondria-chloroplast-archaea.qza

qiime taxa filter-seqs \
  --i-sequences filtered_seqs/rep-seqs-no-mitochondria-chloroplast-archaea.qza \
  --i-taxonomy taxonomy/taxonomy.qza \
  --p-exclude "k__Eukaryota" \
  --o-filtered-sequences filtered_seqs/filtered-rep-seqs.qza

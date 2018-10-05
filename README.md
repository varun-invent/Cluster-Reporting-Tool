# Cluster Reporting Tool

In the field of neuroimaging, the current trend of how the connectivity results are reported in literature suffers from reproducibility.  We feel that it is partly because of the reporting strategy. Usually, the clusters on a brainmap are reported in the form of a table. This table generally specifies the cluster by its peak copordinates, name of the region where the peak coordinates lie and count of number of voxels. The authhors generally do not specify the atlas employed for reporting the regions. For a specific coordinate, different atlases can give different regions. For example, [12, 44, 19] corresponds to  right medial frontal gyrus according to Talairaich-Tournoux atlas and right anterior cingulate cortex according to CA_ML_18_MNIA atlas (AFNI). So the study becomes non-reproducible if we go by just the names of the regions mentioned. So better reporting methods need to be devised. We suggest following one atlas for both the analysis and reporting the results. Just reporting the names of regions where the cluster spans is not sufficient, the representative coordinates for each part of the cluster that spans different brain regions should also be mentioned.

Cluster Reporting Tool is a python based tool for automatic generation of report specifying the details of the clusters of brain activations spanning multiple regions of the brain. This tool helps automatically report the results using our proposed standard.

### Usage:

TBD





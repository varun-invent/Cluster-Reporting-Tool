# CRT: Cluster Reporting Tool

In the field of neuroimaging, the current trend of how the connectivity results are reported in literature suffers from reproducibility.  We feel that it is partly because of the reporting strategy. Usually, the clusters on a brainmap are reported in the form of a table. This table generally specifies the cluster by its peak copordinates, name of the region where the peak coordinates lie and count of number of voxels. The authhors generally do not specify the atlas employed for reporting the regions. For a specific coordinates, different atlases can give different regions. For example, the MNI coordinates [12, 44, 19] corresponds to  right medial frontal gyrus according to Talairaich-Tournoux atlas and right anterior cingulate cortex according to CA_ML_18_MNIA atlas (AFNI). So the study becomes non-reproducible if we go by just the names of the regions mentioned. So better reporting methods need to be devised. We suggest following one atlas for both the analysis and reporting the results. Just reporting the names of regions where the cluster spans is not sufficient, the representative coordinates for each part of the cluster that spans different brain regions should also be mentioned.

Cluster Reporting Tool is a python based tool for automatic generation of report specifying the details of the clusters of brain activations spanning multiple regions of the brain. This tool helps automatically report the results using our proposed standard. For a given brain map, it first finds clusters. Then for each cluster, it finds the span of cluster, i.e., how many atlas regions overlap with the cluster. For each region covered, it finds the number and percentage of voxels it covers and reports the peak coordinates closest to centre of gravity of the voxels in that overlap. 


### Usage:

```>>> python3 cluster_reporting_tool.py -c <contrast_input_brain_map.nii.gz> -t <threshold> -v <volume number>```

**Note**: Currently it thresholds similar to FSL. That is, it takes as input one threshold value and then clips the brain voxels with values lying in between (-ve) threshold value and (+ve) threshold value. Clusters are found with the remaining voxels. 




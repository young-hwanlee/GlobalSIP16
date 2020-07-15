# Online Robust Subspace Clustering for Analyzing Incomplete Synchrophasor Measurements
Published in: 2016 IEEE Global Conference on Signal and Information Processing (GlobalSIP). For more information, please refer to the paper.

* Tools: PSS/E, MATLAB

## Abstract
Phasor measurement units (PMUs) are instrumental for grid monitoring thanks to high sampling rates and precise synchronization. However, collecting and analyzing the PMU data are challenging due to the large volume, computational burden, and missing measurements. In this work, a robust subspace clustering model is adopted to perform reconstruction of missing measurements while simultaneously detecting outliers, which may be due to grid abnormalities or cyber-attacks. To mitigate the computational burden and processing delay of batch computation, an online algorithm is derived based on stochastic approximation. The storage cost of the signal templates (dictionary) used for representing the data is reduced via sparsiﬁcation and pruning procedures. Numerical tests using simulated PMU data validate the performance of the proposed approach.

## Dataset and Results (Reconstruction and Outlier Detection)
The algorithms were tested using simulated PMU data from the PSS/E simulator. The simulated power system consists of 23 buses and 6 generators. (For detail, see [1].) Only the voltage magnitudes are used for simplicity to construct the measurements Z (shown in the top panel in the figures below). A line trip was simulated at 10 sec, which caused oscillations across the symstem. The line was closed at 70 sec. The two events were replicated once more at 110 sec and 170 sec, respectively. The middle and bottom panel show the reconstruction from the data with 5% missing entries and outlier detection, respectively. 
![case1_Z_Zhat_E_sp_prun](https://user-images.githubusercontent.com/67979833/87259548-1ecc9680-c47a-11ea-8989-94193f5ceda6.png)

## Mean Square Error Performance vs Dictionary Size
As a performance metric, the average normalized mean-square error (MSE) was used as the dictionary (linear combination of a set of template vectors, called atoms) size is varied:
![online_synthetic_no_outliers_mse_vs_M_v2](https://user-images.githubusercontent.com/67979833/87259927-b59a5280-c47c-11ea-862b-9ec5b84c6092.png)
where
* Fixed dictionary: dictionary constructed by randomly sampling from Z and fixed  
* Pruning only: dictionary initially constructed with a few random data vectors, but subsequently updated through the pruning procedure with the maximum budget set  
* Sparsification + pruning: dictionary (simiarly to pruning only) initially constructed with a few random data vectors, updated only when it is deemed to sufficiently contribute to the diversity based on some appropriated metric (and then, updated through the pruning procedure)

## References
[1] S.-J. Kim, Y. Lee, and K. Y. Lee, "Robust subspace approaches for analyzing incomplete synchrophasor measurements,” in Proc. of the 9th IFAC Symposium on Control of Power and Energy Systems, New Delhi, India, Dec. 2015, pp. 120–125.

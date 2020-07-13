# Online Robust Subspace Clustering for Analyzing Incomplete Synchrophasor Measurements
Published in: 2016 IEEE Global Conference on Signal and Information Processing (GlobalSIP). For more information, please refer to the paper.

## Dataset and Results
The algorithms were tested using simulated PMU data from the PSS/E simulator. The simulated power system consists of 23 buses and 6 generators. (For detail, see [1].) Only the voltage magnitudes are used for simplicity to construct the measurements Z (shown in the top panel in the figures below). A line trip was simulated at 10 sec, which caused oscillations across the symstem. The line was closed at 70 sec. The two events were replicated once more at 110 sec and 170 sec, respectively. The middle and bottom panel show the reconstruction from the data with 5% missing entries and outlier detection, respectively.

![case1_Z_Zhat_E_sp_prun](https://user-images.githubusercontent.com/67979833/87259548-1ecc9680-c47a-11ea-8989-94193f5ceda6.png)

## Reference
[1] S.-J. Kim, Y. Lee, and K. Y. Lee, "Robust subspace approaches for analyzing incomplete synchrophasor measurements,” in Proc. of the 9th IFAC Symposium on Control of Power and Energy Systems, New Delhi, India, Dec. 2015, pp. 120–125.

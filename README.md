## Multiple Hypothesis Tracking

**This repository is forked from yoon28/pymht[https://github.com/mollyzyy787/pymht]**

This is an implementation of the Multiple Hypothesis Tracking (MHT) algorithm [1, 2, 3].
Check the `main.py`, the demonstration of MHT using counterfeit detections will be shown.

Notes:
- in `main.py`, on `canvas`, fp (false alarms) are drawn in red boxes and tp (true positives) are drawn in blue boxes. `obstacle` is an off-white rectangle fixed in position. There are by default 3 true targets that moves slowly and 1 dynamic true targets that circles around the field. The true target patches are generated by random noise with a different `mu`.
- tracking steps:
  - updateTrackTrees (0.1-0.2s)
  - makeConflictList (<1ms)
  - clustering (<1ms)
  - compBestHypoSet (4ms)
  - treePruning (<1ms)
  - branchMerging (<1ms)


## Dependency

- opencv, numpy
- [anytree](https://anytree.readthedocs.io/en/latest/)
- [gurobi](https://www.gurobi.com/) or [cvxpy](https://www.cvxpy.org/)

## Reference

- [1] Blackman, Samuel, and Robert Popoli. "Design and analysis of modern tracking systems(Book)." Norwood, MA: Artech House, 1999. (1999).
- [2] Yoon, Kwangjin, Young-min Song, and Moongu Jeon. "Multiple hypothesis tracking algorithm for multi-target multi-camera tracking with disjoint views." IET Image Processing 12.7 (2018): 1175-1184.
- [3] Kim, Chanho, et al. "Multiple hypothesis tracking revisited." Proceedings of the IEEE International Conference on Computer Vision. 2015.

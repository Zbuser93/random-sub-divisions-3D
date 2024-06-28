# random-sub-divisions-3D

This is a macro for FreeCAD which randomly sub-divides a predetermined volume into a predetermined number of roughly even sub-volumes.
It works by first creating a "case" which fills the whole volume, then it continuously finds the largest case and cuts it randomly along its longest dimension until the desired number of cases is reached.
It uses a normal distribution to determine its random cut location, with the mean being in the middle of the case and 1 SD being 1/6th of the length of that dimension.
It also computes a minimum allowable dimension length by dividing the total volume by the number of cases, taking the cube root of that, and dividing that by 3.
The normal distribution and minimum case dimension result in very satisfying, even cases filling the whole volume.
I made this to generate 3D models of random, hypothetical multi-SKU pallets to aid in the creation of a new algorithm for determining optimal case stacking order (I work in logistics automation).
I will be using this to study stacking order problems, and future updates to test stacking order algorithms.
Future versions will take an ordered list of cases from a stacking algorithm, and make the cases appear one at a time in order to verify the effectiveness of the algorithm.
Current case numbering has nothing to do with optimal pallet stacking, and instead indicates the order in which the macro created the case.

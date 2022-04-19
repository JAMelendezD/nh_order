# NH Generalized Order Parameter

Calculates the generalized order parameter using the autocorrelation function of the NH vectors (requires well-fitted trajectory) or using the iRED procedure applied to the NH vectors. 

<p align="center">
  <img width="400" src="images/nh_vectors.png">
</p>

## Autocorrelation


$$x + y$$

```
python nh_order.py protein.tpr protein_nj_fit.xtc 5000 10000 "name N and not resname PRO and not resid 1" "name H and not resname PRO and not resid 1" 2 ./data/ --mode 0 --lenacf 100
```

<p align="center">
  <img width="400" src="images/acf_0_100_2.png">
  <img width="400" src="images/acf_0_1000_2.png">
</p>

```
python nh_order.py protein.tpr protein_nj_fit.xtc 5000 10000 "name N and not resname PRO and not resid 1" "name H and not resname PRO and not resid 1" 2 ./data/ --mode 1 --lenacf 100
```

<p align="center">
  <img width="400" src="images/acf_1_100_2.png">
  <img width="400" src="images/acf_1_1000_2.png">
</p>

## iRED

```
python nh_order.py protein.tpr protein_nj_fit.xtc 5000 10000 "name N and not resname PRO and not resid 1" "name H and not resname PRO and not resid 1" 2 ./data/ --mode 2
```

<p align="center">
  <img width="400" src="images/ired_mat_1.png">
  <img width="400" src="images/ired_mat_2.png">
</p>

## Order parameter

<p align="center">
  <img width="800" src="images/NH_order_models.png">
  <img width="800" src="images/NH_order_all.png">
  <img width="800" src="images/NH_order_block.png">
</p>
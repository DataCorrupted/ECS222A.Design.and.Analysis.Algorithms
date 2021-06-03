# Matching.Nuts.and.Bolts

[slides](https://drive.google.com/file/d/1kjvZ4Gtqp0gPiNC9kQimDTjReieTEn2P/view?usp=sharing)

[video](https://ucdavis.zoom.us/rec/share/i3nrIU4dfJgl3Bv8YKDgD_ZZiBZ0H5GPpQBzk9EzfZR1CqIw4uNX2uc6XUAnw3U.Fdpv7dSQk4XOGGZ1?startTime=1622162856000)

## Summary 

This paper designs an algorithm that finds correspondance of a pile of mixed nuts and bolts.
The hardship in this problem is that the size of bolts(or nuts) can't be directly compared, thus sorting won't work.
A brute force way is to compare them one by one and have a time complexity of `O(n^2)`.
A quick sort algorithm is to pick a bolts and calssify the rest nuts as two piles: larger and smaller.
However, it's hard to pick a pivot. 
A bunch of bad pivots can roll the algorithm back to `O(n^2)`.

The algorithm is based on a modified version of quick sort.
The core idea is to find a proper pivot that can divide the pile.
First they construct a bigraph, where one side is bots and the other is nuts.
Then they find an approximate median in the pile.
They proved that the algorithm runs in `O(n log^2 n)`.

## Reference

```
@inproceedings{alon1994matching,
  title={Matching nuts and bolts},
  author={Alon, Noga and Blum, Manuel and Fiat, Amos and Kannan, Sampath and Naor, Moni and Ostrovsky, Rafail},
  booktitle={SODA},
  pages={690--696},
  year={1994},
  organization={Citeseer}
}
```
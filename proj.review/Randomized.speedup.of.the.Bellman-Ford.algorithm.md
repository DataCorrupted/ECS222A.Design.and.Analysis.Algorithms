# Randomized.speedup.of.the.Bellman–Ford.algorithm

[slides](https://docs.google.com/presentation/d/1uv7eV0P-H3VyVi4F1HjcXemHsfyCakHDi5MKAbvmQvo/edit?usp=sharing)

[video](https://drive.google.com/file/d/1R535jus9ewiRQq9v-u3O1le01MNBx4aJ/view?usp=sharing)

## Summary

This presentation talks about a speed up algorithm of bellman-Ford algorithm.

They first established that the change is based on constant time improvements, thus the big O notation is still `O(n^3)`. 
An intuitive improvement is that after `i`-th iteration, `i` destination should be minimized, thus the loop time can be redused. 
Yen's algorithm further reduced the loop time from `|V|-1` to `|V|/2`.

This papre further improved Yen's algorithm. 
The selection of the edges are random.
They proved that with probability at least `1-1/n^c`, the relaxations is at most `nm/3 + m`.

## Reference

```
@article{DBLP:journals/corr/abs-1111-5414,
  author    = {Michael J. Bannister and
               David Eppstein},
  title     = {Randomized Speedup of the Bellman-Ford Algorithm},
  journal   = {CoRR},
  volume    = {abs/1111.5414},
  year      = {2011},
  url       = {http://arxiv.org/abs/1111.5414},
  archivePrefix = {arXiv},
  eprint    = {1111.5414},
  timestamp = {Mon, 13 Aug 2018 16:46:02 +0200},
  biburl    = {https://dblp.org/rec/journals/corr/abs-1111-5414.bib},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}
```
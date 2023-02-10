---
id: xfayuqwz8zd1ulxd8gv90yo
title: '2023-02-10'
desc: ''
updated: 1676041553875
created: 1676020825031
traitIds:
  - open-notebook-mvisani
---
# This is Marco's daily open-notebook.

Today is 2023.02.10

## Todo today

## Theory and ideas of the project
We seek to infer the presence or absence of $M$ metabolites in $S$ species. We denote by $x_{sm}$ whether metabolite $m=1,\ldots,M$ is present ($x_{sm}=1$) or absent ($x_{sm}=0$) in species $s=1,\ldots,S$. To infer the full vector $\bm{x}=(x_{11}, \ldots, x_{1M},\ldots,x_{SM})$, we assume that related species share a similar set of metabolites and that metabolites related in their synthesis share a similar distribution across species. 
Let ${\mathbb P}(x_{sm}=1|y_{sm})=y_{sm}$ be the probability with which metabolite $m$ is present in species $s$. We then assume that

$$
logit \space y_{sm} = \mu_m + \epsilon_{sm}
$$

where $\mu$ is a metabolite-specific intercept and $\epsilon_{sm}$ is normally distributed with mean 0 and co-variance $cov(\epsilon_{sm},\epsilon_{s'm'})=\alpha \sigma_{ss'} + \beta \sigma_{mm'}$ between each combination of species and metabolite. Here, $\sigma_{ss'}$ and $\sigma_{mm'}$ are known measures of covariance between species $s$ and $s'$ and between metabolites $m$ and $m'$, respectively, and $\alpha$ and $\beta$ are positive scalars.

We consider two sets of data informative about $\bm{x}$: i) Presence-absence data obtained with mass-spectrometry and ii) presence-only reports of specific metabolites in specific specie. Let $\bm{d_{sj}}=(d_{sj1}, \ldots, d_{sjM})$ be the presence-absence vector of each metabolite $m$ obtained with mass-spectrometry run $j=1,\ldots,J_s$ performed on species $s$. Assuming a false-positive and false-negative error rates $\epsilon_{01}$ and $\epsilon_{10}$, respectively, we have

$$
{\mathbb P}(\bm{d_{sj}}|\bm{x}, \epsilon_{01}, \epsilon_{10}) = \prod_m \left[ x_{sm}\left(\epsilon_{10}^{1-d_{sjm}}(1-\epsilon_{10})^{d_{sjm}}\right) + (1-x_{sm})\left( \epsilon_{01}^{d_{sjm}}(1-\epsilon_{01})^{1-d_{sjm}}\right)\right].
$$

To model the presence only data, it must be put in relation to the expected research effort. Let $p_{sm}$ denote the known number of presence-only reports for metabolite $m$ in species $s$ and $n_{sm}$ the unknown number of research projects that aimed at discovering metabolite $m$ in species $s$. Assuming a false-positive and false-negative error rates $\pi_{01}$ and $\pi_{10}$, respectively, we have

$$
{\mathbb P}(p_{sm}|n_{sm}, \pi_{01}, \pi_{10}) = ...
$$

###
###

## Doing

## Paused

## Done
Change `prepare_pseudoabsence_tables.R` in order to have a csv table and not a space separated data. 

## Notes
"ref/noref, children/nochildren" mean if you take into account multiple reference (and children) or not.

So, for example: 2 articles report amarogentin in *Gentiana lutea*, 3 (of which 1 is the same) in *Gentiana acaulis*.

Then, for the pair amarogentin in *Gentiana*:
* ref_child: 5
* ref_nochild: 4
* noref_child: 2
* noref_nochild: 1

## Todo tomorrow

###
###
###


## Today I learned that

- 
---
id: s5ghfvJKYE4vBKA7sYDki
title: Reviews
desc: ''
updated: 1630580070782
created: 1630169573436
---
One of the reviewers' comments was that the LOTUS manuscript lacked presentation of practical applications.


In order to adress we could take recent example of classical NP reviews saying "in the last x years z compounds have been isolated from source z" see Table 1.
And see how a LOTUS based query would compare.

Looked for 'natural products of actinobacteria review' in 2021  https://scholar.google.ch/scholar?as_ylo=2021&q=natural+products+of+actinobacteria+review&hl=en&as_sdt=0,5

Found this one : 
https://reader.elsevier.com/reader/sd/pii/S0944501321000148?token=12BB9774EF1AF4C4D7387565CBC96DC31DE1BF26C75CDDAF82A56D2AB0AE1F8ED050ABC8F3131097C646B9F5A06A1DD1&originRegion=eu-west-1&originCreation=20210828164327

Let's try to build Table 1 on our side. 


All compounds from Actinobacteria (and childrens) with DOI https://w.wiki/3yPg
Now lets refine by years

This looks like a way to narrow by dates https://stackoverflow.com/questions/52550929/fast-publication-date-lookup-with-wikidata-query-service



### Called Adriano


Mode op for reproducible min example

https://gitlab.com/lotus7/lotus-processor.git

from the home dir 

lotus-processor git:(main) make -C src/1_gathering/db -B alkamid
returns

make: *** No rule to make target `/1_gathering/db/alkamid/standardizing.R', needed by `/interim/db/alkamid.tsv.gz'.  Stop.

readr needs to be >2.0 

lets see how to update a condaforge package since readr condaforge is not updated
https://conda-forge.org/docs/maintainer/updating_pkgs.html


git clone https://github.com/conda-forge/r-readr-feedstock.git


wget -O- https://cran.r-project.org/src/contrib/readr_2.0.1.tar.gz | shasum -a 256


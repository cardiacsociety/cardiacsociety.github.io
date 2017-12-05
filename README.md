# cardiacsociety.github.io

Overview of web services projects and resources for [CSANZ](http://www.csanz.edu.au).

* [HeartOne Stats](#heartone-stats)
* [HeartOne WebApp](#heartone-webapp)
* [MappCPD API](#mappcpd-api)
* [Pubmed Resources](#pubmed-resources)


## HeartOne Stats

* HeartOne Usage - https://cardiacsociety.github.io/h1-stats/

* Most Popular Resource Links
  * http://csanz.io/popular.html (top 20 by default)
  * http://csanz.io/popular.html?n=50 (top 50, set n as required)
 
* Latest Indexed Resources
  * http://csanz.io/latest.html (latest 20 by default)
  * http://csanz.io/latest.html?n=50 (latest 50, set n as required)
  
## HeartOne WebApp
Current mobile-friendly web app prototype can be viewed here: 

https://mappcpd-csanz-h1.herokuapp.com

Note this app is wired to the production database so any changes you make there are *real*.

This app is being developed with [VueJS](https://vuejs.org/) and [Vuetify](https://vuetifyjs.com).

## MappCPD API
The API provides controlled access to the underlying HeartOne database, allowing apps and 
 other tools to interact with the system is a secure, and consistent way. 
 
It is one component of the [Web Services](https://github.com/mappcpd/web-services) project.   

Initially a limited [REST](https://en.wikipedia.org/wiki/Representational_state_transfer) was developed.

See the [API documentation](https://api-docs.mappcpd.com/)  
 
However, this quickly started to become cumbersome, and an alternative approach using 
[GraphQL](http://graphql.org/) is being investigated.  

  

## Pubmed Resources

Resource are indexed from Pubmed into the MappCPD resources library, and use Algolia to improve the search experience.

The current Pubmed query does *not* use any Mesh terms, but instead pulls all articles from a specific set of journals.

The journals included are the first 30 in this list, plus numbers 32, 34, 36, 37, 38, 39, 43, 44, 45 and 46.

http://www.scimagojr.com/journalrank.php?category=2705&area=2700&type=j&year=2016

Abbreviations for Pubmed search available in this text file:

https://www.ncbi.nlm.nih.gov/books/NBK3827/table/pubmedhelp.T.journal_lists/?report=objectonly


**Current CSANZ Pubmed Term**

```
# Mesh terms were excluded
# "Cardiology"[Mesh] OR "Heart Diseases"[Mesh])  AND
loattrfree full text[Filter]  AND
(
"Am Heart J"[jour] OR
"Am J Cardiol"[jour] OR
"Arterioscler Thromb Vasc Biol"[jour] OR
"Atherosclerosis"[jour] OR
"Basic Res Cardiol"[jour] OR
"Cardiovasc Res"[jour] OR
"Chest"[jour] OR 
"Circulation"[jour] OR
"Circ Arrhythm Electrophysiol"[jour] OR 
"Circ Cardiovasc Genet"[jour] OR
"Circ Cardiovasc Imaging"[jour] OR
"Circ Cardiovasc Qual Outcomes"[jour] OR
"Circ Cardiovasc Interv" OR
"Circ Heart Fail" OR
"Circ Res"[jour] OR
"ESC Heart Fail"[jour] OR
"Eur Heart J"[jour] OR
"Eur Heart J Cardiovasc Imaging"[jour] OR
"Eur Heart J Acute Cardiovasc Care"[jour] OR 
"Eur Heart J Cardiovasc Pharmacother"[jour] OR
"Eur Heart J Qual Care Clin Outcomes"[jour] OR
"Eur J Heart Fail"[jour] OR
"Eur J Vasc Endovasc Surg"[jour] OR
"Europace"[jour] OR
"Heart"[jour] OR
"Heart Lung Circ"[jour] OR
"Heart Rhythm"[jour] OR
"JACC Cardiovasc Interv"[jour] OR
"JACC Cardiovasc Imaging"[jour] OR
"JACC Heart Fail"[jour] OR
"J Am Coll Cardiol"[jour] OR 
"J Am Heart Assoc"[jour] OR
"J Am Soc Echocardiogr" OR
"J Card Fail"[jour] OR
"J Cardiovasc Electrophysiol"[jour] OR
"J Cardiovasc Magn Reson"[jour] OR
"J Heart Lung Transplant"[jour] OR
"J Hypertens"[jour] OR
"J Mol Cell Cardiol"[jour] OR
"J Thorac Cardiovasc Surg"[jour] OR
"J Vasc Surg"[jour] OR
"Nat Rev Cardiol"[jour] OR
"Prog Cardiovasc Dis"[jour] OR
"Resuscitation"[jour] OR
"Stroke"[jour]
)
```

*Compact version*

```
loattrfree full text[Filter] AND ("Am Heart J"[jour] OR "Am J Cardiol"[jour] 
OR "Arterioscler Thromb Vasc Biol"[jour] OR "Atherosclerosis"[jour] 
OR "Basic Res Cardiol"[jour] OR "Cardiovasc Res"[jour] OR "Chest"[jour] 
OR "Circulation"[jour] OR "Circ Arrhythm Electrophysiol"[jour] 
OR "Circ Cardiovasc Genet"[jour] OR "Circ Cardiovasc Imaging"[jour] 
OR "Circ Cardiovasc Qual Outcomes"[jour] 
OR "Circ Cardiovasc Interv"[jour] OR "Circ Heart Fail"[jour] 
OR "Circ Res"[jour] OR "ESC Heart Fail"[jour] OR "Eur Heart J"[jour] 
OR "Eur Heart J Cardiovasc Imaging"[jour] OR "Eur Heart J Acute Cardiovasc Care"[jour] 
OR "Eur Heart J Cardiovasc Pharmacother"[jour] OR "Eur Heart J Qual Care Clin Outcomes"[jour] 
OR "Eur J Heart Fail"[jour] OR "Eur J Vasc Endovasc Surg"[jour] OR "Europace"[jour] OR "Heart"[jour] 
OR "Heart Lung Circ"[jour] OR "Heart Rhythm"[jour] OR "JACC Cardiovasc Interv"[jour] 
OR "JACC Cardiovasc Imaging"[jour] OR "JACC Heart Fail"[jour] OR "J Am Coll Cardiol"[jour] 
OR "J Am Heart Assoc"[jour] OR "J Am Soc Echocardiogr"[jour] OR "J Card Fail"[jour] 
OR "J Cardiovasc Electrophysiol"[jour] OR "J Cardiovasc Magn Reson"[jour] OR "J Heart Lung Transplant"[jour] 
OR "J Hypertens"[jour] OR "J Mol Cell Cardiol"[jour] OR "J Thorac Cardiovasc Surg"[jour] 
OR "J Vasc Surg"[jour] OR "Nat Rev Cardiol"[jour] OR "Prog Cardiovasc Dis"[jour] OR "Resuscitation"[jour] 
OR "Stroke"[jour])
```

[Test Search Url](https://www.ncbi.nlm.nih.gov/pubmed/?term=loattrfree%20full%20text%5BFilter%5D%20AND%20(%22Am%20Heart%20J%22%5Bjour%5D%20OR%20%22Am%20J%20Cardiol%22%5Bjour%5D%20OR%20%22Arterioscler%20Thromb%20Vasc%20Biol%22%5Bjour%5D%20OR%20%22Atherosclerosis%22%5Bjour%5D%20OR%20%22Basic%20Res%20Cardiol%22%5Bjour%5D%20OR%20%22Cardiovasc%20Res%22%5Bjour%5D%20OR%20%22Chest%22%5Bjour%5D%20OR%20%22Circulation%22%5Bjour%5D%20OR%20%22Circ%20Arrhythm%20Electrophysiol%22%5Bjour%5D%20OR%20%22Circ%20Cardiovasc%20Genet%22%5Bjour%5D%20OR%20%22Circ%20Cardiovasc%20Imaging%22%5Bjour%5D%20OR%20%22Circ%20Cardiovasc%20Qual%20Outcomes%22%5Bjour%5D%20OR%20%22Circ%20Cardiovasc%20Interv%22%5Bjour%5D%20OR%20%22Circ%20Heart%20Fail%22%5Bjour%5D%20OR%20%22Circ%20Res%22%5Bjour%5D%20OR%20%22ESC%20Heart%20Fail%22%5Bjour%5D%20OR%20%22Eur%20Heart%20J%22%5Bjour%5D%20OR%20%22Eur%20Heart%20J%20Cardiovasc%20Imaging%22%5Bjour%5D%20OR%20%22Eur%20Heart%20J%20Acute%20Cardiovasc%20Care%22%5Bjour%5D%20OR%20%22Eur%20Heart%20J%20Cardiovasc%20Pharmacother%22%5Bjour%5D%20OR%20%22Eur%20Heart%20J%20Qual%20Care%20Clin%20Outcomes%22%5Bjour%5D%20OR%20%22Eur%20J%20Heart%20Fail%22%5Bjour%5D%20OR%20%22Eur%20J%20Vasc%20Endovasc%20Surg%22%5Bjour%5D%20OR%20%22Europace%22%5Bjour%5D%20OR%20%22Heart%22%5Bjour%5D%20OR%20%22Heart%20Lung%20Circ%22%5Bjour%5D%20OR%20%22Heart%20Rhythm%22%5Bjour%5D%20OR%20%22JACC%20Cardiovasc%20Interv%22%5Bjour%5D%20OR%20%22JACC%20Cardiovasc%20Imaging%22%5Bjour%5D%20OR%20%22JACC%20Heart%20Fail%22%5Bjour%5D%20OR%20%22J%20Am%20Coll%20Cardiol%22%5Bjour%5D%20OR%20%22J%20Am%20Heart%20Assoc%22%5Bjour%5D%20OR%20%22J%20Am%20Soc%20Echocardiogr%22%5Bjour%5D%20OR%20%22J%20Card%20Fail%22%5Bjour%5D%20OR%20%22J%20Cardiovasc%20Electrophysiol%22%5Bjour%5D%20OR%20%22J%20Cardiovasc%20Magn%20Reson%22%5Bjour%5D%20OR%20%22J%20Heart%20Lung%20Transplant%22%5Bjour%5D%20OR%20%22J%20Hypertens%22%5Bjour%5D%20OR%20%22J%20Mol%20Cell%20Cardiol%22%5Bjour%5D%20OR%20%22J%20Thorac%20Cardiovasc%20Surg%22%5Bjour%5D%20OR%20%22J%20Vasc%20Surg%22%5Bjour%5D%20OR%20%22Nat%20Rev%20Cardiol%22%5Bjour%5D%20OR%20%22Prog%20Cardiovasc%20Dis%22%5Bjour%5D%20OR%20%22Resuscitation%22%5Bjour%5D%20OR%20%22Stroke%22%5Bjour%5D)&cmd=DetailsSearch)


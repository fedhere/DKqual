# DKqual

tips and useful links:

- the puma id is contained in the ACS data file, but the ACS id also contains the state id, 360 for NY. These ids are strings so to change the puma id to match the ACS id for a single row you can add the 360 piece as '360' + pumaid. To do that for all row you may want to use the function .apply(lambda x: '360' + x), or you can do it in a loop.

- when you merge make sure you merge the ACS dataframe into the puma geodataframe, and not viceversa:

  puma.merge(acsNY, right_on, left_on)
  
  you should then have 55 puma regions

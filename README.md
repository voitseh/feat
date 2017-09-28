OS: Win 
1 Create dataset direction in User folder 
2 In dataset direction create tree:
For inria:
 -- INRIA 
  -annotations(copy all annotations from INRIA PERSON DB here)
  -images(copy all images from INRIA PERSON DB here)
For afw:
 --AFW(Copy all images and anno here)
For imdb-wiki:
 --IMDB-WIKI
   - 100 directories,named: 00 - 99(Copy images here according to db structure)
   - also copy wiki.mat file hire
For wider:
 --WIDER
  -annotations(copy single ann file hire) 
  -images(copy all images from WIDER DB here)
 (When wider script will be running,"divide_ann" directory will be created in WIDER dir and populate with divide annotations)
  
 3 For converting INRIA to JSON,run json() fonction in InriaPerson.ipynb script(it's the same for other databases)
  The output JSON folder will be created in dataset folder.It's structure:
  -- JSON 
   -annotations
   -images 
 4 JSON_to_PascalVoc.ipynb script will convert JSON to Pascal_VOC.
 After running voc() function it will be created VOC directory in dataset dir. 
 It's structure:
 -- VOC 
   -test
     -annotations
     -images 
  -train 
     -annotations
     -images 
  -val 
     -annotations  
	 -images
  5 Here is also VisualisationTool.ipynb script.It is common for every databases. 
  It visualise images from JSON/images with bounding boxes. 
  As defoult,parameter imdb_wiki is False(wisualise bounding boxes only), 
  but if we want to show IMDB-WIKI images(with bounding boxes, ages and genders),
  we must change this parameter to "True"

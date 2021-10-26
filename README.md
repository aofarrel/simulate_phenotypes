*This is a debugging fork with a purposely malformed Dockstore entry -- please refer to the original repo for use in scientific analysis*

## Issues
* Dockstore can find the CWL and the Dockerfile, but not the test descriptor file, and this persists even if:
	* allele_freq.test.json is moved from the test directory into the same directory as allele_freq.cwl
	* allele_freq.test.json is renamed allele_freq.test.yml
	* Both of the above happen and the Dockstore entry is changed appropriately (ie it still can't find it in /tools/allele_freq.test.yml if you tell it is in /tools/allele_freq.test.yml)
* Dockstore is pointing to a GitHub commit that does not exist
	* The original repo *and* my fork both point to the same non-existent commit ID

## Not a bug
* .dockstore.yml is not being read -- we don't support CWL tools yet
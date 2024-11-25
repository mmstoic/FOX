This is a README that contains directions for setting up and compiling the
fuzzing target.

Set up fuzzer:
Run ./packages.sh
	This script will install the necessary packages needed by the fuzzer
	and check for which version of the service is installed. The script
	should be run in a clean fuzzing-specific directory named "fuzzing".
	Later steps will not work if the directory is not names "fuzzing".
Run ./gitclonecompile.sh
	This script will import and setup the OptFuzz directory. This script
	should be run in the same clean "fuzzing"  directory where
	packages.sh was run. It will create an OptFuzzer subdirectory.

Compiling the target:
Navigate to the directory jsoncpp, which should be located as a sub-directory
in the fuzzing-specific directory. This script will only work if the 
fuzzing-specific directory is named "fuzzing". 
Run ./new_build_aflpp.sh
	The script will clean out the jsoncpp subdirectory, run the pre-
	installation script, and set various enviornment variables. It
	will the perform various other operations to compile the target.

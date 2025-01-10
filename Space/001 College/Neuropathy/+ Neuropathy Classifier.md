#### Dataset First
- Lavalet 2023
	- Bukan Neuropathy (On progress)
		- Data
		- A449
		- BMP
			- abnormal
			- normal   => used dm non neuropathy
			- ragu
		- JPEG
	- Neuropathy
		- Data  => used
		- A417 => used
		- A418 => used
		- A437 => used
		- A438 => used
		- A444 => used
		- A453 => used
		- JPEG File
			- abnormal
			- normal   => used
			- ragu
- Puskesmas Dinoyo + Janti
	- Non Neuropathy
		- abnormal
		- normal => used
		- ragu
	- Neuropathy
		- abormal
		- normal => used
		- ragu
- Riset 2020
	- DM Bukan Neuropathy
		- abnormal
		- normal (30) => used -> into non neuropathy
		- ragu
	- DM Neuropathy
		- abnormal
		- normal => used
		- ragu
	- Non DM
		- abnormal
		- normal    => used
		- ragu
		- non dm (orang sehat) => used


Neuropathy 610
Non Neuropathy 829

Category: DM but it's not neuro, DM Neuro, Non DM

Train 926
Test 232
Epoch 100

#### Dataset Second
- Lavalet 2023
	- Bukan Neuropathy (On progress)
		- Data
		- A449
		- BMP
			- abnormal
			- normal => used ✔️ Non neuro
			- ragu
		- JPEG
	- Neuropathy
		- Data
		- A417
		- A418
		- A437
		- A438
		- A444
		- A453
		- JPEG File
			- abnormal => used ✔️ Neuro
			- normal => used ✔️ Non neuro
			- ragu
- Puskesmas Dinoyo + Janti
	- Non Neuropathy
		- abnormal
		- normal => used ✔️ Non neuro
		- ragu
	- Neuropathy
		- abormal => used ✔️ Neuro
		- normal => used ✔️  Non neuro
		- ragu
- Riset 2020
	- DM Bukan Neuropathy
		- abnormal
		- normal => used ✔️ Non neuro
		- ragu
	- DM Neuropathy
		- abnormal => used ✔️ Neuro
		- normal => used ✔️ Non Neuro
		- ragu
	- Non DM
		- abnormal
		- normal => used ✔️ Non Neuro
		- ragu
		- non dm (orang sehat)


Neuropathy 610
Non Neuropathy 829


#### Dataset Diabetes Melitus
- Lavalet 2023
	- Bukan Neuropathy (On progress)
		- Data
		- A449
		- BMP
			- abnormal  => used ✔️ Non neuro
			- normal
			- ragu
		- JPEG
	- Neuropathy
		- Data
		- A417
		- A418
		- A437
		- A438
		- A444
		- A453
		- JPEG File
			- abnormal => used ✔️ Neuro
			- normal
			- ragu
- Puskesmas Dinoyo + Janti
	- Non Neuropathy
		- abnormal  => used ✔️ Non neuro
		- normal
		- ragu
	- Neuropathy
		- abormal => used ✔️ Neuro
		- normal
		- ragu
- Riset 2020
	- DM Bukan Neuropathy
		- abnormal => used ✔️ Non neuro
		- normal
		- ragu
	- DM Neuropathy
		- abnormal => used ✔️ Neuro
		- normal
		- ragu
	- Non DM
		- abnormal
		- normal
		- ragu
		- non dm (orang sehat)


Neuropathy 990
Non Neuropathy 626

##### Augmentasi
Neuropathy = flip => 1980
Non Neuropathy = rotate 90, flip => 1878



#### Trinary DM Non/Neuro and Normal
- Lavalet 2023
	- Bukan Neuropathy (On progress)
		- Data
		- A449
		- BMP
			- abnormal  => used ✔️ Non neuro
			- normal => used ✔️ Normal
			- ragu
		- JPEG
	- Neuropathy
		- Data
		- A417
		- A418
		- A437
		- A438
		- A444
		- A453
		- JPEG File
			- abnormal => used ✔️ Neuro
			- normal => used ✔️ Normal
			- ragu
- Puskesmas Dinoyo + Janti
	- Non Neuropathy
		- abnormal  => used ✔️ Non neuro
		- normal => used ✔️ Normal
		- ragu
	- Neuropathy
		- abormal => used ✔️ Neuro
		- normal => used ✔️ Normal
		- ragu
- Riset 2020
	- DM Bukan Neuropathy
		- abnormal => used ✔️ Non neuro
		- normal => used ✔️ Normal
		- ragu
	- DM Neuropathy
		- abnormal => used ✔️ Neuro
		- normal => used ✔️ Normal
		- ragu
	- Non DM
		- abnormal
		- normal => used ✔️ Normal
		- ragu
		- non dm (orang sehat)


Neuropathy 990
Non Neuropathy 626
Normal 394

##### Augmentasi
Neuropathy = flip => 1980
Non Neuropathy = rotate 90, flip => 1878
Normal = rotate 90, 180, 270, flip



#### Binary split test and train val
- Train Val
	- Lavalet 2023
		- Bukan Neuropathy (On progress)
			- Data
			- A449
			- BMP
				- abnormal  => used ✔️ Non neuro
				- normal
				- ragu
			- JPEG
		- Neuropathy
			- Data
			- A417
			- A418
			- A437
			- A438
			- A444
			- A453
			- JPEG File
				- abnormal => used ✔️ Neuro
				- normal
				- ragu
	- Puskesmas Dinoyo + Janti
		- Non Neuropathy
			- abnormal  => used ✔️ Non neuro
			- normal
			- ragu
		- Neuropathy
			- abormal => used ✔️ Neuro
			- normal
			- ragu
- Test
	- Riset 2020
		- DM Bukan Neuropathy
			- abnormal => used ✔️ Non neuro
			- normal
			- ragu
		- DM Neuropathy
			- abnormal => used ✔️ Neuro
			- normal
			- ragu
		- Non DM
			- abnormal
			- normal
			- ragu
			- non dm (orang sehat)

Train Val
Neuropathy 990
Non Neuropathy 626

Test
Neuropathy 990
Non Neuropathy 626

##### Augmentasi
Neuropathy = flip => 1980
Non Neuropathy = rotate 90, flip => 1878



#### Trinary split test and train val
- Train val
	- Lavalet 2023
		- Bukan Neuropathy (On progress)
			- Data
			- A449
			- BMP
				- abnormal  => used ✔️ Non neuro
				- normal => used ✔️ Normal
				- ragu
			- JPEG
		- Neuropathy
			- Data
			- A417
			- A418
			- A437
			- A438
			- A444
			- A453
			- JPEG File
				- abnormal => used ✔️ Neuro
				- normal => used ✔️ Normal
				- ragu
	- Puskesmas Dinoyo + Janti
		- Non Neuropathy
			- abnormal  => used ✔️ Non neuro
			- normal => used ✔️ Normal
			- ragu
		- Neuropathy
			- abormal => used ✔️ Neuro
			- normal => used ✔️ Normal
			- ragu
- Test
	- Riset 2020
		- DM Bukan Neuropathy
			- abnormal => used ✔️ Non neuro
			- normal => used ✔️ Normal
			- ragu
		- DM Neuropathy
			- abnormal => used ✔️ Neuro
			- normal => used ✔️ Normal
			- ragu
		- Non DM
			- abnormal
			- normal => used ✔️ Normal
			- ragu
			- non dm (orang sehat)


Train Val
Neuropathy 990
Non Neuropathy 626
Normal 394

Test
Neuropathy 990
Non Neuropathy 626
Normal 394

##### Augmentasi
Neuropathy = flip => 1980
Non Neuropathy = rotate 90, flip => 1878
Normal = rotate 90, 180, 270, flip

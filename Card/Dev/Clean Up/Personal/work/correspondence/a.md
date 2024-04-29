# original
NO_KK	
	201938109238
NIK
	10923809238
NAMA_LGKP	
	Judi
JENIS_KLMIN
	1 | 2
JENIS_KLMIN_KET
	Lk | Pr
TMPT_LHR	
	MALANG
TGL_LHR	
	M/D/Y
AGAMA	
	1
AGAMA_KET	
	Islam
PDDK_AKH	
	3
PENDIDIKAN_AKH_KET	
	Tamat SD/Sederajat
JENIS_PKRJN	
	15
JENIS_PKRJN_KET
	KARYAWAN SWASTA
GOL_DRH	
	13
STAT_KWN_KET
	B
TGL_KWN	
	M/D/Y
STAT_HBKEL	
	1
STAT_HBKEL_1
	KEPALA KELUARGA
ALAMAT	
	DUSUN KRAJAN
	SELOREJO
NO_RT	
	1
NO_RW
	1
DUSUN
	?
	KRAJAN
KODE_POS	
	65151
TELP	
NO_PROP	
	35
NAMA_PROP	
	JAWA TIMUR
NO_KAB	
	7
NAMA_KAB
	MALANG
NO_KEC	
	22
NAMA_KEC
	DAU
NO_KEL
	2004
NAMA_KEL
	SELOREJO

# separatism
kk , nik, nama, 
jk, jk ket, 
tmpt lahir, tgl lahir

agama
agama ket

pendidikan akhir 3
pendidikan akhir ket

jenis pekerjaan
jenis pekerjaan ket

gol darah 1.2.3.4

status kawin b/s

status hubungan keluarga
status hubungan keluarga ket

alamat


# Navigation
Dashboard
Persuratan
	create surat
	template
Kependudukan
	Penduduk
	Tambah Penduduk
Data Master
	Agama
	Pendidikan akhir
	Jenis Pekerjaan
	Golongan Darah
	Status Kawin
	Status Hubungan Keluarga
	Tempat
		Provinsi
		Kabupaten
		Kecamatan
		Kelurahan

# File tree | views
component
	layout
		app
		guest
		atom
			sidebar
			topbar
			footer
	auth
		login
	main
		dashboard
		individual
			individual
			individual-create
		master
			religion
			education
			blood-type
			marriage
			kinship
			address
				city
				province
				urban
				district
				district-sub
				
		
# table
religion
education
job
blood
marriage
kinship

city
province
urban
district
district-sub


individual

mail_template
mail

---
name label keterangan
# Minor en
- Rukun tetangga (RT) = Neighbourhood
- Rukun Warga (RW) = Hamlet
- Pedukuhan = Village
- Kelurahan = Urban village
- Kecamatan = Sub-district
- Kabupaten = District/regency
- Provinsi = Province


- Rukun tetangga (RT) = Neighbourhood
- Rukun Warga (RW) = Hamlet
- dusun = hamlet
- Kelurahan/desa = sub-district / Village / urban village
- Kecamatan = district
- Kabupaten = regency
- Provinsi = Province

# alg
- page one
	- personal
- page two
	- kk
	- address
on save button
	update if exist
	create if doesn't exist
	
	

kk
	1 ppl 1 kk
	2 or more kk, can have same address
	1 kk (all people in it) 1 address

auto complete kk
auto fill address
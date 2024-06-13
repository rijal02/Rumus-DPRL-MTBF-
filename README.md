# Rumus-DPRL-MTBF-
print('* soal ke 1 *')
rata_rata = float(input('Masukkan Rata-rata banyak kali perbaikan :  '))
subjek = float(input('Masukkan berapa unit yang dipinjamkan kepada subjek : '))
hasil = rata_rata / subjek
print('Rata-rata perbaikannya adalah ', hasil)
print()

print('* Mencari Gama *')
hari = float(input('Masukkan lama garansi : '))
gama = hasil / hari
print('Nilai Gama nya adalah ',gama)

print('*Mencari MTBF*')
mtbf = 1/gama
print('Nilai MTBF nya adalah ',mtbf)

#####
print('*Soal ke 2*')
jam_uji = float(input('Lama waktu yang diujikan : '))
jam_rusak = float(input('Lama waktu barang yang digunakan rusak : '))
unit_rusak = float(input('Unit yang rusak : '))
waktu_akhir = (jam_uji/jam_rusak)*unit_rusak
print('Lama waktu unit yang mengalami kerusakan ', waktu_akhir)
print()
total_unit_rusak = float(input('Total unit rusak : '))
total_jam_operasi = jam_uji*total_unit_rusak
print('Total jam operasinya adalah ', total_jam_operasi)
print()
waktu_operasi = total_jam_operasi-waktu_akhir
print('Waktu operasinya adalah ', waktu_operasi)
print()
laju_kerusakan_jam = unit_rusak/waktu_operasi
print('Laju Kerusakan /jam adalah', laju_kerusakan_jam)
laju_kerusakan_tahun = laju_kerusakan_jam/(1/(24*365))
print('Laju Kerusakan /tahun adalah', laju_kerusakan_tahun)
print()
rusak_diinginkan = float(input('Berapa seandainya rusak yang diingikan : '))
rusak_yang_diinginkan = laju_kerusakan_tahun*rusak_diinginkan
print('Kerusakan yang diperkirakan dalam pertahun adlah ',rusak_yang_diinginkan)
print()
mtbf = 1/laju_kerusakan_tahun
print('Hasil MTBF nya adalah ', mtbf)

#####


# Ujian Akhir Semester

<br> Mata Kuliah : Dasar Pemrograman
<br> Nama        : Amanda Zulfa Salsabila
<br> NIM         : 1227050019
<br> Jurusan     : Teknik Informatika UIN Sunan Gunung Djati Bandung



# Deskripsi Umum

Tema utama dari source code yang satu ini adalah untuk membuat array dalam impldementasi deret aritmatika.
Tujuan utama dari source code ini adalah untuk mencari bilangan yang tidak habis dibagi angka 3, 5, dan.
<br> Algoritma dari source code ini yaitu :
<br> 1. User menginputkan berapa banyak baris pada array mulai dari range 0-20.
<br> 2. User menginputkan berapa banyak kolom pada array mulai dari range 0-20.
<br> 3. User memginputkan satu persatu nilai array, dimulai dari baris 1 dan kolom 1.
<br> 4. Jika sudah, nilai dalam array tersebut ditampilkan sesuai aturan matriks.
<br> 5. Kemudian nilai divalidasi kembali apakah nilai tersebut habis dibagi 3, 5, dan 7.
<br> 6. Apabila nilai tadi habis dibagi 3, 5, dan 7, maka nilai tidak akan ditampilkan apabila tidak habis. Tampilkan kembali kepada user.



# Source Code

#include <iostream>
using namespace std;

int main (){
	int A [20][20];
	int b, k, i, j;
	cout << "Masukkan jumlah baris : ";
	cin >> b;
	cout << "Masukkan jumlah kolom : ";
	cin >> k;
	
	for (i=0;i<=b-1;i++) {
		for(j=0;j<=k-1;j++) {
			cout << "Masukkan nilai (" << i << "." << j << ") : ";
			cin >> A [i][j];
		}
	}
	cout << "Nilai yang diinputkan : \n";
	for(int i = 0; i < b; i++){
		for(int j = 0; j < k; j++){
			cout<<A[i][j]<<"\t";
		}
		cout<<endl;
	}
	int angka[20];
	int index = 0;
	for(i=0;i<b;i++){
		for(j=0;j<k;j++) {
			if (A [i][j]%3 != 0 && A[i][j]%5 != 0 && A[i][j]%7 != 0){
				angka[index] = A[i][j];
				index++;
			}
		}
	}
	cout<<"Angka yang tidak bisa dibagi 3, 5, 7 adalah ";
	for(int i = 0; i < index; i++){
		cout<<angka[i]<<", ";

	}
}

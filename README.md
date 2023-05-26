Nama : Andi Rachman Zikry

NIM : 2009076013

Ket : Ujian Tengah Semester_Sistem Operasi 2023

Soal

1. Jika diketahui 6 antrian proses (A,B,C,D,E,F) dengan waktu kedatangan secara bersamaan yaitu : 0. Lama eksekusi tiap-tiap antrian proses secara berurutan 1,3,7,5,5,3. Hitunglah Trun Arround Time (TA) dengan menggunakan teknik penjadwalan proses:

    a. Frist In Frist Out (FIFO)

    b. Shortest Job first (SJF)

    c. Round Robin jika diketahui Quantum = 2

2. Dalam penjadwalan proses terdapat tiga macam penjadwalan, sebutkan dan jelaskan disertai gambar !

3. Sumber daya apa yang digunakan saat thread dibuat? Bagaimana mereka berbeda dari yang digunakan ketika suatu proses dibuat?

4. Output apa yang akan ditampilkan pada LINE A ? Jelaskan !

#include <sys/types.h>

#include <stdio.h>

#include <unistd.h>

int value = 5;

int main()
{
pid_t pid;
	
	pid = fork();
	
	if (pid ==0){ /*child prcess */
		value += 15;
		return 0;
	}
	else if (pid > 0){ /* parent process */
		wait(NULL);
		printf("PARENT : value = %d",value); /* LINE A */
		return 0;
	}
}

# My-First-Project-a-marketing-website-
#include <stdio.h>
#include <conio.h>
#include <windows.h>
#include <stdlib.h>
#include <string.h> 
#include <ctype.h>
#include <iostream> 
#include <time.h>
#include <dos.h>
#include <cstdlib>
#include <tchar.h>

using namespace std;
#pragma warning(disable:4996)

//------------------------------------------------------------------------------------
//Tamam Nazarat
struct TamamNazarat
{
	char Nazar[6][100] = { {"Incredible  Incredible  Incredible  Incredible  Incredible  Incredible"} ,{"Bad Bad  Bad Bad  Bad Bad  Bad Bad  Bad Bad  Bad Bad  Bad Bad"},{"proposal proposal proposal proposal proposal proposal proposal proposal"},	{"Incredible  Incredible  Incredible  Incredible  Incredible  Incredible"} ,{"Bad Bad  Bad Bad  Bad Bad  Bad Bad  Bad Bad  Bad Bad  Bad Bad"},{"proposal proposal proposal proposal proposal proposal proposal proposal"}};
	int Tarikh[6][2] = { {1,1},{1,25},{2,26},{1,10},{1,24},{2,13} };
};
struct TamamNazarat TNazarat;
//Sabad Kharid Dar Hal Pardazesh Safe Moshtari
struct SabadKharidDMosh
{
	int tedad[2] = { 1,5 };
	int gheymat[2] = { 23,78 };
};
struct SabadKharidDMosh SabadKDMosh;
//Safe_Moshtari
struct SafeMoshtari
{
	//Sefaresh Ha Ye Pishin
	int Pgheymat[5] = { 510,23,69,45,48 };
	//Sefaresh Dar Hal Pardazesh
	int Dgheymat[5] = { 564,78,102,45,123 };
};
struct SafeMoshtari SafeMosh;
//Safe_Forooshande
struct SafeForooshande
{
	int Tedad[5] = { 2,9,6,7,3 };
	int n = 5;
};
struct SafeForooshande SafeForoosh;
//List_Karbaran
//**List_Karbaran_Forooshande
struct ListKarbaranForooshande
{
	int TedadSefaresh[3] = { 5,8,3 };
	int MablaghKol[3] = { 458,183,726 };
	int n = 3;
};
struct ListKarbaranForooshande LKForooshande;
//**List_Karbaran_Moshtari
struct ListKarbaranMoshtari
{
	int TedadSefaresh[3] = { 8,3,4 };
	int MablaghKol[3] = { 43,128,76 };
};
struct ListKarbaranMoshtari LKMoshtari;
//Sabad_Kharid
struct SabadKharid
{
	int gheimat5[7] = { 110,320,680,510,70,390,120 };
	int tedad5[7] = { 2,4,5,8,3,5,9 };
	int n = 7;
};
struct SabadKharid SabadKhar;
// Kharid_Anjam_Shode
struct KharidAnjamShode
{
	int gheimat4[5] = { 10,970,80,510,250 };
	int Tarikh4[5][2] = { {1,8},{2,6},{1,9},{2,20},{1,30} };
};
struct KharidAnjamShode KharidnAnjam;
// Moshtari Moshahede Kala
int flag = 0;
// Safe_Kala
struct SafeKala
{
	int setare = 4, emt = 4, flag2 = 0;
	char Nazar[200];
};
struct SafeKala Safe;
// Mavad_Ghazaii_Menu
struct MavadGhazaii
{
	int gheimat1[6] = { 500,200,700,50,790,300 };
	int emtiaz1[6] = { 2,4,5,0,3,2 };
};
struct MavadGhazaii Mavad;
// Lavazem_Tahrir_Menu
struct LavazemTahrir
{
	int gheimat2[6] = { 200,350,10,800,90,600 };
	int emtiaz2[6] = { 2,4,1,5,3,2 };
};
struct LavazemTahrir Tahrir;
// Kala_Digital_Menu
struct KalaDigi
{
	int gheimat3[6] = { 320,700,650,50,90,400 };
	int emtiaz3[6] = { 1,0,5,4,3,2 };
};
struct KalaDigi Digital;
//-----------------------------------------------------------------------------------
void gotoxy(int x, int y)
{
	COORD coord;
	coord.X = x;
	coord.Y = y;
	SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), coord);
}
void setcolor(int colorcode) {
	HANDLE console = GetStdHandle(STD_OUTPUT_HANDLE);
	SetConsoleTextAttribute(console, colorcode % 255);
}
//------------------------------------------------------------------------------------
//$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$
void Moshahede_Kala_Main_Menu(void);
void Sabt_Nam(void);
void Vorood(void);
void Moshtari_Main_menu(void);
void Admin_Main_Menu(void);
void Forooshande_Main_Menu(void);
void Mavad_Ghazaii_Menu(void);
void Lavazem_Tahrir_Menu(void);
void Kala_Digital_Menu(void);
void Kharid_Anjam_Shode(void);
void Tagheer_Moshakhasat_Moshtari(void);
void Sabad_Kharid(void);
void List_Karbaran(void);
void Tamam_Nazarat(void);
void Forush_Kol(void);
void EmalCodeTakhfif_ZamanTahvil_KarmozdKhod(void);
void Kala_Jadid(void);
void Kala_Forookhte_Shode(void);
void Nazar_Forooshande(void);
void Tagheer_Moshakhasat_Forooshande(void);
void Safe_Kala(void);
void Sabad_Kala_Anjam_Shode(void);
void List_Karbaran_Moshtari(void);
void List_Karbaran_Forooshande(void);
void Safe_Forooshande(void);
void Safe_Moshtari(void);
//$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$
//------------------------------------------------------------------------------------

//------------------------------------------------------------------------------------
void Tagheer_Moshakhasat_Forooshande(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;

	setcolor(64); puts("\n\n\n\n\t\t Baraye Didan Foroosh Kol 1, va Baraye Tagheer Moshakhat 2 Ra Vared Konid: "); setcolor(7);
	gotoxy(16, 5);
	scanf("%d", &choise);

	switch (choise)
	{
	case 1:
		{
		system("CLS");
		system("color 47");

		printf("\n\n\t\t\t _______________\n");
		printf("\t\t\t|  Foroosh Kol  |\n");
		printf("\t\t\t|_______________|\t : \t");
		printf("27\n\n\t");

		setcolor(1);
		printf("\n\t\t//\\\\ Foroosh e Kala Ye 1 //\\\\ \t : \t 12 \n\t");

		setcolor(6);
		printf("\n\t\t//\\\\ Foroosh e Kala Ye 2 //\\\\ \t : \t 2 \n\t");

		setcolor(10);
		printf("\n\t\t//\\\\ Foroosh e Kala Ye 3 //\\\\ \t : \t 7 \n\t");

		setcolor(15);
		printf("\n\t\t//\\\\ Foroosh e Kala Ye 4 //\\\\ \t : \t 6 \n\n\n\n\n");

		setcolor(71);
		system("pause");

		Forooshande_Main_Menu();
		}
		break;
	case 2:
		{
		system("CLS");
		system("color 47");
		char name[20], username[20], password[20], phone_number[20], address[20];

		setcolor(192);
		puts("\n\n\n\n\t\tPlease Enter Your New Name, Username, Password & Phone_number in order: ");

		gotoxy(16, 5);
		setcolor(64);
		scanf("%s%s%s%s", name, username, password, phone_number);

		setcolor(144);
		puts("\n\t\tEnter Address Of Your New Office: ");

		gotoxy(16, 8);
		setcolor(64);
		scanf("%s", address);

		Forooshande_Main_Menu();
		}
		break;
	}
}
//------------------------------------------------------------------------------------
void Nazar_Forooshande(void)
{

}
//------------------------------------------------------------------------------------
void Kala_Forookhte_Shode(void)
{

}
//------------------------------------------------------------------------------------
void Kala_Jadid(void)
{

}
//------------------------------------------------------------------------------------
void Forush_Kol(void)
{
	system("CLS");
	system("COLOR F0");
	int qwqw;

	setcolor(240);
	printf("\n\t\t\t\t\t"); cout << char(218);  for (int i = 0; i < 23; i++) { cout << char(205); }  cout << char(194);  for (int i = 0; i < 8; i++) { cout << char(205); }  cout << char(191) << endl;
	printf("\t\t\t\t\t"); cout << char(186) << "Forush Kol Admin       " << char(186) << "568000" << char(186) << endl;
	printf("\t\t\t\t\t"); cout << char(195);  for (int i = 0; i < 23; i++) { cout << char(205); }  cout << char(197);  for (int i = 0; i < 8; i++) { cout << char(205); }  cout << char(185) << endl;
	printf("\t\t\t\t\t"); cout << char(186) << "Forush Kol Forushande 1" << char(186) << "42544   " << char(186) << endl;
	printf("\t\t\t\t\t"); cout << char(195);  for (int i = 0; i < 23; i++) { cout << char(205); }  cout << char(197);  for (int i = 0; i < 8; i++) { cout << char(205); }  cout << char(185) << endl;
	printf("\t\t\t\t\t"); cout << char(186) << "Forush Kol Forushande 2" << char(186) << "123     " << char(186) << endl;
	printf("\t\t\t\t\t"); cout << char(195);  for (int i = 0; i < 23; i++) { cout << char(205); }  cout << char(197);  for (int i = 0; i < 8; i++) { cout << char(205); }  cout << char(185) << endl;
	printf("\t\t\t\t\t"); cout << char(186) << "Forush Kol Forushande 3" << char(186) << "57863   " << char(186) << endl;
	printf("\t\t\t\t\t"); cout << char(195);  for (int i = 0; i < 23; i++) { cout << char(205); }  cout << char(197);  for (int i = 0; i < 8; i++) { cout << char(205); }  cout << char(185) << endl;
	printf("\t\t\t\t\t"); cout << char(186) << "Forush Kol Forushande 4" << char(186) << "22134   " << char(186) << endl;
	printf("\t\t\t\t\t"); cout << char(195);  for (int i = 0; i < 23; i++) { cout << char(205); }  cout << char(197);  for (int i = 0; i < 8; i++) { cout << char(205); }  cout << char(185) << endl;
	printf("\t\t\t\t\t"); cout << char(186) << "Forush Kol Forushande 5" << char(186) << "5567    " << char(186) << endl;
	printf("\t\t\t\t\t"); cout << char(192);  for (int i = 0; i < 23; i++) { cout << char(205); }  cout << char(193);  for (int i = 0; i < 8; i++) { cout << char(205); }  cout << char(217) << endl;

	setcolor(1); printf("\n\n\t\t\tBaraye Sort Kardan 1 Ra Vared Konid: "); scanf("%d", &qwqw);
	printf("\n\n\n\n\n");
	if (qwqw == 1)
	{
		Forush_Kol();
	}
}
//------------------------------------------------------------------------------------

//------------------------------------------------------------------------------------
void Tamam_Nazarat(void)
{
	system("CLS");
	int choise;

	setcolor(4); printf("\t\t\t _________\n"); printf("\t\t--------|"); setcolor(96); printf(" NAZARAT "); setcolor(4); printf("| --------");

	printf("\n\n\n");
	for (int i = 0; i < 3; i++)
	{
		printf("\t\t  %d.Karbar e Adi: \n\n  %s", i + 1, TNazarat.Nazar[i]);
	}

	printf("\n\n\n");
	for (int i = 3; i < 6; i++)
	{
		printf("\t\t  %d.Moshtari: \n\n  %s", i + 1, TNazarat.Nazar[i]);
	}

	setcolor(8); printf("\n\n\t\tAge Mikhay Bar Asas Tarikh Sort Koni 1, \n\t\tVa Age Mikhay Be Safhe Ye Mored Nazar Kalayi Beri 2, Ra Vared Konid: ");
	scanf("%d", &choise);

	switch (choise)
	{
	case 1:
	{
		for (int i = 0; i < 6; ++i)
		{
			for (int j = i + 1; j < 6; ++j)
			{
				if (TNazarat.Tarikh[i][0] < TNazarat.Tarikh[j][0])
				{
					int a = TNazarat.Tarikh[i][0];
					TNazarat.Tarikh[i][0] = TNazarat.Tarikh[j][0];
					TNazarat.Tarikh[j][0] = a;

					char b[100];
					strcpy(b, TNazarat.Nazar[i]);
					strcpy(TNazarat.Nazar[i], TNazarat.Nazar[j]);
					strcpy(TNazarat.Nazar[j], b);

					for (int ii = 0; ii < 5; ++ii)
					{
						for (int jj = ii + 1; jj < 5; ++jj)
						{
							if (TNazarat.Tarikh[ii][1] < TNazarat.Tarikh[jj][1])
							{
								a = TNazarat.Tarikh[ii][1];
								TNazarat.Tarikh[ii][1] = TNazarat.Tarikh[jj][1];
								TNazarat.Tarikh[jj][1] = a;
							}
						}
					}
				}
			}
		}
	}
	break;
	case 2:
	{
		int shomare;
		setcolor(8); printf("\n\n\t\tShomare Nazar Ra Vared Kon: ");
		scanf("%d", &shomare);
		Safe_Kala();
	}
	break;
	}
}
//------------------------------------------------------------------------------------
void Safe_Moshtari(void)
{
	system("CLS");
	system("COLOR E0");
	int kodoom;

	setcolor(96);
	printf("\n\t\t\t  "); cout << char(201);      for (int i = 0; i < 30; i++) { cout << char(205); }      cout << char(187) << "  " << endl;
	printf("\t\t\t  "); cout << char(186) << "            Kharidar          " << char(186) << "  " << endl;
	printf("\t\t\t  "); cout << char(200);      for (int i = 0; i < 30; i++) { cout << char(205); }      cout << char(188) << "  " << endl;

	setcolor(48); printf("\n\n\t\t\t\tSefaresh Ha Ye Pishin:\n"); setcolor(240);
	for (int i = 0; i < 5; i++)
	{
		printf("\n\t\t\t %d. Sefaresh%d \t Gheymat Kol: %d", i + 1, i + 1, SafeMosh.Pgheymat[i]);
	}

	setcolor(144); printf("\n\n\t\t\t\tDar Hal Pardazesh:\n"); setcolor(240);
	for (int i = 0; i < 5; i++)
	{
		printf("\n\t\t\t %d. Sefaresh%d \t Gheymat Kol: %d", i + 1, i + 1, SafeMosh.Dgheymat[i]);
	}

	setcolor(8); printf("\n\n\t\tBaraye Moshahede Sabad Kharid Shomare Sefaresh Ra Vared Konid:"); scanf("%d", &kodoom);

	//sabad kharid
	system("CLS");
	printf("\n\n\t\t\t   "); setcolor(7); printf("~ "); setcolor(3); printf("~ "); setcolor(1); printf("~ "); setcolor(2); printf("~ "); setcolor(10); printf("~ "); setcolor(64); printf("Sabad Kharid"); setcolor(14); printf(" ~ "); setcolor(6); printf("~ "); setcolor(12); printf("~ "); setcolor(4); printf("~ "); setcolor(13); printf("~ ");

	setcolor(192);
	for (int i = 0; i < 2; i++)
	{
		printf("\n\n\t\t\t%d. Kala%d \t Gheymat: %d \t Tedad: %d", i + 1, i + 1);
	}
}
//------------------------------------------------------------------------------------
void Safe_Forooshande(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;

	setcolor(96);
	printf("\n\t\t\t"); cout << char(201);      for (int i = 0; i < 30; i++) { cout << char(205); }      cout << char(187) << endl;
	printf("\t\t\t"); cout << char(186) << "          Forooshande         " << char(186) << endl;
	printf("\t\t\t"); cout << char(200);      for (int i = 0; i < 30; i++) { cout << char(205); }      cout << char(188) << endl;

	setcolor(128);
	printf("\n\n");
	for (int i = 0; i < 5; i++)
	{
		printf("\n\t\t%d. Kala Forookhte Shode%d", i + 1, i + 1);
	}
	for (int i = 0; i < 5; i++)
	{
		printf("\n\t\t%d. Kala Baraye Foroosh%d \t Tedad: %d", i + 1, i + 1, SafeForoosh.Tedad[i]);
	}

	setcolor(64);
	printf("\n\n\n\tAge Mikhay Kalayi Ra Hazf Koni 1, Va Age Mikhay Tedadesh Ro Kahesh Bedi 2 Ra Vared Kon: "); scanf("%d", &choise);

	switch (choise)
	{
	case 1:
	{
		int kodoom;

		setcolor(233); puts("\n\tKodoom Kala Ro Mikhay Hazf Koni?");
		gotoxy(40, 23);
		setcolor(224); scanf("%d", &kodoom);

		// func Hazf
		for (int c = kodoom - 1; c < SafeForoosh.n; c++)
			SafeForoosh.Tedad[c] = SafeForoosh.Tedad[c + 1];

		Safe_Forooshande();
	}
	break;
	case 2:
	{
		int kodoom, TedadJadid;

		setcolor(233); puts("\n\tKodoom Kala Ro Mikhay Kam Koni?");
		gotoxy(40, 23);
		setcolor(224); scanf("%d", &kodoom);

		setcolor(233); puts("\n\tTedad Jadid Kala Ro Vared Kon: ");
		gotoxy(40, 25);
		setcolor(224); scanf("%d", &TedadJadid);

		SafeForoosh.Tedad[kodoom] = TedadJadid;

		Safe_Forooshande();
	}
	break;
	}
}
//------------------------------------------------------------------------------------
void List_Karbaran_Forooshande(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;

	printf("\n\n");
	for (int i = 0; i < 3; i++)
	{
		printf("\n\t\t%d. Forushande%d \t Tedad Sefaresh Anjam Shode : %d \t Mablagh Kol Forush: %d", i + 1, i + 1, LKForooshande.TedadSefaresh[i], LKForooshande.MablaghKol[i]);
	}

	setcolor(240);
	printf("\n\n\n\n\t\tVase Sort Kardan Bar Asas Tedad Sefaresh 1 Ra vared Konid,"); setcolor(64);
	printf("\n\t\tVase Sort Kardan Bar Asas Mablagh Foroosh Kol 2 Ra vared Konid,"); setcolor(96);
	printf("\n\t\tVase Hazf Foroshande 3 Ra vared Konid,"); setcolor(32);
	printf("\n\t\tVase Didan Safhe Forooshande 4 Ra vared Konid:"); setcolor(224);
	scanf("%d", &choise);

	switch (choise)
	{
	case 1:
		for (int i = 0; i < 3; ++i)
		{
			for (int j = i + 1; j < 3; ++j)
			{
				if (LKForooshande.TedadSefaresh[i] < LKForooshande.TedadSefaresh[j])
				{
					int a = LKForooshande.TedadSefaresh[i];
					LKForooshande.TedadSefaresh[i] = LKForooshande.TedadSefaresh[j];
					LKForooshande.TedadSefaresh[i] = a;

					int b = LKForooshande.MablaghKol[i];
					LKForooshande.MablaghKol[i] = LKForooshande.MablaghKol[j];
					LKForooshande.MablaghKol[j] = b;
				}
			}
		}
		List_Karbaran_Forooshande();
		break;
	case 2:
		for (int i = 0; i < 3; ++i)
		{
			for (int j = i + 1; j < 3; ++j)
			{
				if (LKForooshande.MablaghKol[i] < LKForooshande.MablaghKol[j])
				{
					int a = LKForooshande.TedadSefaresh[i];
					LKForooshande.TedadSefaresh[i] = LKForooshande.TedadSefaresh[j];
					LKForooshande.TedadSefaresh[i] = a;

					int b = LKForooshande.MablaghKol[i];
					LKForooshande.MablaghKol[i] = LKForooshande.MablaghKol[j];
					LKForooshande.MablaghKol[j] = b;
				}
			}
		}
		List_Karbaran_Forooshande();
		break;
	case 3:
		{
		int kodoom;

		setcolor(233); puts("\n\tKodoom Foroshande Ro Mikhay Hazf Koni?");
		gotoxy(40, 23);
		setcolor(224); scanf("%d", &kodoom);

		// func Hazf
		for (int c = kodoom - 1; c < LKForooshande.n; c++)
			LKForooshande.TedadSefaresh[c] = LKForooshande.TedadSefaresh[c + 1];
		// func Hazf
		for (int c = kodoom - 1; c < LKForooshande.n; c++)
			LKForooshande.MablaghKol[c] = LKForooshande.MablaghKol[c + 1];

		int jarime;
		printf("\n\t\tMablagh Jarime Ra Vared Konid: ");
		scanf("%d", &jarime);

		List_Karbaran();
		}
		break;
	case 4:
		Safe_Forooshande();
		break;
	}
}
//------------------------------------------------------------------------------------
void List_Karbaran_Moshtari(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;

	printf("\n\n");
	for (int i = 0; i < 3; i++)
	{
		printf("\n\t\t%d. Kharidar%d \t Tedad Sefaresh: %d \t Mablagh Kol Kharid: %d", i + 1, i + 1, LKMoshtari.TedadSefaresh[i], LKMoshtari.MablaghKol[i]);
	}

	setcolor(240);
	printf("\n\n\n\n\t\tVase Sort Kardan Bar Asas Tedad Sefaresh 1 Ra vared Konid,"); setcolor(64);
	printf("\n\t\tVase Sort Kardan Bar Asas Mablagh Kharid Kol 2 Ra vared Konid,"); setcolor(96);
	//printf("\n\t\tVase Didan Sabad Kharid Har Kodam Ra Bebinid 3 Ra vared Konid:"); setcolor(32);
	printf("\n\t\tVase Didan Sefaresh Haye Pishin Va Dar Hal Pardazesh 3 Ra vared Konid:"); setcolor(32);
	scanf("%d", &choise);

	switch (choise)
	{
	case 1:
		for (int i = 0; i < 3; ++i)
		{
			for (int j = i + 1; j < 3; ++j)
			{
				if (LKMoshtari.TedadSefaresh[i] < LKMoshtari.TedadSefaresh[j])
				{
					int a = LKMoshtari.TedadSefaresh[i];
					LKMoshtari.TedadSefaresh[i] = LKMoshtari.TedadSefaresh[j];
					LKMoshtari.TedadSefaresh[i] = a;

					int b = LKMoshtari.MablaghKol[i];
					LKMoshtari.MablaghKol[i] = LKMoshtari.MablaghKol[j];
					LKMoshtari.MablaghKol[j] = b;
				}
			}
		}
		List_Karbaran_Moshtari();
		break;
	case 2:
		for (int i = 0; i < 3; ++i)
		{
			for (int j = i + 1; j < 3; ++j)
			{
				if (LKMoshtari.MablaghKol[i] < LKMoshtari.MablaghKol[j])
				{
					int a = LKMoshtari.TedadSefaresh[i];
					LKMoshtari.TedadSefaresh[i] = LKMoshtari.TedadSefaresh[j];
					LKMoshtari.TedadSefaresh[i] = a;

					int b = LKMoshtari.MablaghKol[i];
					LKMoshtari.MablaghKol[i] = LKMoshtari.MablaghKol[j];
					LKMoshtari.MablaghKol[j] = b;
				}
			}
		}
		List_Karbaran_Moshtari();
		break;
	case 3:
		Safe_Moshtari();
		break;
	}
}
//------------------------------------------------------------------------------------
void List_Karbaran(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;
	
	setcolor(248);
	printf("\n\t\t\t\t\t\t"); cout << char(218);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(194);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(191) << endl;
	printf("\t\t\t\t\t\t"); cout << char(186) << "1. List   " << char(186) << "Forushande" << char(186) << endl;
	printf("\t\t\t\t\t\t"); cout << char(195);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(197);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(185) << endl;
	printf("\t\t\t\t\t\t"); cout << char(186) << "2. List   " << char(186) << " Karbaran " << char(186) << endl;
	printf("\t\t\t\t\t\t"); cout << char(192);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(193);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(217) << endl;

	setcolor(8);
	printf("\n\n\t\tEnter Your Choise: ");
	gotoxy(16, 9);
	scanf("%d", &choise);

	switch (choise)
	{
	case 1:
		List_Karbaran_Forooshande();
		break;
	case 2:
		List_Karbaran_Moshtari();
		break;
	}
}
//------------------------------------------------------------------------------------
void Tagheer_Moshakhasat_Moshtari(void)
{
	system("CLS");
	system("COLOR E0");
	char name[20], username[20], password[20], phone_number[20], address[20];

	setcolor(192);
	puts("\n\n\n\n\t\tPlease Enter Your New Name, Username, Password & Phone_number in order: ");
	gotoxy(16, 5);
	setcolor(7);
	scanf("%s%s%s%s", name, username, password, phone_number);

	setcolor(144);
	puts("\n\t\tEnter Address Of Your Home: ");

	gotoxy(16, 8);
	setcolor(7);
	scanf("%s", address);

	Moshtari_Main_menu();
}
//------------------------------------------------------------------------------------
void Sabad_Kharid(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;

	setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~\t\n");

	printf("\n\n\n\t\t   "); setcolor(7); printf("~ "); setcolor(3); printf("~ "); setcolor(1); printf("~ "); setcolor(2); printf("~ "); setcolor(10); printf("~ "); setcolor(192); printf("Sabad Kharid"); setcolor(14); printf(" ~ "); setcolor(6); printf("~ "); setcolor(12); printf("~ "); setcolor(4); printf("~ "); setcolor(13); printf("~ ");

	setcolor(224); printf("\n\n\n");
	for (int i = 0; i < SabadKhar.n; i++)
	{
		printf("\t\t%d. Kala%d \t Gheymat: %d \t Tedad: %d\n", i + 1, i + 1, SabadKhar.gheimat5[i], SabadKhar.tedad5[i]);
	}

	setcolor(6); puts("\n\n\tAge Mikhay Kalaii Ro Hazf Koni Enter 1,"); setcolor(12); puts("\n\tAge Mikhay Teedad Kalaii Ro Kam Ya Ziyad Koni Enter 2,"); setcolor(4); puts("\n\tBara Ye Nahaii Kardan Kharid Enter 3 :"); setcolor(7);
	gotoxy(48, 21);
	scanf("%d", &choise);

	switch (choise)
	{
	case 1:
		{
		int kodoom;

		setcolor(233); puts("\n\tKodoom Kala Ro Mikhay Hazf Koni?");
		gotoxy(40, 23);
		setcolor(224); scanf("%d", &kodoom);

		// func Hazf
		for (int c = kodoom - 1; c < SabadKhar.n; c++)
			SabadKhar.gheimat5[c] = SabadKhar.gheimat5[c + 1];
		// func Hazf
		for (int c = kodoom - 1; c < SabadKhar.n; c++)
			SabadKhar.tedad5[c] = SabadKhar.tedad5[c + 1];

		Sabad_Kharid();
	}
		break;
	case 2:
		{
		int kam_zyiad, kodoom;

		setcolor(232); puts("\n\tKodoom Kala Ro Mikhay Kam Ya Zyad Koni?");
		gotoxy(48, 23);
		setcolor(224); scanf("%d", &kodoom);

		setcolor(232); puts("\n\tTedad e Jadid Ro Vared Kon : ");
		gotoxy(37, 25);
		setcolor(224); scanf("%d", &kam_zyiad);

		SabadKhar.tedad5[kodoom - 1] = kam_zyiad;

		Sabad_Kharid();
	}
		break;
	case 3:
		{
		system("CLS");
		system("COLOR E0");
		int code; char shomare_kart[20];

		setcolor(232); puts("\n\n\n\n\t\tAge Code Takhfif Dari Vared Kon, Age Nadari 0 Ro Vared Kon : ");
		gotoxy(16, 5);
		setcolor(224); scanf("%s", &code);

		setcolor(235); puts("\n\t\tShomare Kartet Ro Vared Kon : ");
		gotoxy(16, 8);
		setcolor(224); scanf("%s", shomare_kart);

		setcolor(234); puts("\n\t\tRamzet Ro Vared Kon : ");
		gotoxy(16, 11);
		setcolor(224); scanf("%s", shomare_kart);

		setcolor(192); puts("\n\n\t\tKharid Ba Moafaghiyat Anjam Shod :)  "); setcolor(238);
		system("pause");

		Moshtari_Main_menu();
	}
	break;
	}
}
//------------------------------------------------------------------------------------
void Sabad_Kala_Anjam_Shode(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;

	setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~\t\n");

	printf("\n\n\n\t\t   "); setcolor(7); printf("~ "); setcolor(3); printf("~ "); setcolor(1); printf("~ "); setcolor(2); printf("~ "); setcolor(10); printf("~ "); setcolor(192); printf("Sabad Kharid"); setcolor(14); printf(" ~ "); setcolor(6); printf("~ "); setcolor(12); printf("~ "); setcolor(4); printf("~ "); setcolor(13); printf("~ ");

	setcolor(224); printf("\n\n\n\t\t1. Kala1 \t Gheymat: 1500 \t Tedad: 2\n"); printf("\n\t\t2. Kala2 \t Gheymat: 500 \t Tedad: 3\n"); printf("\n\t\t3. Kala3 \t Gheymat: 630 \t Tedad: 8\n"); printf("\n\t\t4. Kala4 \t Gheymat: 10 \t Tedad: 7\n"); printf("\n\t\t5. Kala5 \t Gheymat: 800 \t Tedad: 1\n");

	setcolor(240); puts("\n\n\tSafhe ye kodoom kala ro mikhay bebini?"); setcolor(224);
	gotoxy(8, 20);
	scanf("%d", &choise);

	Safe_Kala();
}
//------------------------------------------------------------------------------------
void Kharid_Anjam_Shode(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;

	puts("\n\n");
	setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~"); setcolor(6); printf("*"); setcolor(7); printf(" ~\t\n");
	printf("\n\n\n\t\t\t"); setcolor(7); printf("~ "); setcolor(3); printf("~ "); setcolor(1); printf("~ "); setcolor(2); printf("~ "); setcolor(10); printf("~ "); setcolor(7); setcolor(48); printf("Kharid Ha Ye Anjam Shode"); setcolor(14); printf(" ~ "); setcolor(6); printf("~ "); setcolor(12); printf("~ "); setcolor(4); printf("~ "); setcolor(13); printf("~ ");

	setcolor(224); printf("\n");
	for (int i = 0; i < 5; i++)
	{
		printf("\n\t\t%d. Kharid%d \t\t Gheymat: %d \t\t Tarikh: 99/%d/%d", i + 1, i + 1, KharidnAnjam.gheimat4[i], KharidnAnjam.Tarikh4[i][0], KharidnAnjam.Tarikh4[i][1]);
	} printf("\n\n");

	setcolor(230);
	puts("\n\t\t-- Agar Mikhay  Bar Asas Gheimat Kala ha ro Sort Koni Enter 1,");
	setcolor(234);
	puts(" \t\t   Agar Mikhay  Bar Asas Tarikh Kala ha ro Sort Koni Enter 2,");
	setcolor(233);
	puts("  \t\t   Baray e Moshahede har kodoon az Sabad Ha Enter 3:");

	setcolor(224);
	gotoxy(19, 20);
	scanf("%d", &choise);

	switch (choise)
	{
	case 1:
		for (int i = 0; i < 6; ++i)
		{
			for (int j = i + 1; j < 6; ++j)
			{
				if (KharidnAnjam.gheimat4[i] < KharidnAnjam.gheimat4[j])
				{
					int a = KharidnAnjam.gheimat4[i];
					KharidnAnjam.gheimat4[i] = KharidnAnjam.gheimat4[j];
					KharidnAnjam.gheimat4[j] = a;

					int b = KharidnAnjam.Tarikh4[i][0];
					KharidnAnjam.Tarikh4[i][0] = KharidnAnjam.Tarikh4[j][0];
					KharidnAnjam.Tarikh4[j][0] = b;

					b = KharidnAnjam.Tarikh4[i][1];
					KharidnAnjam.Tarikh4[i][1] = KharidnAnjam.Tarikh4[j][1];
					KharidnAnjam.Tarikh4[j][1] = b;
				}
			}
		}
		Kharid_Anjam_Shode();
		break;
	case 2:
		for (int i = 0; i < 5; ++i)
		{
			for (int j = i + 1; j < 5; ++j)
			{
				if (KharidnAnjam.Tarikh4[i][0] < KharidnAnjam.Tarikh4[j][0])
				{
					int a = KharidnAnjam.Tarikh4[i][0];
					KharidnAnjam.Tarikh4[i][0] = KharidnAnjam.Tarikh4[j][0];
					KharidnAnjam.Tarikh4[j][0] = a;

					a = KharidnAnjam.gheimat4[i];
					KharidnAnjam.gheimat4[i] = KharidnAnjam.gheimat4[j];
					KharidnAnjam.gheimat4[j] = a;

					for (int ii = 0; ii < 5; ++ii)
					{
						for (int jj = ii + 1; jj < 5; ++jj)
						{
							if (KharidnAnjam.Tarikh4[ii][1] < KharidnAnjam.Tarikh4[jj][1])
							{
								a = KharidnAnjam.Tarikh4[ii][1];
								KharidnAnjam.Tarikh4[ii][1] = KharidnAnjam.Tarikh4[jj][1];
								KharidnAnjam.Tarikh4[jj][1] = a;
							}
						}
					}
				}
			}
		}

		Kharid_Anjam_Shode();
		break;
	case 3:
	{
		int Sabad;

		setcolor(160);
		puts("\n\t\tShomare Sabad Ro Benevis?");
		setcolor(224);
		gotoxy(42, 22);
		scanf("%d", &Sabad);

		Sabad_Kala_Anjam_Shode();
	}
	break;
	}
}
//------------------------------------------------------------------------------------
void Safe_Kala(void)
{
	system("CLS");
	system("color 7");
	int choise;

	setcolor(192); printf("\n\n\n   \t\t\t\t\t\t"); setcolor(7); printf("~ "); setcolor(3); printf("~ "); setcolor(1); printf("~ "); setcolor(2); printf("~ "); setcolor(10); printf("~ "); setcolor(7); printf("KALA "); setcolor(14); printf("~ "); setcolor(6); printf("~ "); setcolor(12); printf("~ "); setcolor(4); printf("~ "); setcolor(13); printf("~ ");

	printf("\n\n\n\t\t\t"); setcolor(128); printf("Foroshande:"); setcolor(11); printf("   <  Sahar >"); setcolor(7);

	setcolor(128);  printf("\t\t\t\tEmtyaz:"); setcolor(6); 

	// Emtiyaz
	{
		Safe.setare += Safe.emt;
		Safe.setare /= 2;

		printf("   ");
		for (int i = 0; i < Safe.setare; i++)
		{
			printf("* ");
		}
	}
	// Emtiyaz ends
	printf("\n"); setcolor(7);

	setcolor(128); printf("\n\t\t\tMojoodi:"); setcolor(11); printf(" 5\n\n");

	setcolor(5); puts("\n\n\n\t\tText Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih \n\t\tText Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih \n\t\tText Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih \n\t\tText Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih \n\t\tText Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih \n\t\tText Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih Text Tozih ");
	printf("\n\n");

	setcolor(4); printf("\t\t\t _________\n"); printf("\t\t--------|"); setcolor(96); printf(" NAZARAT "); setcolor(4); printf("| --------");

	setcolor(14); puts("\n\n\n\t\t  Kharidar: \n\n\t\t  Incredible  Incredible  Incredible  Incredible  Incredible  Incredible  Incredible \n\t\t  Incredible  Incredible  Incredible  Incredible  Incredible  Incredible \n\t\t  Incredible  Incredible  Incredible ");

	puts("\n\n\n\t\t  Karbar e Adi: \n\n\t\t  Bad Bad  Bad Bad  Bad Bad  Bad Bad  Bad Bad  Bad Bad  Bad Bad\n\t\t  Bad Bad  Bad Bad  Bad Bad  Bad Bad  Bad Bad  Bad Bad \n\n");

	if (Safe.flag2 == 1)
	{
		setcolor(14); puts("\n\t\t  Moshtari: \n");
		printf("\t\t  %s\n\n", Safe.Nazar);
	}

	if (flag == 1)
	{
		setcolor(10); puts("\t\tDo You Want To Add SomeThing?? (Enter 1) , Mikhay Emtiaz Bedi?? (Enter 2) : "); setcolor(7);

		gotoxy(16, 45);
		scanf("%d", &choise);

		switch (choise)
		{
		case 1:
		{
			Safe.flag2 = 1;
			gotoxy(16, 45);
			scanf("%s", &Safe.Nazar);
			Safe_Kala();
		}
		break;
		case 2:
		{
			gotoxy(16, 45);
			scanf("%d", &Safe.emt);
			Safe_Kala();
			break;
		}
		}
	}
	int pause;
	scanf("%d", &pause);
}
//------------------------------------------------------------------------------------
void Kala_Digital_Menu(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;

	printf("\n");
	for (int t = 1, i = 0; i < 6; i++, t++)
	{
		printf("\n\n\t\t%d. Kala\t\tGheimat: %d\t\tEmtiaz: %d", t, Digital.gheimat3[i], Digital.emtiaz3[i]);
	} printf("\n\n");

	setcolor(230);
	puts("\n\t\t-- Agar Mikhay  Bar Asas Gheimat Kala ha ro Sort Koni Enter 1,");
	setcolor(234);
	puts(" \t\t   Agar Mikhay  Bar Asas Emtiyaz Kala ha ro Sort Koni Enter 2,");
	setcolor(233);
	puts(" \t\t   Baraye Didan Safhe ye Yek Kala Enter 3,");
	setcolor(229);
	puts(" \t\t   Age Mikhay Barasas e Daste Bandi Bebiny Enter 4: ");
	setcolor(224);
	gotoxy(68, 19);
	scanf("%d", &choise);

	switch (choise)
	{
	case 1:
		for (int i = 0; i < 6; ++i)
		{
			for (int j = i + 1; j < 6; ++j)
			{
				if (Digital.gheimat3[i] < Digital.gheimat3[j])
				{
					int a = Digital.gheimat3[i];
					Digital.gheimat3[i] = Digital.gheimat3[j];
					Digital.gheimat3[j] = a;

					a = Digital.emtiaz3[i];
					Digital.emtiaz3[i] = Digital.emtiaz3[j];
					Digital.emtiaz3[j] = a;
				}
			}
		}
		Lavazem_Tahrir_Menu();
		break;
	case 2:
		for (int i = 0; i < 6; ++i)
		{
			for (int j = i + 1; j < 6; ++j)
			{
				if (Digital.emtiaz3[i] < Digital.emtiaz3[j])
				{
					int a = Digital.emtiaz3[i];
					Digital.emtiaz3[i] = Digital.emtiaz3[j];
					Digital.emtiaz3[j] = a;

					a = Digital.gheimat3[i];
					Digital.gheimat3[i] = Digital.gheimat3[j];
					Digital.gheimat3[j] = a;
				}
			}
		}
		Lavazem_Tahrir_Menu();
		break;
	case 3:
	{
		int ShomareKala;

		setcolor(160);
		puts("\n\t\tShomare Kala Ro Benevis?");
		setcolor(224);
		gotoxy(40, 21);
		scanf("%d", &ShomareKala);

		Safe_Kala();
	}
	break;
	case 4:
		Moshahede_Kala_Main_Menu();
		break;
	}
}
//------------------------------------------------------------------------------------
void Lavazem_Tahrir_Menu(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;

	printf("\n");
	for (int t = 1, i = 0; i < 6; i++, t++)
	{
		printf("\n\n\t\t%d. Kala\t\tGheimat: %d\t\tEmtiaz: %d", t, Tahrir.gheimat2[i], Tahrir.emtiaz2[i]);
	} printf("\n\n");

	setcolor(230);
	puts("\n\t\t-- Agar Mikhay  Bar Asas Gheimat Kala ha ro Sort Koni Enter 1,");
	setcolor(234);
	puts(" \t\t   Agar Mikhay  Bar Asas Emtiyaz Kala ha ro Sort Koni Enter 2,");
	setcolor(233);
	puts(" \t\t   Baraye Didan Safhe ye Yek Kala Enter 3,");
	setcolor(229);
	puts(" \t\t   Age Mikhay Barasas e Daste Bandi Bebiny Enter 4: ");
	setcolor(224);
	gotoxy(68, 19);
	scanf("%d", &choise);

	switch (choise)
	{
	case 1:
		for (int i = 0; i < 6; ++i)
		{
			for (int j = i + 1; j < 6; ++j)
			{
				if (Tahrir.gheimat2[i] < Tahrir.gheimat2[j])
				{
					int a = Tahrir.gheimat2[i];
					Tahrir.gheimat2[i] = Tahrir.gheimat2[j];
					Tahrir.gheimat2[j] = a;

					a = Tahrir.emtiaz2[i];
					Tahrir.emtiaz2[i] = Tahrir.emtiaz2[j];
					Tahrir.emtiaz2[j] = a;
				}
			}
		}
		Lavazem_Tahrir_Menu();
		break;
	case 2:
		for (int i = 0; i < 6; ++i)
		{
			for (int j = i + 1; j < 6; ++j)
			{
				if (Tahrir.emtiaz2[i] < Tahrir.emtiaz2[j])
				{
					int a = Tahrir.emtiaz2[i];
					Tahrir.emtiaz2[i] = Tahrir.emtiaz2[j];
					Tahrir.emtiaz2[j] = a;

					a = Tahrir.gheimat2[i];
					Tahrir.gheimat2[i] = Tahrir.gheimat2[j];
					Tahrir.gheimat2[j] = a;
				}
			}
		}
		Lavazem_Tahrir_Menu();
		break;
	case 3:
	{
		int ShomareKala;

		setcolor(160);
		puts("\n\t\tShomare Kala Ro Benevis?");
		setcolor(224);
		gotoxy(40, 21);
		scanf("%d", &ShomareKala);

		Safe_Kala();
	}
	break;
	case 4:
		Moshahede_Kala_Main_Menu();
		break;
	}
}
//------------------------------------------------------------------------------------
void Mavad_Ghazaii_Menu(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;

	printf("\n");
	for (int t = 1, i = 0; i < 6; i++, t++)
	{
		printf("\n\n\t\t%d. Kala\t\tGheimat: %d\t\tEmtiaz: %d", t, Mavad.gheimat1[i], Mavad.emtiaz1[i]);
	} printf("\n\n");

	setcolor(230);
	puts("\n\t\t-- Agar Mikhay  Bar Asas Gheimat Kala ha ro Sort Koni Enter 1,");
	setcolor(234);
	puts(" \t\t   Agar Mikhay  Bar Asas Emtiyaz Kala ha ro Sort Koni Enter 2,");
	setcolor(233);
	puts(" \t\t   Baraye Didan Safhe ye Yek Kala Enter 3,");
	setcolor(229);
	puts(" \t\t   Age Mikhay Barasas e Daste Bandi Bebiny Enter 4: ");
	setcolor(224);
	gotoxy(68, 19);
	scanf("%d", &choise);

	switch (choise)
	{
	case 1:
		for (int i = 0; i < 6; ++i)
		{
			for (int j = i + 1; j < 6; ++j)
			{
				if (Mavad.gheimat1[i] < Mavad.gheimat1[j])
				{
					int a = Mavad.gheimat1[i];
					Mavad.gheimat1[i] = Mavad.gheimat1[j];
					Mavad.gheimat1[j] = a;

					a = Mavad.emtiaz1[i];
					Mavad.emtiaz1[i] = Mavad.emtiaz1[j];
					Mavad.emtiaz1[j] = a;
				}
			}
		}
		Mavad_Ghazaii_Menu();
		break;
	case 2:
		for (int i = 0; i < 6; ++i)
		{
			for (int j = i + 1; j < 6; ++j)
			{
				if (Mavad.emtiaz1[i] < Mavad.emtiaz1[j])
				{
					int a = Mavad.emtiaz1[i];
					Mavad.emtiaz1[i] = Mavad.emtiaz1[j];
					Mavad.emtiaz1[j] = a;

					a = Mavad.gheimat1[i];
					Mavad.gheimat1[i] = Mavad.gheimat1[j];
					Mavad.gheimat1[j] = a;
				}
			}
		}
		Mavad_Ghazaii_Menu();
		break;
	case 3:
		{
		int ShomareKala;

		setcolor(160);
		puts("\n\t\tShomare Kala Ro Benevis?");
		setcolor(224);
		gotoxy(40, 21);
		scanf("%d", &ShomareKala);

		Safe_Kala();
		}
		break;
	case 4:
		Moshahede_Kala_Main_Menu();
		break;
	}
}
//------------------------------------------------------------------------------------
void Forooshande_Main_Menu(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;

	setcolor(32);
	puts("\n\n\n\n\t\t1.Kala Ye Jadid\n");
	setcolor(48);
	puts("\t\t2.Moshahede Kala Ha Ye Forookhte Shode\n");
	setcolor(16);
	puts("\t\t3.Nazarat\n");
	setcolor(64);
	puts("\t\t4.Tagheer Moshakhasat Va Moshahede Moshakhasat\n");
	setcolor(80);
	puts("\t\t5.Moshahede Kala Ha\n");
	setcolor(112);
	puts("\t\t6.Enteghal Be Hesab\n");

	setcolor(128);
	puts("\t\tEnter your choise: ");
	gotoxy(16, 19);
	scanf("%d", &choise);

	switch (choise)
	{
	case 1:
		Kala_Jadid();
		break;
	case 2:
		Kala_Forookhte_Shode();
		break;
	case 3:
		Nazar_Forooshande();
		break;
	case 4:
		Tagheer_Moshakhasat_Forooshande();
		break;
	case 5:
		Moshahede_Kala_Main_Menu();
		break;
	case 6:
		{
		system("CLS");
		system("color D1");

		char shomare_h[20];

		setcolor(80);
		printf("\n\n\n\tShomare Hesab Khod Ra Vared Konid: ");
		gotoxy(8, 4);
		scanf("%s", shomare_h);

		printf("\n\n\tMabalegh Ba Moaafaghiat Be Hesab e Shoma Variz Shod :) \n\n\n\n\n\n");
		setcolor(7);
		system("pause");

		Forooshande_Main_Menu();
		}
		break;
	}
}
//------------------------------------------------------------------------------------
void EmalCodeTakhfif_ZamanTahvil_KarmozdKhod(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;

	setcolor(48);
	printf("\n\n\n\t\t1. Sakht Code Takhfif\n");
	setcolor(160);
	printf("\n\t\t2. Taeen Modat Zaman Tahvil\n");
	setcolor(128);
	printf("\n\t\t3. Taeen Karmozd\n");
	setcolor(192);
	printf("\n\t\t4. Taeen Modat Zamani Ke Sefaresh Ghabel e Hazf Ast\n");
	setcolor(240);
	printf("\n\t\tEnter Your Choise: \n"); gotoxy(35, 11); scanf("%d", &choise);

	switch (choise)
	{
	case 1:
	{
		system("CLS");
		system("COLOR E0");
		char payam[50];

		setcolor(240);
		printf("\n\n\n\t\tCode Takhfif Jadid Ra Vared Konid: \n"); gotoxy(54, 3); scanf("%s", payam);

		setcolor(48);
		printf("\n\t\tDarsad Takhfif Ra Vared Konid: \n"); gotoxy(50, 5); scanf("%s", payam);

		setcolor(160);
		printf("\n\t\tTarikh Etebar Code Ra Vared Konid: \n"); gotoxy(54, 7); scanf("%s", payam);

		system("CLS");
		EmalCodeTakhfif_ZamanTahvil_KarmozdKhod();
	}
	break;
	case 2:
	{
		char payam[50];

		setcolor(128);
		printf("\n\t\tModat Zaman Tahvil Ra Vared Konid: \n"); gotoxy(52, 13); scanf("%s", payam);

		EmalCodeTakhfif_ZamanTahvil_KarmozdKhod();
	}
	break;
	case 3:
	{
		char payam[50];

		setcolor(128);
		printf("\n\t\tKarmozd Khod Ra Vared Konid: \n"); gotoxy(46, 13); scanf("%s", payam);

		EmalCodeTakhfif_ZamanTahvil_KarmozdKhod();
	}
	break;
	case 4:
	{
		char payam[50];

		setcolor(128);
		printf("\n\t\tModat Zaman Ke Sefaresh Ghabel e Hazf Ast Ra Vared Konid: \n"); gotoxy(75, 13); scanf("%s", payam);

		EmalCodeTakhfif_ZamanTahvil_KarmozdKhod();
	}
	break;
	}
}
//------------------------------------------------------------------------------------
void Admin_Main_Menu(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;

	setcolor(192);
	printf("\n\t\t\t\t\t\t"); cout << char(218);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(194);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(191) << endl;
	printf("\t\t\t\t\t\t"); cout << char(186) << "   Admin  " << char(186) << "          " << char(186) << endl;
	printf("\t\t\t\t\t\t"); cout << char(195);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(197);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(185) << endl;
	printf("\t\t\t\t\t\t"); cout << char(186) << "          " << char(186) << "   Menu   " << char(186) << endl;
	printf("\t\t\t\t\t\t"); cout << char(192);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(193);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(217) << endl;

	setcolor(64);
	printf("\n\t\t"); cout << char(201);      for (int i = 0; i < 50; i++) { cout << char(205); }      cout << char(187) << endl;
	printf("\t\t"); cout << char(186) << " 1. Emal Code Takhfif, Zaman Tahvil, Karmozd Khod " << char(186) << endl;
	printf("\t\t"); cout << char(200);      for (int i = 0; i < 50; i++) { cout << char(205); }      cout << char(188) << endl;

	setcolor(96);
	printf("\n\t\t"); cout << char(201);      for (int i = 0; i < 21; i++) { cout << char(205); }      cout << char(187) << endl;
	printf("\t\t"); cout << char(186) << " 2. List Karbaran    " << char(186) << endl;
	printf("\t\t"); cout << char(200);      for (int i = 0; i < 21; i++) { cout << char(205); }      cout << char(188) << endl;

	setcolor(32);
	printf("\n\t\t"); cout << char(201);      for (int i = 0; i < 21; i++) { cout << char(205); }      cout << char(187) << endl;
	printf("\t\t"); cout << char(186) << " 3. Tamam Nazarat    " << char(186) << endl;
	printf("\t\t"); cout << char(200);      for (int i = 0; i < 21; i++) { cout << char(205); }      cout << char(188) << endl;

	setcolor(16);
	printf("\n\t\t"); cout << char(201);      for (int i = 0; i < 25; i++) { cout << char(205); }      cout << char(187) << endl;
	printf("\t\t"); cout << char(186) << " 4. Moshahede Forush Kol " << char(186) << endl;
	printf("\t\t"); cout << char(200);      for (int i = 0; i < 25; i++) { cout << char(205); }      cout << char(188) << endl;

	//setcolor(80);
	//printf("\n\t\t"); cout << char(201);      for (int i = 0; i < 32; i++) { cout << char(205); }      cout << char(187) << endl;
	//printf("\t\t"); cout << char(186) << " 5. Payam Adam Daryaft Sefaresh " << char(186) << endl;
	//printf("\t\t"); cout << char(200);      for (int i = 0; i < 32; i++) { cout << char(205); }      cout << char(188) << endl;

	setcolor(240);
	printf("\n\t\tEnter Your Choise: ");
	setcolor(224);
	scanf("%d", &choise);

	switch (choise)
	{
	case 1:
		EmalCodeTakhfif_ZamanTahvil_KarmozdKhod();
		break;
	case 2:
		List_Karbaran();
		break;
	case 3:
		Tamam_Nazarat();
		break;
	case 4:
		Forush_Kol();
		break;
	/*case 5:
		Residegi_Sefareshat_Daryaft_Nashode();
		break;*/
	}
}
//------------------------------------------------------------------------------------
void Moshtari_Main_menu(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;
	flag = 1;

	setcolor(192);
	puts("\n\n\n\n\t\t1.Moshahede Kala Ha\n");
	setcolor(64);
	puts("\t\t2.Moshahede Kharid Ha Ye Anjam Shode\n");
	/*setcolor(208);
	puts("\t\t3.Moshahede Kharid Ha Ye Tahvil Dade Nashode\n");*/
	setcolor(176);
	puts("\t\t3.Tagheer Moshakhasat\n");
	setcolor(32);
	puts("\t\t4.Sabad e Kharid\n");

	setcolor(96);
	puts("\t\tEnter your choise: ");
	gotoxy(35, 12);
	scanf("%d", &choise);

	switch (choise)
	{
	case 1:
		Moshahede_Kala_Main_Menu();
		break;
	case 2:
		Kharid_Anjam_Shode();
		break;
	/*case 3:
		Kharid_Tahvil_Dade_Nashode();
		break;*/
	case 3:
		Tagheer_Moshakhasat_Moshtari();
		break;
	case 4:
		Sabad_Kharid();
		break;
	}
}
//------------------------------------------------------------------------------------
void Moshahede_Kala_Main_Menu(void)
{
	system("CLS");
	system("COLOR E0");
	int choise;

	setcolor(192);
	puts("\n\n\n\n\t\tList e Kala ha :");
	setcolor(225);
	puts("\n\t\t1. Mavad e Ghazaee");
	setcolor(232);
	puts("\n\t\t2. Lavazem Tahrir");
	setcolor(228);
	puts("\n\t\t3. Kala Ye Digital");

	setcolor(96);
	puts("\n\n\n\t\tEnter Your Choise :");
	setcolor(224);
	gotoxy(16, 15);
	scanf("%d", &choise);

	switch (choise)
	{
	case 1:
		Mavad_Ghazaii_Menu();
		break;
	case 2:
		Lavazem_Tahrir_Menu();
		break;
	case 3:
		Kala_Digital_Menu();
		break;
	}
}
//------------------------------------------------------------------------------------
void Sabt_Nam(void)
{
	system("CLS");
	system("COLOR E0");

	char name[20], username[20], password[20], phone_number[20], address[20];
	int cus_sell;

	setcolor(192);
	puts("\n\n\n\n\t\tPlease Enter Your Name, Username, Password & Phone_number in order: ");
	gotoxy(16, 5);
	setcolor(224);
	scanf("%s%s%s%s", name, username, password, phone_number);

	setcolor(96);
	puts("\n\t\tAre You A Customer Or A Seller? (Enter 1 for customer and 0 for seller) : ");
	gotoxy(16, 8);
	setcolor(224);
	scanf("%d", &cus_sell);

	if (cus_sell == 0)
	{
		setcolor(144);
		puts("\n\t\tEnter Address Of Your Office: ");
		gotoxy(16, 11);
		setcolor(224);
		scanf("%s", address);
	}
	else if (cus_sell == 1)
	{
		setcolor(144);
		puts("\n\t\tEnter Address Of Your House: ");
		gotoxy(16, 11);
		setcolor(224);
		scanf("%s", address);
	}
}
//------------------------------------------------------------------------------------
void Vorood(void)
{
	system("CLS");
	system("COLOR E0");

	char usr_name[100], passw[100];

	while (1)
	{
		setcolor(80);
		puts("\n\n\n\n\t\tPlease Enter Your Username: ");
		gotoxy(16, 5);
		setcolor(224);
		scanf("%s", usr_name);

		setcolor(192);
		puts("\n\t\tPlease Enter Your Password: ");
		gotoxy(16, 8);
		setcolor(224);
		scanf("%s", passw);

		if (strcmp(usr_name, "admin") == 0)
		{
			if (strcmp(passw, "admin") == 0)
			{
				setcolor(244);
				puts("\n\t\tWelcom Back!!\n\n");
				setcolor(238);

				system("pause");
				system("CLS");

				Admin_Main_Menu();

				break;
			}
			else
			{
				setcolor(244);
				puts("\n\t\tWrong Password  :(\n\n");
				setcolor(238);

				system("pause");
				system("CLS");
			}
		}
		else if (strcmp(usr_name, "customer") == 0)
		{
			if (strcmp(passw, "customer") == 0)
			{
				setcolor(244);
				puts("\n\t\tWelcom Back!!\n\n");
				setcolor(238);

				system("pause");
				system("CLS");

				Moshtari_Main_menu();
				break;
			}
			else
			{
				setcolor(244);
				puts("\n\t\tWrong Password  :(\n\n");
				setcolor(238);

				system("pause");
				system("CLS");
			}
		}
		else if (strcmp(usr_name, "seller") == 0)
		{
			if (strcmp(passw, "seller") == 0)
			{
				setcolor(244);
				puts("\n\t\tWelcom Back!!\n\n");
				setcolor(238);

				system("pause");
				system("CLS");

				Forooshande_Main_Menu();
				break;
			}
			else
			{
				setcolor(244);
				puts("\n\t\tWrong Password :(\n\n");
				setcolor(238);

				system("pause");
				system("CLS");
			}
		}
		else
		{
			setcolor(244);
			puts("\n\t\tWrong Username :(\n\n");
			setcolor(238);

			system("pause");
			system("CLS");
		}
	}
}
//------------------------------------------------------------------------------------

int main(int argc, char** args)
{
	system("CLS");
	system("COLOR E0");
	int choise;

	// Font
	{
		CONSOLE_FONT_INFOEX cfi;
		cfi.cbSize = sizeof cfi;
		cfi.nFont = 0;
		cfi.dwFontSize.X = 8;
		cfi.dwFontSize.Y = 17;
		cfi.FontFamily = FF_DONTCARE;
		cfi.FontWeight = 700;
		wcscpy(cfi.FaceName, L"Consolas");
		SetCurrentConsoleFontEx(GetStdHandle(STD_OUTPUT_HANDLE), FALSE, &cfi);
		//EnumFonts(GetDC((HWND)GetStdHandle(STD_OUTPUT_HANDLE)), L"Terminal", logfont, NULL);
		/*wcscpy_s(cfi.FaceName, 9, L"Terminal");
		SetCurrentConsoleFontEx(GetStdHandle(STD_OUTPUT_HANDLE), FALSE, &cfi);*/
	}

	{
		setcolor(192);
		printf("\n\t\t\t\t\t\t"); cout << char(218);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(194);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(191) << endl;
		printf("\t\t\t\t\t\t"); cout << char(186) << "   main   " << char(186) << "          " << char(186) << endl;
		printf("\t\t\t\t\t\t"); cout << char(195);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(197);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(185) << endl;
		printf("\t\t\t\t\t\t"); cout << char(186) << "          " << char(186) << "   Menu   " << char(186) << endl;
		printf("\t\t\t\t\t\t"); cout << char(192);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(193);  for (int i = 0; i < 10; i++) { cout << char(205); }  cout << char(217) << endl;

		setcolor(64);
		printf("\n\t\t"); cout << char(201);      for (int i = 0; i < 22; i++) { cout << char(205); }      cout << char(187) << endl;
		printf("\t\t"); cout << char(186) << " 1. Moshahede Kala Ha " << char(186) << endl;
		printf("\t\t"); cout << char(200);      for (int i = 0; i < 22; i++) { cout << char(205); }      cout << char(188) << endl;

		setcolor(96);
		printf("\n\t\t"); cout << char(201);      for (int i = 0; i < 15; i++) { cout << char(205); }      cout << char(187) << endl;
		printf("\t\t"); cout << char(186) << " 2. Sabt e Nam " << char(186) << endl;
		printf("\t\t"); cout << char(200);      for (int i = 0; i < 15; i++) { cout << char(205); }      cout << char(188) << endl;

		setcolor(32);
		printf("\n\t\t"); cout << char(201);      for (int i = 0; i < 14; i++) { cout << char(205); }      cout << char(187) << endl;
		printf("\t\t"); cout << char(186) << " 3. Vorood    " << char(186) << endl;
		printf("\t\t"); cout << char(200);      for (int i = 0; i < 14; i++) { cout << char(205); }      cout << char(188) << endl;
		setcolor(7);
	}

	setcolor(135);
	printf("\n\t\tEnter Your Choise : ");
	scanf("%d", &choise);

	switch (choise)
	{
	case 1:
		Moshahede_Kala_Main_Menu();
		break;
	case 2:
		Sabt_Nam();
		break;
	case 3:
		Vorood();
		break;
	}

	{
		setcolor(224);
		printf("\n\n\n");
		return 0;
	}
}

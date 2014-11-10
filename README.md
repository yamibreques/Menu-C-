Menu-C-
=======

El siguiente programa exhibe en pantalla las opciones propuestas en el menú

#include <iostream>
using namespace std;

int main(int argc, char *argv[]) {
	
	char op;
	int dato;
	bool hay_dato = false;
	
	do {
		
		cout<<"Disenio de menus en c++"<<endl<<endl;
		
		cout<<"CALCULOS"<<endl<<endl;
		cout<<"A- Ingresar nuevo dato."<<endl;
		cout<<"B- Calcular el doble del dato."<<endl;
		cout<<"C- Determinar si es par."<<endl;
		cout<<"D- Determinar si es primo."<<endl;
		cout<<"E- Salir."<<endl;
		cout<<"	Elija una Opcion (A..E): ";
		cin>>op;
		
		//segun de pseint
		switch (op) {
		
		case 'A':
			cin>>dato;
			hay_dato=true;
			break;
			
		case 'B':
			
			if (hay_dato) {
				cout<<2*dato; }
			else { 
				cout<<"Error, no hay dato"; 
			break; 
			}
			
			
		case 'C':
			
			if (hay_dato) { 
				
				if (dato % 2 == 0) {
					cout<<"Es par"; 
				} else {
					cout<<"Es impar";
				}
				
			else{ 
				cout<<"No hay dato"; 
				break;
				}
			}
			
		case 'D':
			if (hay_dato) {
				
				
				bool primo = true;
				int i=2;
				while ((i<dato) && (!primo)); {
					
					if (dato % i == 0) {
						primo = false;
					}
				i++;
				}
				if (primo) {
					cout<<"Primo";}
				else {
					cout<<"No es Primo";
				}
			} else {
				cout<<"No hay dato";
				break;
			}
			
			
		case 'E': 
			break;
			
		default: 
			cout<<"Opcion Invalida";
		
		}
	while (op!='E');
	}
	
	return 0;}


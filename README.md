#include <iostream>
#include <fstream>

using namespace std;

int main(int argc, char** argv) 
{
	
	cout << "Content-type: text/html\n\n"
         "<html>"
          "<head>"
           "<title>Zmienne POST-T</title>"
           "</head>"
           "<body>";
           
            fstream plik;  
            int t[1000];
            int i=0;
            double srednia=0;
            
   plik.open("ocena.txt", ios::in);  
   if(plik.good()) 
            while(!plik.eof())
            {
            	      
            	plik>>t[i];
            		srednia+=t[i];
            		i++;
            
            }
			plik.close();
            
            	srednia=srednia/i;
        
	cout << "<h1>Srednia : </h1>"<< srednia;
	
	cout << "</body>"
			"</html>";		
	return 0;
}

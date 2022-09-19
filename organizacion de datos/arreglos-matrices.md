# Arreglos/Matrices

Codigo para generar una matriz.
```Java
public class matriz{
	public static void main(String[] args){
		Scanner sc=new Scanner(System.in);
		System.out.print("Ingrese orden de la matriz");
		int n=sc.nextInt();
	
		string m[][]=new String[n][n];
		system.out.println("Matriz completa");
		for(int i=0;i<n;i++){
			for(int j=0;j<n;j++){
			m[i][j]=("*");
			system.out.print(m[i][j]);
			}
			system.out.println("");
			
		}
	}
}
```

Este codigo genera una matriz, pero unicamente como dibujo en ASCII
00000
00000
00000    Matriz de 5x5
00000
00000


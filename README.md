import java.util.Scanner;

public class bankamatik {

	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		int bakiye = 6000;
		System.out.println("Bakiyeniz: "+bakiye);
		while(true) {
			System.out.println("İşlem 1:Para yatır"+" "+"İşlem 2.Para çek"+" "+"İşlem 3:Bakiye güncele"+" "+"İşlem 4:Çıkış");
			int tercih = input.nextInt();
			switch (tercih) {
			case 1:
				System.out.println("Yatırmak istediğiniz tutarı girin: ");
				int miktary = input.nextInt();
				bakiye += miktary;
						System.out.println("Güncel bakiye: "+bakiye);
						break;
			case 2:
				System.out.println("Çekmek istediğiniz tutarı girin: ");
				int miktarc = input.nextInt();
				if(miktarc > bakiye) {
					System.out.println("=Yetersiz bakiye=");
				}else {
				bakiye -= miktarc;
						System.out.println("Güncel bakiye: "+bakiye);
						}
				break;
			case 3:
				System.out.println("Güncel bakiyenizi giriniz: ");
				int yenimiktar= input.nextInt();
				bakiye = yenimiktar;
						System.out.println("Yeni bakiye: "+bakiye);
						break;
		}
			if(tercih == 4) {
				System.out.println("Çıkış yapıldı");
				break;
			}
			}
	}

	}

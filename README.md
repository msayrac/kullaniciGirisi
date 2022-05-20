# kullaniciGirisi
import java.sql.SQLOutput;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        String userName, password;
        Scanner input = new Scanner(System.in);
        System.out.println("Lutfen isminizi giriniz : ");
        userName = input.nextLine();
        System.out.println("my name is " + userName);
        System.out.println("Pasword giriniz : ");
        password = input.nextLine();
        System.out.println("password " + password);
        if (userName.equals("patika") && password.equals("java123")) {
            System.out.println("hosgeldiniz Giris yapiniz");
        } else {
            System.out.println("Bilgileriniz yanlis");
            System.out.println("Sifrenizi sifirlamak istermisiniz Y or N");
            String approve, newPassword;
            approve = input.nextLine();
            if (approve.equals("Y") || approve.equals("y")) {
                System.out.println("Yeni sifre eski sifre ve hatali sifre ile ayni olmamali. Yani sifrenizi giriniz");
                newPassword = input.nextLine();
                if (newPassword.equals("java123")) {
                    System.out.println("Eski sifrenizi kullanamazsiniz");
                } else {
                    System.out.println("Sifre olusturuldu ");
                    System.out.println("yeni paralo : " + newPassword);
                    return;
                }
            } else {
                System.out.println("Eski Sifrenizle tekrar giris yapabilirsiniz");
            }
        }
    }
}

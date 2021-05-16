# calculadora.java

import java.util.Scanner;

import java.text.SimpleDateFormat;

import java.util.Date;

import java.text.DateFormat;

import java.text.ParseException;

import java.util.Locale;

public class teste700

{

    public static void main(String[]args){

    Scanner sc = new Scanner(System.in);

   

    System.out.println("Por favor insira o nome do anuncio: ");

    String nome_anuncio = sc.nextLine();

   

    System.out.println("Por favor insira o nome do cliente: ");

    String nome_cliente = sc.nextLine();

        try{

       

       

       

        //primeira parte da data, input da data em String

        System.out.println("Por favor insira a data inicial: ");

        String dataInicial = sc.nextLine();

       

        //Formula para alterar a String para formato dia,mes e ano

        DateFormat di = new

        SimpleDateFormat("dd/MM/yyyy");  

       

        Date dataum = di.parse(dataInicial);

       

        System.out.println(di.format(dataum));

       

       

        //Segunda parte da data, input da data em String  

               

        System.out.println("Por favor insira a data final: ");

        String dataFinal = sc.nextLine();

       

        //Formula para alterar a String para formato dia,mes e ano

        DateFormat df = new

        SimpleDateFormat("dd/MM/yyyy");

               

        Date datadois = df.parse(dataFinal);

       

        System.out.println(df.format(datadois));

       

       

        //subtracao do valor das datas

       

        long diffEmMil = Math.abs(datadois.getTime() - dataum.getTime());

        double diff = (int) (diffEmMil/(1000 * 60 * 60 * 24));

           

        //calculando o valor total do investimento

        System.out.println("Por favor insira o valor do investimento para um dia: ");

        double investimento = sc.nextDouble();

   

        double total;

        total = diff*investimento;

       

        //calculadora

        double visuori,click,comp,visu,maxcom;

        visuori = total*30;

        click = (visuori*12)/100;

        comp = (click*3)/20;

        visu = comp*40;

        maxcom = comp*4;

       

        //imprimindo resultados

        System.out.print("Anuncio: "+ nome_anuncio+"\nCliente: "+nome_cliente);

        System.out.format("\nO valor total investido é de: R$%.2f", total);

        System.out.format("\nQuantidade maxima de visualizacoes: %.0f", visu);

        System.out.format("\nQuantidade maxima de cliques: %.0f", click);

        System.out.format("\nQuantidade maxima de compartilhamentos: %.0f", maxcom);

       

       

    } catch (Exception ex) {    

    ex.printStackTrace();

    }

   

   

    }

}

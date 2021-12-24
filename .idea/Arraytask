package com.full.school;

import java.util.Scanner;

public class Problem2 {
    int count;
    int sizeofArray;
    int array[];
    public  Problem2(){
        count=0;
        sizeofArray=1;
        array = new int[1];
    }

    public void addElement(int num){
        if(sizeofArray == count){
            growArray();
        }
        array[count] = num;
        count++;
    }

    public void addElement(int index,int num){
        if(count == sizeofArray){
            growArray();
        }
        for (int i = count-1; i >= index; i--) {
            array[i+1]=array[i];
        }
        array[index]= num;
        count++;
    }

    public void removeElement(){
        if(count > 0){
            array[count-1]=0;
        }
        count--;
        shrinkArray();
    }


    public void removeElement(int index){
        int i;
        array[index]=0;
        for  (i = index; i < count-1; i++) {
            array[i]=array[i+1];
        }
        array[i]=0;
        count--;
        shrinkArray();

    }

    public void setElement(int index,int num){
        array[index]= num;
    }

    public void growArray(){
        int temp[]=null;
        if(sizeofArray == count){
            temp = new int[sizeofArray *2];
            for (int i = 0; i <sizeofArray ; i++) {
                temp[i] = array[i];
            }
        }
        array=temp;
        sizeofArray= sizeofArray*2;
    }

    public void shrinkArray(){
        int temp[]=null;
        temp = new int[count];
        for (int i = 0; i <count ; i++) {
            temp[i] = array[i];
        }
        array=temp;
    }

    public void printElements(){
        for (int i = 0; i < array.length; i++) {
            if(array[i] != 0){
                System.out.print(array[i] + " ") ;
            }
        }
    }


    public static void main(String[] args) {
        Problem2 problem2 = new Problem2();
        Scanner input = new Scanner(System.in);
        System.out.println("Enter number of values to added in array : ");
        int times = input.nextInt();
        for (int i = 0; i <times ; i++) {
            System.out.println("Enter the value : ");
            problem2.addElement(input.nextInt());
        }
        System.out.println("Print the Array elements : ");
        problem2.printElements();
        System.out.println();

        System.out.println("Enter the value to added in the array : ");
        problem2.addElement(input.nextInt());
        System.out.println("Print the Array elements : ");
        problem2.printElements();
        System.out.println();


        System.out.println("Enter the index and value  to added in the array : ");
        problem2.addElement(input.nextInt(), input.nextInt());
        System.out.println("Print the Array elements : ");
        problem2.printElements();
        System.out.println();

        System.out.println("Enter the index and value to be reset :  ");
        problem2.setElement(input.nextInt(), input.nextInt());
        System.out.println("Print the Array elements : ");
        problem2.printElements();
        System.out.println();

        System.out.println("Enter index to delete element ");
        problem2.removeElement(input.nextInt());
        System.out.println("Print the Array elements : ");
        problem2.printElements();
        System.out.println();

        System.out.println("Enter the index to get the value : ");
        int get= input.nextInt();
        System.out.println("The value in the given index is : "+problem2.array[get]);
    }
}

 public static void main(String[] args) {
        //1.Write a Java program to test if the first and the last element of an array of integers are same. The length of the array must be greater than or equal to 2
        System.out.println("Q1");
        int [] arr={50, -20, 0, 30, 40, 60, 10};
        if(arr[0]==arr[arr.length-1]){
            System.out.println(true);
        }
        else{
            System.out.println(false);
        }

        //2.Write a Java program to find the k largest elements in a given array. Elements in the array can be in any order.
        System.out.println("Q2");
        int [] arr2={1, 4, 17, 7, 25, 3, 100};
        Arrays.sort(arr2);
        System.out.println(arr2[arr2.length-1]+","+arr2[arr2.length-2]+","+arr2[arr2.length-3]);

        //3.Write a Java program to find the numbers greater than the average of the numbers of a given array.
        System.out.println("Q3");
        int [] arr3={1, 4, 17, 7, 25, 3, 100};
        ArrayList<Integer> great=new ArrayList<Integer>();

        int avarg=0;
        for(int i =0;i<arr3.length;i++){

            avarg+=arr3[i];
        }

        avarg=avarg/arr3.length;
        for(int y :arr3){
            if(y>avarg){
                great.add(y);
            }
        }
        System.out.println("The average of the said array is: "+avarg+" The numbers in the said array that are greater than the average are: "+great);

        //4.Write a Java program to get the larger value between first and last element of an array of integers.
        System.out.println("Q4");
        int [] arr4={20, 30, 40};
        int gr=arr4[0];
        int gre=arr4[arr4.length-1];
        int res4=0;
        if(gr>gre){
            res4=gr;
        }
        else {
            res4=gre;
        }
        System.out.println("Larger value between first and last element:"+res4);

        //5.Write a Java program to swap the first and last elements of an array and create a new array.
        System.out.println("Q5");
        int [] arr5={20, 30, 40};
        int firstEm=arr5[0];
        int endEm=arr5[arr5.length-1];
        arr5[0]=endEm;
        arr5[arr5.length-1]=firstEm;
        System.out.println(Arrays.toString(arr5));

        //6.Write a Java program to find all of the longest word in a given dictionary.
        System.out.println("Q6");
        String [] strs={"cat", "dog", "red", "is", "am"};
        int larg=strs[0].length();
        for(String s:strs){
            if(s.length()>=larg){
                larg=s.length();
            }
        }
        for(String str:strs){
            if(str.length()==larg){
                System.out.print(" "+str);
            }

        }
        System.out.println();

        //7.Write a menu driven Java program with following option:
        System.out.println("Q7");
        Scanner s=new Scanner(System.in);
        boolean isRun=true;
        System.out.println("Please Enter the Size Array");
        int sizeArray=s.nextInt();
        String [] elmn=new String[sizeArray];
        while (isRun){

            System.out.println("a. Accept elements of an array b. Display elements of an array c. Search the element within array d. Sort the array if want exit enter any key");
            s.nextLine();
            String opt=s.nextLine();


            switch (opt){
                case "a":
                case "A":
                    for(int i=0;i<elmn.length;i++){
                        System.out.println("Enter item number");
                        String ite=s.nextLine();
                        elmn[i]=ite;
                    }
                    break;
                case "b":
                case "B":
                    for( String i : elmn){
                        System.out.println(i);
                    }
                    break;
                case "c":
                case "C":
                    System.out.println("Please Enter the Item want to search");
                    String word=s.nextLine();
                    boolean isFound=false;
                   for(String i :elmn){
                       if(i.equalsIgnoreCase(word)){
                           isFound=true;

                       }
                       if(isFound){
                           System.out.println(word+" is found");
                       }
                       else{
                           System.out.println(word+" is not found");
                       }

                   }
                    break;
                case "d":
                case "D":
                    Arrays.sort(elmn);
                    System.out.println(Arrays.toString(elmn));
                    break;
                default:
                    System.out.println("Option Error");
                    isRun=false;
                    break;
            }
        }



        //8. Write a program thats displays the number of occurrences of an element in the array.
        System.out.println("Q8");
        int [] aar8={1,1,1,3,3,5};
        ArrayList<Integer> elemnt=new ArrayList<>();
        ArrayList<Integer> Item=new ArrayList<>();
        int [] occ=new int[aar8.length];
        for(int i=0;i<aar8.length;i++){
            int count =0;
            for(int y=0;y<aar8.length;y++){
                if(aar8[i]==aar8[y]){
                    count++;
                }
            }
            if (!elemnt.contains(aar8[i])) {

                elemnt.add(aar8[i]);
                Item.add(count);
            }
            occ[i]=count;

        }

        for(int i=0;i<elemnt.size();i++){
            System.out.println(elemnt.get(i)+" occurs "+ Item.get(i) +" times");
        }

        //9. Write a program that places the odd elements of an array before the even elements.
        System.out.println("Q9");
        int [] ar9={2,3,40,1,5,9,4,10,7};
        ArrayList<Integer> odd=new ArrayList<Integer>();
        ArrayList<Integer> even=new ArrayList<Integer>();
        ArrayList<Integer> result=new ArrayList<Integer>();



        for(int i =0;i<ar9.length;i++){
            if(ar9[i]%2==0){
                even.add(ar9[i]);
            }
            else{
                odd.add(ar9[i]);
            }
        }

        odd.addAll(even);

        System.out.println(odd);

        //10.Write a program that test the equality of two arrays.
        System.out.println("Q10");
        int [] a1={2,3,6,6,4};
        int [] a2={2,3,6,6,4};
        int sum1=0;
        int sum2=0;
        for(int i1:a1){
            sum1+=i1;
        }
        for(int i2:a2){
            sum2+=i2;
        }
        if(sum1==sum2){
     System.out.println(true);
        }
        else{
            System.out.println(false);
        }



    }

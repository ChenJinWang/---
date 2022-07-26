# ---
1、冒泡排序

</br>
class PetApplicationTests {

    @Test
    void contextLoads() {
    }

    @Test
    public static void Demo(int[] arr){
        boolean flag = false;
        for (int i = 0; i<arr.length; i++){
                for (int j = i + 1; j<arr.length; j++){
                    if (arr[i]>arr[i+1]){
                        flag = true;
                        int temp = arr[i];
                        arr[i] = arr[j];
                        arr[j] = temp;
                    }
                }
            if (!flag){
                break;
            }
            else {
                flag = false;
            }
        }
    }

    public static void main(String[] args){
        int arr[] = {1,-10,30,4};
        System.out.println("冒泡排序前：");
        System.out.println(Arrays.toString(arr));
        Demo(arr);
        System.out.println("冒泡排序后：");
        System.out.println(Arrays.toString(arr));
    }
}

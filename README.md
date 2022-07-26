# leanring
学习-数据结构：选择排序
class PetApplicationTests {

    @Test
    void contextLoads() {
    }



    @Test
    public static void Demo(int[] arr){
        for (int i = 0; i < arr.length; i++){
            int minIndex = i;
            for (int j = minIndex + 1; j < arr.length; j++){
                if (arr[j]<arr[minIndex]){
                    minIndex = j;
                }
            }
            int temp = arr[i];
            arr[i] = arr[minIndex];
            arr[minIndex] = temp;
        }
    }

    public static void main(String[] args){
        int arr[] = {1,-10,30,4,22};
        System.out.println("选择排序前：");
        System.out.println(Arrays.toString(arr));
        Demo(arr);
        System.out.println("选择排序后：");
        System.out.println(Arrays.toString(arr));
    }
}

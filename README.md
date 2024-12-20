public class DynamicArray {
    int[] marks;
    int index;

    DynamicArray()
    {
        marks = new int[1];
        index = 0;
    }
    public void insert(int item)
    {
        if(index==marks.length)
        {
            int[] temp = new int[marks.length+1];
            for(int i=0;i<marks.length;i++)
            {
                temp[i] = marks[i];
            }
            marks = temp;
        }
        marks[index++] = item;
    }

    public int get(int index) {
        return marks[index];
    }

    public int size() {
        return index;
    }


    public String print()
    {
        String result = "";
        for(int i=0;i<index;i++)
        {
            result += " "+marks[i];
        }
        return result;
    }
}

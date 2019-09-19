# CodeFragment

1. 对spiner设置到指定位置：
    ```
    /**
     * spinner 设置为指定数据
     * @param dmz
     * @param spinner
     */
    public static void setSpinnerToDmz(String dmz,Spinner spinner){  
        if(TextUtils.isEmpty(dmz)){return;}  
        ArrayAdapter<String> adapter = (ArrayAdapter<String>) spinner.getAdapter();  
        int count = adapter.getCount();  
        for (int i = 0; i <count; i++) {  
            String item = adapter.getItem(i);  
            String adapterDmz = item.split(":")[0];  
            if(dmz.equals(adapterDmz)){  
                spinner.setSelection(i);  
                break;  
            }  
        } 
     }  
    ```
  

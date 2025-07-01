# UART鮑率(115200))

電路圖

![image](https://github.com/user-attachments/assets/961b3661-d432-413f-bc1b-bf2374d57950)


        

![image](https://github.com/user-attachments/assets/8928f946-b17d-451d-9a42-7c5f5cae8eb5)

-黃框為tx_ready高態為一筆資料


## UART FSM順序

- TX的FSM TX_IDLE->TX_START_BIT->TX_DATA_BIT->TX_STOP_BIT->TX_CLEANUP

  ![image](https://github.com/user-attachments/assets/d5fce55a-f7d8-4c85-97cb-6d95e48420de)

  
- RX的FSM RX_IDLE->RX_START_BIT->RX_DATA_BIT->RX_STOP_BIT->RX_CLEANUP

  ![image](https://github.com/user-attachments/assets/cb67c7a6-a55d-496f-b3b3-47be812bd16b)



## 測試的方式

- ## input data:
  
- tx_data_tb  <= "00011"  tx_start='1';


![image](https://github.com/user-attachments/assets/aa75a919-a5dc-4afd-85ea-e16fc1e6e872)


tx_data_tb  <= "01001" tx_start='1';

![image](https://github.com/user-attachments/assets/cc02ad78-d539-4c47-b01e-581102b6d0f1)


tx_data_tb  <= "10001" tx_start='1';

![image](https://github.com/user-attachments/assets/261117d8-2d29-4673-80e6-6fcc9d848f3c)
### outputdata

- rx_data_tb="00011"

  ![image](https://github.com/user-attachments/assets/e6f0c384-2743-4ec4-a479-fa0c91125384)

- rx_data_tb="01001"

  ![image](https://github.com/user-attachments/assets/d2d69dcd-af9b-49f6-a406-0b14a4f4ebf1)


- rx_data_tb="10001"

![image](https://github.com/user-attachments/assets/ed49f85e-6349-4f79-bce2-e22d7cf7da59)
- 紅框為rx_ready='1''




            



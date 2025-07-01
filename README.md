# UART

## UART FSM順序

- TX的FSM TX_IDLE->TX_START_BIT->TX_DATA_BIT->TX_STOP_BIT->TX_CLEANUP
  
- RX的FSM RX_IDLE->RX_START_BIT->RX_DATA_BIT->RX_STOP_BIT->RX_CLEANUP


## 測試的方式

input data: tx_data_tb  <= "00011"  tx_start='1';

            tx_data_tb  <= "01001" tx_start='1';

            tx_data_tb  <= "10001" tx_start='1';
            
電路圖

![image](https://github.com/user-attachments/assets/961b3661-d432-413f-bc1b-bf2374d57950)


        

![image](https://github.com/user-attachments/assets/8928f946-b17d-451d-9a42-7c5f5cae8eb5)

-黃框為tx_ready高態為一筆資料



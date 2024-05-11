# VDT-RGB-WhiteLED-control

Thêm ứng dụng dim LED bên trong hàm callback() (từ line 150)
```
    else if(messageTemp.indexOf("dim") != -1){
    control_white = 1;
    Serial.println("dim white");
    int dimlevelIndex = messageTemp.indexOf(':');
    int dimlevel = messageTemp.substring(dimlevelIndex + 1).toInt();
    analogWrite(WARM_WHITE, int(dimlevel/100.0*255));
    send_message_mqtt("white","dim");
    }
```



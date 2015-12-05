編輯  
/etc/ssh/sshd_config
修改  
PermitRootLogin without-password
為  
PermitRootLogin yes
執行  
/etc/init.d/ssh restart
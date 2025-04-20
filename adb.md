# adb

Lista:

```bash
# Lista todos os aplicativos
adb shell pm list packages    

# Lista apenas aplicativos de terceiros (não os do sistema)
adb shell pm list packages -3 

# Lista apenas aplicativos do sistema
adb shell pm list packages -s 

# Inclui aplicativos desinstalados recentemente
adb shell pm list packages -u 

# Mostra o caminho do arquivo APK de cada aplicativo
adb shell pm list packages -f 
```

Remoção:

```bash
# Remove completamente o aplicativo
adb shell pm uninstall <package_name>          

# Remove o aplicativo, mas mantém os dados e cache
adb shell pm uninstall -k <package_name>

# Desinstala o aplicativo apenas para o usuário principal, útil para remover apps pré-instalados sem root
adb shell pm uninstall --user 0 <package_name>
```

## Instruciones para habilitar la configuracion
```bash
git clone https://github.com/albertoCaroM/dotgdb.git  ~/.gdb
rm .gdbinit 
ln -s ~/.gdb .gdbinit
```

### Crear .gdbinit por proyecto
Para añadir un fichero .gdbinit con intrucciones personalizadas para un proyecto, añadir al fichero ~/.gdb/safe_path "add-auto-load-safe-path path_a_la_carpeta"

Ejemplo: "add-auto-load-safe-path /home/alberto/repositorios/linphone/.gdbinit"

####ejemplo de fichero .gdbinit en proyecto , tambien se puede usar ./dotgdbinit.example.forProject renonmbrado a .gdbinit en la carpeta del proyecto 

```gdb
file  ./gtk/.libs/linphone
set args --verbose
set breakpoint pending on
source breaks 
```

De esta manera se pueden salvar los breakpoints que estemos usando en una sesion, con el comando "save breakpoints breaks" 


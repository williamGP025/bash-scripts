# Como hacer que un alias sea permanente #

### Averiguar la shell o terminal que estamos usando. ###
echo "$SHELL"

### Editar la lista de alias ###
nano ~/.bashrc

## Mis alias ##

### Crear un directorio y acceder directamente al directorio creado. ###
alias mkdircd='function _mkdircd(){ mkdir -p "$1"; cd "$1"; };_mkdircd'
### Encontrar un comando en el historial de la terminal mediante el comando gh ###
alias gh="history | grep"
### Usar el comando count para contar los ficheros que contiene un directorio.###
alias count="find . -type f | wc -l"
### Listar los puertos abiertos en nuestro equipo.###
alias ports="netstat -tulanp"
### Cada 3 segundos mostrar los 10 procesos que consumen más CPU con el comando cpu10 ###
alias cpu10='watch -n 3 "free; echo; uptime; echo; ps aux --sort=-%cpu | head -n 11; echo; who"'
### Cada 3 segundos mostrar los 10 procesos que consumen más RAM con el comando mem10 ###
alias mem10='watch -n 3 "free; echo; uptime; echo; ps aux --sort=-%mem | head -n 11; echo; who"'
### Actualizar repos de linux ###
alias update="sudo apt-get update"
### Apagar server ###
alias pof="sudo shutdow -h now"
### Reiniciar server ###
alias rof="sudo shutdow -r now"
### Cerrar todas las sesiones de tmux ###
alias etx="pkill -f tmux"

# Power Shell Shortcuts

## Atalhos

Comando = CmdLet
Padrão: Verbo+Substantivo

Ctrl+Backspace or Delete
Deletar palavra a frente ou atrás

Shift+Control+Seta
Seleciona palavra inteira

Esq
Apaga linha inteira

Tab auto completa os comandos

---

## Comandos

cp
Igual ao comando copy

erease
Igual ao comando delete

ni
Comando para criar arquivo: ni test.txt

---

## Cmdlet

Clear-Host
Igual ao comando cls ou clear

Get-ChildItens
Igual ao comando dir ou ls

Get-Command
Exibe os comandos que exitem

Get-Command Get-Host
Exibe especificamente informações desse comando

Get-Command -CommandType Cmdlet
Exbie todos os comandos do tipo Cmdlet

Get-Location
Igual ao comando pwd ou gl

Get-Help
Exibe a ajuda do comando: Get-Help erase

Get-Host
Mostra informações de versões e sessão

Set-Location
Igual ao comando cd

Show-Command
Exibe janela do PowerShell ISE

Update-Help
Atualiza a base de ajuda

---

Mapear pasta na rede
New-PSDrive –Name "R" –PSProvider FileSystem –Root '\\fswcorp\cto\sauti\gas\POLOS_REPOSITORIOS\REGIONAIS\HP\RJ-CENTRO" –Persist
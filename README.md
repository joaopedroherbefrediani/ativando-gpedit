## Instalando o GPEDIT em máquinas de versões antigas

### Tutorial da instalação

1. Na tecla do Windows pesquise por `cmd`
2. Execute ele em modo administrador
3. Cole a linha de comando abaixo para executar o Script no CMD

```powershell
FOR %F IN ("%SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientTools-Package~*.mum") DO (DISM /Online /NoRestart /Add-Package:"%F")
```

4. Depois de concluir o primeiro passo, refaça o procedimento 1. e 2.
5. Cole a segunda linha de comando abaixo para finalizar a instalação
6. Reinicie o computador

```powershell
FOR %F IN ("%SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientExtensions-Package~*.mum") DO (DISM /Online /NoRestart /Add-Package:"%F")
```

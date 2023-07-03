# ativando-gpedit
Como ativar o gpedit.msc no windows

1 - Abra o CMD como administrador e em seguida execute o seguinte comando:

FOR %F IN ("%SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientTools-Package~*.mum") DO (DISM /Online /NoRestart /Add-Package:"%F")

2 - Após concluir o primeiro passo execute o ultimo comando a seguir:

FOR %F IN ("%SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientExtensions-Package~*.mum") DO (DISM /Online /NoRestart /Add-Package:"%F")

Pronto, seu computador estará pronto para usar o gpedit.msc

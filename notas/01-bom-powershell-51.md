# UTF-8 com BOM no PowerShell 5.1

O Windows PowerShell 5.1 grava UTF-8 **com** BOM (`EF BB BF`). `-Encoding utf8` não ajuda: nessa versão `utf8` *significa* "com BOM". O `utf8NoBOM` só existe do PowerShell 6 em diante.

Quebra em silêncio: `--cli-input-json` do AWS CLI, `.env` lido pelo Docker, YAML de CI, PEM.

```powershell
[System.IO.File]::WriteAllText("$PWD\c.json", $json, (New-Object System.Text.UTF8Encoding $false))
```

Diagnóstico em uma linha: `Format-Hex arquivo | Select-Object -First 1`.

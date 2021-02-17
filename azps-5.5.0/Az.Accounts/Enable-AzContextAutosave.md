---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229511"
---
# Enable-AzContextAutosave

## SYNOPSIS
Azure-sammanhang är PowerShell-objekt som representerar din aktiva prenumeration att köra kommandon mot och den autentiseringsinformation som behövs för att ansluta till ett Azure-moln. Med Azure-sammanhang behöver Inte Azure PowerShell ändra ditt konto varje gång du byter prenumeration. Mer information finns i Azure [PowerShell-sammanhangsobjekt.](https://docs.microsoft.com/powershell/azure/context-persistence)

Med den här cmdleten kan kontextinformationen för Azure sparas och läsas in automatiskt när du startar en PowerShell-process. Till exempel när du öppnar ett nytt fönster.

## SYNTAX

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING

Gör att azure-kontextinformationen sparas och läses in automatiskt när en PowerShell-process startas. Kontexten sparas i slutet av körningen av en cmdlet som påverkar sammanhanget. Till exempel en cmdlet för profil. Om du använder användarautentisering kan token uppdateras under hela körningen av en cmdlet.

## EXEMPEL

### Exempel 1: Aktivera autentiseringsuppgifter för automatiskt sparat för den aktuella användaren

Aktivera spara automatiskt autentiseringsuppgifter för den aktuella användaren. När ett PowerShell-fönster öppnas sparas det aktuella sammanhanget utan att du loggar in.

```powershell
Enable-AzContextAutosave
```

### Exempel 2

Tillåt att Azure-autentiseringsuppgifter, konto- och prenumerationsinformation sparas och läses in automatiskt när du öppnar ett PowerShell-fönster i den här PowerShell-sessionen. (autogenererat)

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## PARAMETERS

### -DefaultProfile

Autentiseringsuppgifter, klientorganisation och prenumeration som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Omfattning

Avgör omfattningen av sammanhangsändringar. Till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som startas av den här användaren. Ändringar som görs med omfattningen `CurrentUser` påverkar alla PowerShell-sessioner som startas av användaren. Om en viss session behöver ha olika inställningar använder du `Process` omfånget.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta

Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Visar vad som skulle hända om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Vanliga parametrar

Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings

## ANTECKNINGAR

## RELATERADE LÄNKAR

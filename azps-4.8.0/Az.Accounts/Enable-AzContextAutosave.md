---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259652"
---
# Enable-AzContextAutosave

## Sammanfattning
Azure-kontexter är PowerShell-objekt som representerar ditt aktiva abonnemang för att köra kommandon mot och autentiseringsinformation som behövs för att ansluta till ett Azure-moln. Med Azure-kontexter behöver Azure PowerShell inte omverifiera ditt konto varje gång du byter abonnemang. Mer information finns i [kontext objekt för Azure PowerShell](https://docs.microsoft.com/powershell/azure/context-persistence).

Denna cmdlet gör att Azure context-informationen sparas och läses in automatiskt när du startar en PowerShell-process. Till exempel när du öppnar ett nytt fönster.

## FRÅGESYNTAXEN

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING

Gör att Azure context-informationen sparas och läses in automatiskt när en PowerShell-process startas. Kontexten sparas i slutet av körningen av en cmdlet som påverkar kontexten. Till exempel alla profil-cmdletar. Om du använder användarautentisering kan token uppdateras när en cmdlet körs.

## BESKRIVS

### Exempel 1: Aktivera Autospara-autentiseringsuppgifter för den aktuella användaren

Aktivera Spara automatiskt för den aktuella användaren. När ett PowerShell-fönster öppnas sparas din nuvarande kontext utan att logga in.

```powershell
Enable-AzContextAutosave
```

### Exempel 2

Tillåt att Azure Credential, konto-och prenumerations information sparas och läses in automatiskt när du öppnar ett PowerShell-fönster i den här PowerShell-sessionen. (automatiskt genererat)

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## MALLPARAMETRAR

### -DefaultProfile

Autentiseringsuppgifter, klient organisationen och prenumerationen som används för kommunikation med Azure

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

Avgör omfattningen av kontext ändringar. Till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar. Ändringar som görs med omfattningen `CurrentUser` påverkar alla PowerShell-sessioner som användaren startat. Om en speciell session måste ha olika inställningar använder du omfattningen `Process` .

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

Du uppmanas att bekräfta innan du kör cmdleten.

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

Visar vad som händer om cmdleten körs.
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

Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. kommandon. Common. inloggningsautentisering. ContextAutosaveSettings

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: b0b91e2892f087da6eb510d087980e6f31dd67ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754468"
---
# Set-AzVMAccessExtension

## Sammanfattning
Lägger till VMAccess-tillägget på en virtuell dator.

## FRÅGESYNTAXEN

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzVMAccessExtension** lägger till den virtuella datorns VMAccess-tillägg till en virtuell dator. VMAccess-tillägget kan användas för att ange ett tillfälligt lösen ord och det bör ändras direkt efter att du har loggat in på datorn. Det här stöds inte på Windows-domänkontrollanter.

## BESKRIVS

### Exempel 1: lägga till ett VMAccess-tillägg
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

Det här kommandot lägger till ett VMAccess-tillägg för den virtuella datorn med namnet VirtualMachine07 i ResrouceGroup11.
Kommandot anger namn och typ av hanterarmappning för VMAccess.

## MALLPARAMETRAR

### -Autentiseringsuppgift
Anger användar namn och lösen ord för den virtuella datorn som ett **PSCredential** -objekt.
Om du skriver ett annat namn än det nuvarande lokala administratörs kontot på din virtuella dator, lägger VMAccess-tillägget till ett lokalt administratörs konto med det namnet och tilldelar ditt lösen ord till kontot. Om det lokala administratörs kontot på din VM finns återställs lösen ordet och om kontot är inaktiverat aktiverar VMAccess-tillägget det.
För att få en autentiseringsuppgift, Använd cmdleten Get-Credential.
Om du vill ha mer information skriver du `Get-Help Get-Credential` .

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -DisableAutoUpgradeMinorVersion
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceRerun
Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.
Värdet kan vara en annan sträng än det aktuella värdet.
Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plats
Anger platsen för den virtuella datorn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på tillägget som läggs till i cmdleten.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den virtuella datorns resurs grupp.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
Anger vilken version av tillägget som ska användas för den här virtuella datorn.
För att hämta versionen kör du Get-AzVMExtensionImage cmdlet med värdet Microsoft. Compute for the *PublisherName* parameter och VMAccessAgent för parametern *Type* . TypeHandlerVersion måste vara 2,0 eller senare, eftersom version 1 är föråldrad.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Anger namnet på en virtuell dator.
Denna cmdlet lägger till VMAccess för den virtuella datorn som den här parametern anger.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. Management. Automation. PSCredential

### System. String

### System. Management. Automation. SwitchParameter

## VÄRDEN

### Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzVMAccessExtension](./Get-AzVMAccessExtension.md)

[Remove-AzVMAccessExtension](./Remove-AzVMAccessExtension.md)

[Set-AzVMExtension](./Set-AzVMExtension.md)

[Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md)



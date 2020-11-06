---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: edc91b756b90684299d84228c04862a0ce6c2e21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573517"
---
# Set-AzureRmVMAEMExtension

## Sammanfattning
Aktiverar support för övervakning för SAP-system.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmVMAEMExtension** uppdaterar konfigurationen av en virtuell dator för att aktivera eller uppdatera supporten för övervakning för SAP-system som är installerade på den virtuella datorn.
Denna cmdlet installerar den AEM-anknytning (Azure Enhanced Monitoring) som samlar in prestanda data och gör det synligt för SAP-systemet.

## BESKRIVS

### Exempel 1: använda AEM-tillägget
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

Det här kommandot konfigurerar den virtuella datorn som heter Contoso-server att använda AEM-tillägget.
Kommandot anger lagrings kontot som heter stdstorage.

## MALLPARAMETRAR

### -DisableWAD
Anger att denna cmdlet inte aktiverar Azure Diagnostics för den virtuella datorn.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWAD
Om den här parametern tillhandahålls aktiverar cmdleten Windows Azure Diagnostics för den här virtuella datorn.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSType
Visar operativ systemets operativ system.
Om operativ system disken inte har en typ måste du ange den här parametern.
De acceptabla värdena för denna parameter är: Windows och Linux.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resurs gruppen för den virtuella datorn som denna cmdlet ändrar.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipStorage
Anger att denna cmdlet hoppar över konfigurering av lagrings utrymme.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
Anger namnet på en virtuell dator.
Denna cmdlet lägger till AEM-tillägget för den virtuella datorn som den här parametern anger.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WADStorageAccountName
Anger namnet på det lagrings konto som används i cmdleten för att konfigurera LinuxDiagnostics-eller IaaSDiagnostics-tillägget.
Om den virtuella datorn inte använder ett standard lagrings konto måste du ange ett värde för den här parametern.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmVMAEMExtension](./Get-AzureRmVMAEMExtension.md)

[Remove-AzureRmVMAEMExtension](./Remove-AzureRmVMAEMExtension.md)

[Test-AzureRmVMAEMExtension](./Test-AzureRmVMAEMExtension.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236431"
---
# Update-AzCustomIpPrefix

## SYNOPSIS
Uppdaterar ett CustomIpPrefix

## SYNTAX

### UpdateByNameParameterSet
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### UpdateByInputObjectParameterSet
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UpdateByResourceIdParameterSet
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Med **cmdleten Update-AzCustomIpPrefix** kan användaren antingen provisionera eller inaktivera sitt CustomIpPrefix eller redigera resursens taggar.

## EXEMPEL

### Exempel 1: Provision the CustomIpPrefix
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

Kommandot ovan startar iledningen av CustomIpPrefix.

### Exempel 2: Inaktivera CustomIpPrefix
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

Kommandot ovan startar ur provisioneringsprocessen för CustomIpPrefix.

### Exempel 3: Uppdateringstaggar för CustomIpPrefix
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

Ovanstående kommando uppdaterar taggarna för CustomIpPrefix.

## PARAMETERS

### -As Ent
Kör cmdleten i bakgrunden

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

### -Commission
Kör cmdleten i bakgrunden

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

### -Avkodning
Kör cmdleten i bakgrunden

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

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
CustomIpPrefix för att ställa in.

```yaml
Type: PSCustomIpPrefix
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Resursnamnet.

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resursgruppens namn.

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Resurs-ID.

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
En hashtabell som representerar resurstaggar.

```yaml
Type: Hashtable
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: SetByInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix

### System.Collections.Hashtable

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzCustomIpPrefix](./Get-AzCustomIpPrefix.md)

[New-AzCustomIpPrefix](./New-AzCustomIpPrefix.md)

[Remove-AzCustomIpPrefix](./Remove-AzCustomIpPrefix.md)
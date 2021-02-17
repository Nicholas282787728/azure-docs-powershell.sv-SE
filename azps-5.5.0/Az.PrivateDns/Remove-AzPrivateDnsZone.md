---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227167"
---
# Remove-AzPrivateDnsZone

## SYNOPSIS
Tar bort en privat DNS-zon från en resursgrupp.

## SYNTAX

### Fält (standard)
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekt
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Remove-AzPrivateDnsZone** tar bort en privat DNS-zon (Domain Name System) permanent från en angiven resursgrupp.
Alla postuppsättningar i zonen tas också bort.
Du kan skicka ett **PrivateDnsZone-objekt** med parametern *PrivateZone* eller med hjälp av rörledningsoperatorn, eller så kan du ange parametrarna *Name* och *ResourceGroupName.*
Du kan använda parametern Confirm och $ConfirmPreference Windows PowerShell för att styra om cmdleten uppmanar dig att bekräfta.
När du anger zonen med ett **PrivateDnsZone-objekt** (som skickas via pipeline- eller zonparametern) tas zonen inte bort om den har ändrats i Azure DNS sedan det lokala **PrivateDnsZone-objektet** hämtades (endast åtgärder direkt i DNS-zonresursräkningen som ändringar, åtgärder för postuppsättningar i zonen påverkas inte). 
Det ger skydd för samtidiga zonändringar.
Detta kan ignoreras med *parametern Overwrite,* som tar bort zonen oavsett samtidiga ändringar.

## EXEMPEL

### Exempel 1: Ta bort en privat zon
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Med det här kommandot tas zonen myzone.com från resursgruppen MyResourceGroup.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

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

### -Name
Anger namnet på den privata DNS-zonen som cmdleten tar bort.
Du måste också ange *parametern ResourceGroupName.*
Du kan också ange DNS-zonen med hjälp av *zonparametern.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
När du anger zonen med ett **PrivateDnsZone-objekt** (som skickas via pipeline- eller zonparametern) tas zonen inte bort om den har ändrats i Azure DNS sedan det lokala **PrivateDnsZone-objektet** hämtades (endast åtgärder direkt i DNS-zonresursräkningen som ändringar, åtgärder för postuppsättningar i zonen påverkas inte). 
Det här ger skydd för samtidiga zonändringar.
Detta kan ignoreras med *parametern Overwrite,* som tar bort zonen oavsett samtidiga ändringar.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Används för att skicka resultatet (boolesk) för åtgärden ta bort den privata zonen längre ned i pipelinen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateZone
Det privata zonobjektet som ska tas bort.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resursgruppen som innehåller zonen som ska tas bort.
Du måste också ange *zonename-parametern.*
Du kan också ange DNS-zonen med ett **PrivateDnsZone-objekt** som skickas via antingen pipelinen eller *zone-parametern.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Private DNS Zone ResourceID.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone

### System.String

## UTDATA

### System.Boolean

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzPrivateDnsZone](./Get-AzPrivateDnsZone.md)

[New-AzPrivateDnsZone](./New-AzPrivateDnsZone.md)

[Set-AzPrivateDnsZone](./Set-AzPrivateDnsZone.md)

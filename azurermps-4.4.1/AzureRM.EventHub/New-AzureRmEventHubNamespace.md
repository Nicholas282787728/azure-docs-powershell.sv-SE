---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 07b5de12e042c81bb5f27c844d1fc8962453310a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758084"
---
# New-AzureRmEventHubNamespace

## Sammanfattning
Skapar ett namn område för Event Hub.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### NamespaceParameterSet (standard)
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### AutoInflateParameterSet
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-EnableAutoInflate]
 [-MaximumThroughputUnits] <Int32> [-WhatIf] [-Confirm]
```

## PROBLEMBESKRIVNING
New-AzureRmEventHubNamespace-cmdleten skapar ett nytt namn område av typen Event Hub.

## BESKRIVS

### Exempel 1
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation 
```

Skapar en namnrymd för händelse nav \` MyNamespaceName \` på min plats med geografisk plats \` \` i MyResourceGroupName för resurs \` grupp \` .

### Exempel 2
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

Skapar namn områdes \` MyNamespaceName för Event Hub \` på den angivna geografiska platsen min \` plats \` , i resurs grupp \` MyResourceGroupName \` och automittre är aktiverat med MaximumThroughputUnits 10.

## MALLPARAMETRAR

### -Plats
Namn område för händelse nav Geo-Location.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs grupps namn.

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

### -SkuCapacity
Data flödes enheter för Event Hub.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuName
Namn på SKU-namn.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tagg
Hashtables som representerar resurs koder.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoInflate
Anger om autoöka-funktionen är aktive rad

```yaml
Type: SwitchParameter
Parameter Sets: NamespaceParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumThroughputUnits
Övre gräns för flödes enheter när automittre är aktiverat ska Vaule vara inom 0 till 20 data flödes enheter.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Namn område för EventHub.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## KOSTNADS

### System. String
System. Nullable \` 1 \[ \[ system. Int32, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = B77a5c561934e089 \] \] system. Nullable \` 1 \[ \[ system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089 \] \] system. Collections. hash

## VÄRDEN

### Microsoft. Azure. commands. EventHub. Models. NamespaceAttributes

## ANMÄRKNINGAR

## RELATERADE LÄNKAR


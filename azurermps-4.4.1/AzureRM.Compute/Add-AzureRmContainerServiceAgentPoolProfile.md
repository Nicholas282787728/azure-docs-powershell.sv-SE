---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: a5ce087e8ebf768b63d09a4002c3aaf38ddd9f84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585792"
---
# Add-AzureRmContainerServiceAgentPoolProfile

## Sammanfattning
Lägger till en cacheprofil för en behållar tjänst.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmContainerServiceAgentPoolProfile** lägger till en programpool för behållar tjänst till ett objekt för lokal behållar tjänst.

## BESKRIVS

### Exempel 1: lägga till en profil
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

Det här kommandot lägger till en behållare för en programpool i det lokala behållarobjekts tjänstens objekt.

## MALLPARAMETRAR

### -ContainerService
Anger det behållar tjänst objekt som denna cmdlet lägger till en cacheprofil för.
För att få ett **ContainerService** -objekt, Använd cmdleten [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) .

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Antal
Anger antalet agenter som är värd för behållarna.
De acceptabla värdena för den här parametern är: heltal från 1 till 100.
Standardvärdet är 1.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsPrefix
Anger det DNS-prefix som denna cmdlet använder för att skapa det fullständigt kvalificerade domän namnet för den här poolen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på mediepoolen.
Det här värdet måste vara unikt i kontexten för abonnemanget och resurs gruppen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSize
Anger storleken på de virtuella datorerna för agenterna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md)

[Remove-AzureRmContainerServiceAgentPoolProfile](./Remove-AzureRmContainerServiceAgentPoolProfile.md)

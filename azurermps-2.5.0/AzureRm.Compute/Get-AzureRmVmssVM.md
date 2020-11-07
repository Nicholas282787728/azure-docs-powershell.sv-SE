---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvm
schema: 2.0.0
ms.openlocfilehash: bac1bf365ff1135366f2612bfbe5ba313e2300b8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931498"
---
# Get-AzureRmVmssVM

## Sammanfattning
Hämtar egenskaperna för en VMSS-virtuell dator.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### DefaultParameter (standard)
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmVmssVM** hämtar modellen vy och instans för en virtuell dator med skalnings uppsättning (virtuell dator).
Model-vyn är de användardefinierade egenskaperna för den virtuella datorn.
Instans visningen är den virtuella datorns status för förekomst nivå.
Ange en *status* parameter för att få en instans av en virtuell dator.

## BESKRIVS

### Exempel 1: Hämta egenskaper för en VMSS virtuell dator
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Det här kommandot får egenskaperna för den virtuella dator datorn som heter VMSS001 som tillhör resurs gruppen VMSS.
Eftersom kommandot inte anger parameter för *InstanceView* , får cmdleten modellen för den virtuella datorn.

### Exempel 2: Hämta modell visnings egenskaperna för en VMSS-virtuell dator
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

Det här kommandot får egenskaperna för den virtuella dator datorn som heter VMSS004 som tillhör resurs gruppen VMSS.
Kommandot hämtar det instans-ID som lagras i variabeln $ID vars modell vy ska visas.

### Exempel 3: Hämta instans Visa egenskaper för en VMSS-virtuell dator
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

Det här kommandot får egenskaperna för den virtuella dator datorn som heter VMSS004 som tillhör resurs gruppen VMSS.
Eftersom kommandot *InstanceView* parameter anges i cmdlet hämtas instans visningen av den virtuella datorn.
Med kommandot hämtas instans-ID som lagras i variabeln $ID som instans-vyn ska hämtas för.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
Anger det instans-ID som modell läget ska visas för.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceView
Anger att denna cmdlet endast får till gång till den virtuella datorns instans.

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resurs gruppen för VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Arter namnet på VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Denna cmdlet genererar inga utdata.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Set-AzureRmVmssVM](./Set-AzureRmVmssVM.md)

[Get-AzureRmVmss](./Get-AzureRmVmss.md)



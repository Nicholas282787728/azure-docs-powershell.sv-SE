---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 2f33b0dbee4f584553eac1047471adef08e3523b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925214"
---
# Get-AzVM

## Sammanfattning
Hämtar egenskaperna för en virtuell dator.

## FRÅGESYNTAXEN

### ListAllVirtualMachinesParamSet (standard)
```
Get-AzVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListVirtualMachineInResourceGroupParamSet
```
Get-AzVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetVirtualMachineInResourceGroupParamSet
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListNextLinkVirtualMachinesParamSet
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzVM** hämtar vyn modell och instans för en virtuell Azure-dator.
Model-vyn är de användardefinierade egenskaperna för den virtuella datorn.
Instans visningen är den virtuella datorns status för förekomst nivå.
Ange en *status* parameter för att få en instans av en virtuell dator.

## BESKRIVS

### Exempel 1: Hämta egenskaper för modell och instans
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

Det här kommandot hämtar egenskaperna för vyn modell och vyn för den virtuella datorn med namnet VirtualMachine07.

### Exempel 2: Hämta egenskaper för instans
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

Det här kommandot får egenskaper för den virtuella datorn som heter VirtualMachine07.
Det här kommandot anger *status* -parametern.
Därför får kommandot bara till förekomst egenskaperna för vyn.

### Exempel 3: Hämta egenskaper för alla virtuella datorer i en resurs grupp
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"
```

Det här kommandot får egenskaper för alla virtuella datorer i resurs gruppen som heter ResourceGroup11.

### Exempel 4: Hämta alla virtuella datorer i ditt abonnemang
```
PS C:\> Get-AzVM
```

Det här kommandot får alla virtuella datorer i ditt abonnemang.

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

### -DisplayHint
Bestämmer hur det virtuella datorobjektet visas.

Giltiga värden är:

--Kompakt: visar endast de högsta nivå egenskaperna

--Expand: visar alla egenskaper på alla nivåer
```yaml
Type: DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: 
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på den virtuella dator som ska visas.

```yaml
Type: String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
Anger nästa länk.

```yaml
Type: Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en resurs grupp.

```yaml
Type: String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Anger att denna cmdlet endast får till gång till den virtuella datorns instans.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. Compute. Models. PSVirtualMachine

### Microsoft. Azure. commands. Compute. Models. PSVirtualMachineInstanceView

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzVM](./New-AzVM.md)

[Remove-AzVM](./Remove-AzVM.md)

[Restart-AzVM](./Restart-AzVM.md)

[Start-AzVM](./Start-AzVM.md)

[Stopp-AzVM](./Stop-AzVM.md)

[Update-AzVM](./Update-AzVM.md)



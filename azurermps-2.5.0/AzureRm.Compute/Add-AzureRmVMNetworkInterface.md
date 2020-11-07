---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 112403f4cb742c5df39538eb2d8d8fac629d3379
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930754"
---
# Add-AzureRmVMNetworkInterface

## Sammanfattning
Lägger till ett nätverks gränssnitt till en virtuell dator.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### GetNicFromNicId (standard)
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetNicFromNicObject
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmVMNetworkInterface** lägger till ett nätverks gränssnitt till en virtuell dator.
Du kan lägga till ett gränssnitt när du skapar en virtuell dator eller lägger till en på en befintlig virtuell dator.

## BESKRIVS

### Exempel 1: lägga till ett nätverks gränssnitt till en ny virtuell dator
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

Det första kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.
Kommandot tilldelar den virtuella datorn ett namn och en storlek.

Det andra kommandot lägger till ett nätverks gränssnitt till den virtuella datorn som lagras i $VirtualMachine.

### Exempel 2: lägga till ett nätverks gränssnitt till en befintlig virtuell dator
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten **Get-AzureRmVM** .
Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.

Det andra kommandot lägger till ett nätverks gränssnitt till den virtuella datorn som lagras i $VirtualMachine.

Det sista kommandot uppdaterar tillståndet för den virtuella datorn som lagras i $VirtualMachine i ResourceGroup11.

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

### -ID
Anger ID för ett nätverks gränssnitt att lägga till på en virtuell dator.
Du kan använda cmdleten [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) för att få ett nätverks gränssnitt.

```yaml
Type: String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkInterface
Anger nätverks gränssnitt.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Primär
Anger att nätverks gränssnittet läggs till i det primära gränssnittet.

```yaml
Type: SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Anger ett lokalt virtuellt dator objekt där du kan lägga till ett nätverks gränssnitt.
Använd cmdleten **New-AzureRmVMConfig** för att skapa en virtuell dator.
Använd cmdleten **Get-AzureRmVM** för att få en befintlig virtuell dator.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. Network. Models. PSNetworkInterface]
Parametern ' NetworkInterface ' godkänner värdet för typen system. Collections. Generic. list ' 1 [Microsoft. Azure. commands. Network. Models. PSNetworkInterface] ' från pipeline

### PSVirtualMachine
Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline

## VÄRDEN

### Microsoft. Azure. commands. Compute. Models. PSVirtualMachine

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRmVMConfig](./New-AzureRmVMConfig.md)

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Get-AzureRmAvailabilitySet](./Get-AzureRmAvailabilitySet.md)

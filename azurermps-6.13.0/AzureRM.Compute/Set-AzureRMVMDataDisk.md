---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 4ed0abb355bf7a755e5acaa36f8bb11e88d80c5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755856"
---
# Set-AzureRmVMDataDisk

## Sammanfattning
Ändrar egenskaper för en data disk för en virtuell dator.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ChangeWithName
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ChangeWithLun
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmVMDataDisk** ändrar egenskaper för en virtuell dator data disk.

## BESKRIVS

### Exempel 1: ändra cacheläge för en data disk
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

Det första kommandot får den virtuella datorn med namnet ContosoVM07 med hjälp av **Get-AzureRmVM**.
Kommandot sparar det i $VM variabel.
Det andra kommandot ändrar cacheläge för data disken med namnet DataDisk01 på den virtuella datorn i $VM.
Kommandot skickar resultatet till Update-AzureRmVM cmdlet som implementerar dina ändringar.
En ändring av likviditets läget gör att den virtuella datorn startas om.

## MALLPARAMETRAR

### -Cachning
Anger diskens cacheläge.
De acceptabla värdena för den här parametern är:
- ReadOnly
- ReadWrite standardvärdet är ReadWrite.
Om du ändrar det här värdet startas den virtuella datorn om.
Den här inställningen påverkar diskens konsekvens och prestanda.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

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

### -DiskSizeInGB
Anger storleken i GB för data disken.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LUN
Anger LUN (Logical Unit Number) för data disken som denna cmdlet ändrar.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ChangeWithLun
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på data disken som denna cmdlet ändrar.

```yaml
Type: System.String
Parameter Sets: ChangeWithName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Den virtuella datorns kontotyp.

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

### -VM
Anger den virtuella dator för vilken denna cmdlet ändrar en data disk.
Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Anger om WriteAccelerator ska aktive ras eller inaktive ras på data disken.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. Compute. Models. PSVirtualMachine

### System. String

### System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, version = 21.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

## VÄRDEN

### Microsoft. Azure. commands. Compute. Models. PSVirtualMachine

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Update-AzureRmVM](./Update-AzureRmVM.md)



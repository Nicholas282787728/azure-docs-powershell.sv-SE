---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: 60d525cc50b62350853755ae46698cbecb358654
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573651"
---
# Set-AzureRmVmssStorageProfile

## Sammanfattning
Anger lagrings profil egenskaper för VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-ManagedDisk <StorageAccountTypes>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmVmssStorageProfile** anger lagrings profil egenskaperna för den virtuella datorns skal uppsättning (VMSS).

## BESKRIVS

### Exempel 1: Ange lagrings profil egenskaper för VMSS
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

Det här kommandot anger lagrings profil egenskaperna för VMSS med namnet ContosoVMSS.

## MALLPARAMETRAR

### -DataDisk
Anger data diskens objekt.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Image
Anger BLOB URI för användar avbildningen.
VMSS skapar en operativ Systems disk i samma behållare som användar bilden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageReferenceId
Anger bild referens-ID.

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

### -ImageReferenceOffer
Anger typen av virtuell dator avbildning (VMImage).
För att få ett bild utbud, Använd cmdleten Get-AzureRmVMImageOffer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageReferencePublisher
Anger namnet på en utgivare av en VMImage.
Använd Get-AzureRmVMImagePublisher cmdlet för att få en utgivare.

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

### -ImageReferenceSku
Anger VMImage-SKU.
För att få SKU: er, Använd Get-AzureRmVMImageSku cmdlet.

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

### -ImageReferenceVersion
Anger versionen för VMImage.
För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.

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

### -ManagedDisk
Anger den hanterade disken.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsDiskCaching
Anger operativ system diskens cacheläge. De acceptabla värdena för den här parametern är:

- ReadOnly
- Läs

Standardvärdet är ReadWrite.
Om du ändrar värdet för cachelagring startas den virtuella datorn om.

Den här inställningen påverkar diskens konsekvens och prestanda.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsDiskCreateOption
Anger hur den här cmdleten skapar de VMSS virtuella datorerna.

De acceptabla värdena för den här parametern är:

- Bifoga: det här värdet används när du använder en specialiserad disk för att skapa den VMSS virtuella datorn. 
- FromImage: det här värdet används när du använder en bild för att skapa den virtuella VMSS-datorn.
Om du använder en plattforms bild kan du även använda parametern *imageReference* .

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsDiskName
Anger namnet på operativ system disken.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsDiskOsType
Anger operativ systemet på disken.
Detta krävs endast för användar bild scenarier och inte för en plattforms bild.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdContainer
Anger de URL-adresser som används för att lagra operativ system diskar för VMSS.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Anger VMSS-objektet.
Använd New-AzureRmVmssConfig-objektet för att få ett objekt.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

###  
Denna cmdlet genererar inga utdata.

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmVMImageOffer](./Get-AzureRmVMImageOffer.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md)



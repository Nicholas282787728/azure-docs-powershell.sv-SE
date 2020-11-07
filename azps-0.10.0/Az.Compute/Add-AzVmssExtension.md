---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 97c8824bca395ddd8fb23ebb4750ab35931c5d51
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925290"
---
# <span data-ttu-id="a172c-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a172c-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="a172c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a172c-102">SYNOPSIS</span></span>
<span data-ttu-id="a172c-103">Lägger till en anknytning till VMSS.</span><span class="sxs-lookup"><span data-stu-id="a172c-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="a172c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a172c-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a172c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a172c-105">DESCRIPTION</span></span>
<span data-ttu-id="a172c-106">Cmdleten **Add-AzVmssExtension** lägger till ett tillägg i den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a172c-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a172c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a172c-107">EXAMPLES</span></span>

### <span data-ttu-id="a172c-108">Exempel 1: lägga till ett tillägg i VMSS</span><span class="sxs-lookup"><span data-stu-id="a172c-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="a172c-109">Det här kommandot lägger till en anknytning till VMMS.</span><span class="sxs-lookup"><span data-stu-id="a172c-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="a172c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a172c-110">PARAMETERS</span></span>

### <span data-ttu-id="a172c-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a172c-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a172c-112">Anger om tilläggs versionen ska uppdateras automatiskt till en nyare del version.</span><span class="sxs-lookup"><span data-stu-id="a172c-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a172c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a172c-113">-DefaultProfile</span></span>
<span data-ttu-id="a172c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a172c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a172c-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="a172c-115">-ForceUpdateTag</span></span>
<span data-ttu-id="a172c-116">Om ett värde anges och skiljer sig från det tidigare värdet tvingas förlängnings hanteraren att uppdateras även om tilläggs konfigurationen inte har ändrats.</span><span class="sxs-lookup"><span data-stu-id="a172c-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a172c-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a172c-117">-Name</span></span>
<span data-ttu-id="a172c-118">Anger namnet på tillägget som läggs till i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a172c-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="a172c-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="a172c-119">-ProtectedSetting</span></span>
<span data-ttu-id="a172c-120">Anger privat konfiguration för tillägget som en sträng.</span><span class="sxs-lookup"><span data-stu-id="a172c-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="a172c-121">Denna cmdlet krypterar den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="a172c-121">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a172c-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a172c-122">-Publisher</span></span>
<span data-ttu-id="a172c-123">Anger namnet på tilläggs utgivaren.</span><span class="sxs-lookup"><span data-stu-id="a172c-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="a172c-124">Utgivaren får ett namn när utgivaren registrerar ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="a172c-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="a172c-125">Detta kan använda cmdleten [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) för att hämta utgivaren.</span><span class="sxs-lookup"><span data-stu-id="a172c-125">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a172c-126">-Ställ in</span><span class="sxs-lookup"><span data-stu-id="a172c-126">-Setting</span></span>
<span data-ttu-id="a172c-127">Anger den offentliga konfigurationen som en sträng för tillägget.</span><span class="sxs-lookup"><span data-stu-id="a172c-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="a172c-128">Denna cmdlet krypterar inte offentlig konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a172c-128">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a172c-129">– Skriv</span><span class="sxs-lookup"><span data-stu-id="a172c-129">-Type</span></span>
<span data-ttu-id="a172c-130">Anger fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="a172c-130">Specifies the extension type.</span></span>
<span data-ttu-id="a172c-131">Du kan använda cmdleten [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) för att få fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="a172c-131">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="a172c-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a172c-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="a172c-133">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="a172c-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="a172c-134">Du kan använda cmdleten [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) för att få versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="a172c-134">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a172c-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a172c-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a172c-136">Ange VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="a172c-136">Specify the VMSS object.</span></span>
<span data-ttu-id="a172c-137">Du kan använda den [nya-AzVmssConfig](./New-AzVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="a172c-137">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a172c-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a172c-138">-Confirm</span></span>
<span data-ttu-id="a172c-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a172c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a172c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a172c-140">-WhatIf</span></span>
<span data-ttu-id="a172c-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a172c-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a172c-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a172c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a172c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a172c-143">CommonParameters</span></span>
<span data-ttu-id="a172c-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a172c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a172c-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a172c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a172c-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a172c-146">INPUTS</span></span>

### <span data-ttu-id="a172c-147">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a172c-147">VirtualMachineScaleSet</span></span>
<span data-ttu-id="a172c-148">Parametern ' VirtualMachineScaleSet ' godkänner värdet av typen ' VirtualMachineScaleSet ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a172c-148">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="a172c-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a172c-149">OUTPUTS</span></span>

###  
<span data-ttu-id="a172c-150">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a172c-150">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a172c-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a172c-151">NOTES</span></span>

## <span data-ttu-id="a172c-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a172c-152">RELATED LINKS</span></span>

[<span data-ttu-id="a172c-153">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a172c-153">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="a172c-154">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a172c-154">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="a172c-155">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="a172c-155">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="a172c-156">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="a172c-156">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="a172c-157">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a172c-157">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

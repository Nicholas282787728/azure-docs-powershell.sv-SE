---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: 20446fc7c93000b29680689001d9e3c40c4862e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573550"
---
# <span data-ttu-id="998a0-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="998a0-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="998a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="998a0-102">SYNOPSIS</span></span>
<span data-ttu-id="998a0-103">Lägger till en anknytning till VMSS.</span><span class="sxs-lookup"><span data-stu-id="998a0-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="998a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="998a0-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="998a0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="998a0-105">DESCRIPTION</span></span>
<span data-ttu-id="998a0-106">Cmdleten **Add-AzureRmVmssExtension** lägger till ett tillägg i den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="998a0-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="998a0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="998a0-107">EXAMPLES</span></span>

### <span data-ttu-id="998a0-108">Exempel 1: lägga till ett tillägg i VMSS</span><span class="sxs-lookup"><span data-stu-id="998a0-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="998a0-109">Det här kommandot lägger till en anknytning till VMMS.</span><span class="sxs-lookup"><span data-stu-id="998a0-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="998a0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="998a0-110">PARAMETERS</span></span>

### <span data-ttu-id="998a0-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="998a0-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="998a0-112">Anger om tilläggs versionen ska uppdateras automatiskt till en nyare del version.</span><span class="sxs-lookup"><span data-stu-id="998a0-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="998a0-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="998a0-113">-Name</span></span>
<span data-ttu-id="998a0-114">Anger namnet på tillägget som läggs till i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="998a0-114">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="998a0-115">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="998a0-115">-ProtectedSetting</span></span>
<span data-ttu-id="998a0-116">Anger privat konfiguration för tillägget som en sträng.</span><span class="sxs-lookup"><span data-stu-id="998a0-116">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="998a0-117">Denna cmdlet krypterar den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="998a0-117">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="998a0-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="998a0-118">-Publisher</span></span>
<span data-ttu-id="998a0-119">Anger namnet på tilläggs utgivaren.</span><span class="sxs-lookup"><span data-stu-id="998a0-119">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="998a0-120">Utgivaren får ett namn när utgivaren registrerar ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="998a0-120">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="998a0-121">Detta kan använda cmdleten [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) för att hämta utgivaren.</span><span class="sxs-lookup"><span data-stu-id="998a0-121">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="998a0-122">-Ställ in</span><span class="sxs-lookup"><span data-stu-id="998a0-122">-Setting</span></span>
<span data-ttu-id="998a0-123">Anger den offentliga konfigurationen som en sträng för tillägget.</span><span class="sxs-lookup"><span data-stu-id="998a0-123">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="998a0-124">Denna cmdlet krypterar inte offentlig konfiguration.</span><span class="sxs-lookup"><span data-stu-id="998a0-124">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="998a0-125">– Skriv</span><span class="sxs-lookup"><span data-stu-id="998a0-125">-Type</span></span>
<span data-ttu-id="998a0-126">Anger fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="998a0-126">Specifies the extension type.</span></span>
<span data-ttu-id="998a0-127">Du kan använda cmdleten [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) för att få fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="998a0-127">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="998a0-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="998a0-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="998a0-129">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="998a0-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="998a0-130">Du kan använda cmdleten [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) för att få versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="998a0-130">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="998a0-131">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="998a0-131">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="998a0-132">Ange VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="998a0-132">Specify the VMSS object.</span></span>
<span data-ttu-id="998a0-133">Du kan använda den [nya-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="998a0-133">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="998a0-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="998a0-134">-Confirm</span></span>
<span data-ttu-id="998a0-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="998a0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="998a0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="998a0-136">-WhatIf</span></span>
<span data-ttu-id="998a0-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="998a0-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="998a0-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="998a0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="998a0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="998a0-139">CommonParameters</span></span>
<span data-ttu-id="998a0-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="998a0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="998a0-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="998a0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="998a0-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="998a0-142">INPUTS</span></span>

### <span data-ttu-id="998a0-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="998a0-143">None</span></span>
<span data-ttu-id="998a0-144">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="998a0-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="998a0-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="998a0-145">OUTPUTS</span></span>

###  
<span data-ttu-id="998a0-146">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="998a0-146">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="998a0-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="998a0-147">NOTES</span></span>

## <span data-ttu-id="998a0-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="998a0-148">RELATED LINKS</span></span>

[<span data-ttu-id="998a0-149">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="998a0-149">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="998a0-150">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="998a0-150">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="998a0-151">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="998a0-151">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="998a0-152">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="998a0-152">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="998a0-153">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="998a0-153">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)

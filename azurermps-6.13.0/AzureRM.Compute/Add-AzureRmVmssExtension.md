---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: ad87e4e556263889de23640abad391ee28d7b397
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580820"
---
# <span data-ttu-id="0453f-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="0453f-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="0453f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0453f-102">SYNOPSIS</span></span>
<span data-ttu-id="0453f-103">Lägger till en anknytning till VMSS.</span><span class="sxs-lookup"><span data-stu-id="0453f-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0453f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0453f-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0453f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0453f-105">DESCRIPTION</span></span>
<span data-ttu-id="0453f-106">Cmdleten **Add-AzureRmVmssExtension** lägger till ett tillägg i den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="0453f-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="0453f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0453f-107">EXAMPLES</span></span>

### <span data-ttu-id="0453f-108">Exempel 1: lägga till ett tillägg i VMSS</span><span class="sxs-lookup"><span data-stu-id="0453f-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="0453f-109">Det här kommandot lägger till en anknytning till VMSS.</span><span class="sxs-lookup"><span data-stu-id="0453f-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="0453f-110">Exempel 2: lägga till en anknytning till VMSS med inställningar och skyddade inställningar</span><span class="sxs-lookup"><span data-stu-id="0453f-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="0453f-111">Det här kommandot lägger till ett tillägg till VMSS med ett exempel bash-skript på en blob-lagring, och anger URL-adressen för Blob Storage och Executable i inställningar och säkerhets åtkomst i skyddade inställningar.</span><span class="sxs-lookup"><span data-stu-id="0453f-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="0453f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0453f-112">PARAMETERS</span></span>

### <span data-ttu-id="0453f-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0453f-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="0453f-114">Anger om tilläggs versionen ska uppdateras automatiskt till en nyare del version.</span><span class="sxs-lookup"><span data-stu-id="0453f-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0453f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0453f-115">-DefaultProfile</span></span>
<span data-ttu-id="0453f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0453f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0453f-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="0453f-117">-ForceUpdateTag</span></span>
<span data-ttu-id="0453f-118">Om ett värde anges och skiljer sig från det tidigare värdet tvingas förlängnings hanteraren att uppdateras även om tilläggs konfigurationen inte har ändrats.</span><span class="sxs-lookup"><span data-stu-id="0453f-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="0453f-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="0453f-119">-Name</span></span>
<span data-ttu-id="0453f-120">Anger namnet på tillägget som läggs till i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0453f-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="0453f-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="0453f-121">-ProtectedSetting</span></span>
<span data-ttu-id="0453f-122">Anger privat konfiguration för tillägget som en sträng.</span><span class="sxs-lookup"><span data-stu-id="0453f-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="0453f-123">Denna cmdlet krypterar den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="0453f-123">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0453f-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="0453f-124">-Publisher</span></span>
<span data-ttu-id="0453f-125">Anger namnet på tilläggs utgivaren.</span><span class="sxs-lookup"><span data-stu-id="0453f-125">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="0453f-126">Utgivaren får ett namn när utgivaren registrerar ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="0453f-126">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="0453f-127">Detta kan använda cmdleten [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) för att hämta utgivaren.</span><span class="sxs-lookup"><span data-stu-id="0453f-127">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="0453f-128">-Ställ in</span><span class="sxs-lookup"><span data-stu-id="0453f-128">-Setting</span></span>
<span data-ttu-id="0453f-129">Anger den offentliga konfigurationen som en sträng för tillägget.</span><span class="sxs-lookup"><span data-stu-id="0453f-129">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="0453f-130">Denna cmdlet krypterar inte offentlig konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0453f-130">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0453f-131">– Skriv</span><span class="sxs-lookup"><span data-stu-id="0453f-131">-Type</span></span>
<span data-ttu-id="0453f-132">Anger fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="0453f-132">Specifies the extension type.</span></span>
<span data-ttu-id="0453f-133">Du kan använda cmdleten [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) för att få fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="0453f-133">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="0453f-134">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="0453f-134">-TypeHandlerVersion</span></span>
<span data-ttu-id="0453f-135">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0453f-135">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="0453f-136">Du kan använda cmdleten [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) för att få versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="0453f-136">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="0453f-137">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0453f-137">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0453f-138">Ange VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="0453f-138">Specify the VMSS object.</span></span>
<span data-ttu-id="0453f-139">Du kan använda den [nya-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="0453f-139">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="0453f-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0453f-140">-Confirm</span></span>
<span data-ttu-id="0453f-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0453f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0453f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0453f-142">-WhatIf</span></span>
<span data-ttu-id="0453f-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0453f-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0453f-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0453f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0453f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0453f-145">CommonParameters</span></span>
<span data-ttu-id="0453f-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0453f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0453f-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0453f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0453f-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0453f-148">INPUTS</span></span>

### <span data-ttu-id="0453f-149">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0453f-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="0453f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="0453f-150">System.String</span></span>

### <span data-ttu-id="0453f-151">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0453f-151">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="0453f-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="0453f-152">System.Object</span></span>

## <span data-ttu-id="0453f-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0453f-153">OUTPUTS</span></span>

### <span data-ttu-id="0453f-154">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0453f-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="0453f-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0453f-155">NOTES</span></span>

## <span data-ttu-id="0453f-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0453f-156">RELATED LINKS</span></span>

[<span data-ttu-id="0453f-157">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="0453f-157">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="0453f-158">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0453f-158">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="0453f-159">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="0453f-159">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="0453f-160">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="0453f-160">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="0453f-161">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0453f-161">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)

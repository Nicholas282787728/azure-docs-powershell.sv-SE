---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 87ea9af1980948f28477a9f483b3c6429df98d12
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260618"
---
# <span data-ttu-id="7ce93-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="7ce93-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="7ce93-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ce93-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce93-103">Lägger till en anknytning till VMSS.</span><span class="sxs-lookup"><span data-stu-id="7ce93-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="7ce93-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ce93-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ce93-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ce93-105">DESCRIPTION</span></span>
<span data-ttu-id="7ce93-106">Cmdleten **Add-AzVmssExtension** lägger till ett tillägg i den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="7ce93-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="7ce93-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ce93-107">EXAMPLES</span></span>

### <span data-ttu-id="7ce93-108">Exempel 1: lägga till ett tillägg i VMSS</span><span class="sxs-lookup"><span data-stu-id="7ce93-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="7ce93-109">Det här kommandot lägger till en anknytning till VMSS.</span><span class="sxs-lookup"><span data-stu-id="7ce93-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="7ce93-110">Exempel 2: lägga till en anknytning till VMSS med inställningar och skyddade inställningar</span><span class="sxs-lookup"><span data-stu-id="7ce93-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="7ce93-111">Det här kommandot lägger till ett tillägg till VMSS med ett exempel bash-skript på en blob-lagring, och anger URL-adressen för Blob Storage och Executable i inställningar och säkerhets åtkomst i skyddade inställningar.</span><span class="sxs-lookup"><span data-stu-id="7ce93-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="7ce93-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ce93-112">PARAMETERS</span></span>

### <span data-ttu-id="7ce93-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7ce93-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="7ce93-114">Anger om tilläggs versionen ska uppdateras automatiskt till en nyare del version.</span><span class="sxs-lookup"><span data-stu-id="7ce93-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="7ce93-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ce93-115">-DefaultProfile</span></span>
<span data-ttu-id="7ce93-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ce93-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce93-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="7ce93-117">-ForceUpdateTag</span></span>
<span data-ttu-id="7ce93-118">Om ett värde anges och skiljer sig från det tidigare värdet tvingas förlängnings hanteraren att uppdateras även om tilläggs konfigurationen inte har ändrats.</span><span class="sxs-lookup"><span data-stu-id="7ce93-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="7ce93-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ce93-119">-Name</span></span>
<span data-ttu-id="7ce93-120">Anger namnet på tillägget som läggs till i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ce93-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="7ce93-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="7ce93-121">-ProtectedSetting</span></span>
<span data-ttu-id="7ce93-122">Anger privat konfiguration för tillägget som en sträng.</span><span class="sxs-lookup"><span data-stu-id="7ce93-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="7ce93-123">Denna cmdlet krypterar den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="7ce93-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="7ce93-124">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="7ce93-124">-ProvisionAfterExtension</span></span>
<span data-ttu-id="7ce93-125">Samling med tilläggs namn efter vilka tillägget måste etableras.</span><span class="sxs-lookup"><span data-stu-id="7ce93-125">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ce93-126">-Publisher</span><span class="sxs-lookup"><span data-stu-id="7ce93-126">-Publisher</span></span>
<span data-ttu-id="7ce93-127">Anger namnet på tilläggs utgivaren.</span><span class="sxs-lookup"><span data-stu-id="7ce93-127">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="7ce93-128">Utgivaren får ett namn när utgivaren registrerar ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="7ce93-128">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="7ce93-129">Detta kan använda cmdleten [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) för att hämta utgivaren.</span><span class="sxs-lookup"><span data-stu-id="7ce93-129">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="7ce93-130">-Ställ in</span><span class="sxs-lookup"><span data-stu-id="7ce93-130">-Setting</span></span>
<span data-ttu-id="7ce93-131">Anger den offentliga konfigurationen som en sträng för tillägget.</span><span class="sxs-lookup"><span data-stu-id="7ce93-131">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="7ce93-132">Denna cmdlet krypterar inte offentlig konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7ce93-132">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="7ce93-133">– Skriv</span><span class="sxs-lookup"><span data-stu-id="7ce93-133">-Type</span></span>
<span data-ttu-id="7ce93-134">Anger fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="7ce93-134">Specifies the extension type.</span></span>
<span data-ttu-id="7ce93-135">Du kan använda cmdleten [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) för att få fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="7ce93-135">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="7ce93-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7ce93-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="7ce93-137">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7ce93-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="7ce93-138">Du kan använda cmdleten [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) för att få versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="7ce93-138">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="7ce93-139">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7ce93-139">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7ce93-140">Ange VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="7ce93-140">Specify the VMSS object.</span></span>
<span data-ttu-id="7ce93-141">Du kan använda den [nya-AzVmssConfig](./New-AzVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="7ce93-141">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="7ce93-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ce93-142">-Confirm</span></span>
<span data-ttu-id="7ce93-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ce93-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ce93-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ce93-144">-WhatIf</span></span>
<span data-ttu-id="7ce93-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7ce93-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ce93-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7ce93-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ce93-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce93-147">CommonParameters</span></span>
<span data-ttu-id="7ce93-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ce93-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce93-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ce93-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce93-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ce93-150">INPUTS</span></span>

### <span data-ttu-id="7ce93-151">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7ce93-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="7ce93-152">System. String</span><span class="sxs-lookup"><span data-stu-id="7ce93-152">System.String</span></span>

### <span data-ttu-id="7ce93-153">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7ce93-153">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7ce93-154">System. Object</span><span class="sxs-lookup"><span data-stu-id="7ce93-154">System.Object</span></span>

## <span data-ttu-id="7ce93-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ce93-155">OUTPUTS</span></span>

### <span data-ttu-id="7ce93-156">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7ce93-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7ce93-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ce93-157">NOTES</span></span>

## <span data-ttu-id="7ce93-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ce93-158">RELATED LINKS</span></span>

[<span data-ttu-id="7ce93-159">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="7ce93-159">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="7ce93-160">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7ce93-160">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="7ce93-161">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="7ce93-161">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="7ce93-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="7ce93-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="7ce93-163">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7ce93-163">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

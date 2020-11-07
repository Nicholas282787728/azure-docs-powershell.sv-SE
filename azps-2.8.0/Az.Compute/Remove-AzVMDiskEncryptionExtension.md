---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 084775812a887e0cc6fe497a0e0cef46ec464956
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745018"
---
# <span data-ttu-id="f7eff-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f7eff-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="f7eff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7eff-102">SYNOPSIS</span></span>
<span data-ttu-id="f7eff-103">Tar bort disk krypterings tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f7eff-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="f7eff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7eff-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7eff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7eff-105">DESCRIPTION</span></span>
<span data-ttu-id="f7eff-106">Cmdleten **Remove-AzVMDiskEncryptionExtension** tar bort disk krypterings tillägget och tillhör ande tilläggs konfiguration från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f7eff-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="f7eff-107">Om inget tilläggs namn anges tar denna cmdlet bort tillägget med standard namnet AzureDiskEncryption för virtuella datorer som kör operativ systemet Windows eller AzureDiskEncryptionForLinux för Linux-baserade virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="f7eff-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="f7eff-108">Denna cmdlet fungerar inte om kryptering på den virtuella datorn inte har inaktiverats.</span><span class="sxs-lookup"><span data-stu-id="f7eff-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="f7eff-109">Använd [disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md)om du vill inaktivera kryptering på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f7eff-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="f7eff-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7eff-110">EXAMPLES</span></span>

### <span data-ttu-id="f7eff-111">Exempel 1: ta bort disk krypterings tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f7eff-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="f7eff-112">Det här kommandot tar bort tillägget med standard namnet AzureDiskEncryption för en virtuell dator som kör operativ systemet Windows eller AzureDiskEncryptionForLinux för Linux-baserad virtuell dator med namnet MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="f7eff-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="f7eff-113">Exempel 2: ta bort ett disk krypterings tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f7eff-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="f7eff-114">Det här kommandot tar bort krypterings tillägget med namnet MyDiskEncryptionExtension från den virtuella datorn med namnet MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="f7eff-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="f7eff-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7eff-115">PARAMETERS</span></span>

### <span data-ttu-id="f7eff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7eff-116">-DefaultProfile</span></span>
<span data-ttu-id="f7eff-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f7eff-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7eff-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f7eff-118">-Force</span></span>
<span data-ttu-id="f7eff-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f7eff-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f7eff-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f7eff-120">-Name</span></span>
<span data-ttu-id="f7eff-121">Anger namnet på Azure Resource Manager-resursen som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="f7eff-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="f7eff-122">Den Set-AzVMDiskEncryptionExtension cmdleten ställer in det här namnet på AzureDiskEncryption för virtuella datorer som kör operativ systemet Windows och AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="f7eff-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="f7eff-123">Ange endast den här parametern om du har ändrat standard namnet i cmdleten **set-AzVMDiskEncryptionExtension** eller använt ett annat resurs namn i en resurs hanterares mall.</span><span class="sxs-lookup"><span data-stu-id="f7eff-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7eff-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f7eff-124">-NoWait</span></span>
<span data-ttu-id="f7eff-125">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="f7eff-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f7eff-126">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="f7eff-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f7eff-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7eff-127">-ResourceGroupName</span></span>
<span data-ttu-id="f7eff-128">Anger namnet på resurs gruppen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="f7eff-128">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7eff-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="f7eff-129">-VMName</span></span>
<span data-ttu-id="f7eff-130">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="f7eff-130">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7eff-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f7eff-131">-Confirm</span></span>
<span data-ttu-id="f7eff-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f7eff-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7eff-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7eff-133">-WhatIf</span></span>
<span data-ttu-id="f7eff-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f7eff-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7eff-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f7eff-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7eff-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7eff-136">CommonParameters</span></span>
<span data-ttu-id="f7eff-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7eff-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7eff-138">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7eff-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7eff-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7eff-139">INPUTS</span></span>

### <span data-ttu-id="f7eff-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f7eff-140">System.String</span></span>

## <span data-ttu-id="f7eff-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7eff-141">OUTPUTS</span></span>

### <span data-ttu-id="f7eff-142">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f7eff-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f7eff-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7eff-143">NOTES</span></span>

## <span data-ttu-id="f7eff-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7eff-144">RELATED LINKS</span></span>

[<span data-ttu-id="f7eff-145">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="f7eff-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="f7eff-146">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f7eff-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)



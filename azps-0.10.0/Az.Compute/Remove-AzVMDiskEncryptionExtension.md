---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 51b1273e5c44756df56177878dbe4fbc9563ec2a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924953"
---
# <span data-ttu-id="2d276-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="2d276-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="2d276-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d276-102">SYNOPSIS</span></span>
<span data-ttu-id="2d276-103">Tar bort disk krypterings tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2d276-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="2d276-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d276-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d276-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d276-105">DESCRIPTION</span></span>
<span data-ttu-id="2d276-106">Cmdleten **Remove-AzVMDiskEncryptionExtension** tar bort disk krypterings tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2d276-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="2d276-107">Om inget tilläggs namn anges tar denna cmdlet bort tillägget med standard namnet AzureDiskEncryption för virtuella datorer som kör operativ systemet Windows eller AzureDiskEncryptionForLinux för Linux-baserade virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="2d276-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="2d276-108">Denna cmdlet inaktiverar inte kryptering på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2d276-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="2d276-109">Det tar bort tillägget och den associerade tilläggs konfigurationen från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2d276-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="2d276-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d276-110">EXAMPLES</span></span>

### <span data-ttu-id="2d276-111">Exempel 1: ta bort disk krypterings tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2d276-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="2d276-112">Det här kommandot tar bort tillägget med standard namnet AzureDiskEncryption för en virtuell dator som kör operativ systemet Windows eller AzureDiskEncryptionForLinux för Linux-baserad virtuell dator med namnet MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="2d276-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="2d276-113">Exempel 2: ta bort ett disk krypterings tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2d276-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="2d276-114">Det här kommandot tar bort krypterings tillägget med namnet MyDiskEncryptionExtension från den virtuella datorn med namnet MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="2d276-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="2d276-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d276-115">PARAMETERS</span></span>

### <span data-ttu-id="2d276-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d276-116">-DefaultProfile</span></span>
<span data-ttu-id="2d276-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2d276-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d276-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2d276-118">-Force</span></span>
<span data-ttu-id="2d276-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2d276-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d276-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="2d276-120">-Name</span></span>
<span data-ttu-id="2d276-121">Anger namnet på Azure Resource Manager-resursen som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="2d276-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="2d276-122">Den Set-AzVMDiskEncryptionExtension cmdleten ställer in det här namnet på AzureDiskEncryption för virtuella datorer som kör operativ systemet Windows och AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="2d276-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="2d276-123">Ange endast den här parametern om du har ändrat standard namnet i cmdleten **set-AzVMDiskEncryptionExtension** eller använt ett annat resurs namn i en resurs hanterares mall.</span><span class="sxs-lookup"><span data-stu-id="2d276-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d276-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d276-124">-ResourceGroupName</span></span>
<span data-ttu-id="2d276-125">Anger namnet på resurs gruppen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2d276-125">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d276-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="2d276-126">-VMName</span></span>
<span data-ttu-id="2d276-127">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2d276-127">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d276-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2d276-128">-Confirm</span></span>
<span data-ttu-id="2d276-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2d276-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d276-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d276-130">-WhatIf</span></span>
<span data-ttu-id="2d276-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2d276-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2d276-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2d276-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d276-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d276-133">CommonParameters</span></span>
<span data-ttu-id="2d276-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d276-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d276-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d276-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d276-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d276-136">INPUTS</span></span>

### <span data-ttu-id="2d276-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="2d276-137">None</span></span>
<span data-ttu-id="2d276-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2d276-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2d276-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d276-139">OUTPUTS</span></span>

### <span data-ttu-id="2d276-140">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2d276-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2d276-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d276-141">NOTES</span></span>

## <span data-ttu-id="2d276-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d276-142">RELATED LINKS</span></span>

[<span data-ttu-id="2d276-143">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="2d276-143">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="2d276-144">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="2d276-144">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)



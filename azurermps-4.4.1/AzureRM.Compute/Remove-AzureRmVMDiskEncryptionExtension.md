---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: 3fc1424fe2cde9b2137ca6925a8788fa5c8a8139
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755300"
---
# <span data-ttu-id="97f0d-101">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="97f0d-101">Remove-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="97f0d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="97f0d-103">Tar bort disk krypterings tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="97f0d-103">Removes the disk encryption extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97f0d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97f0d-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97f0d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97f0d-105">DESCRIPTION</span></span>
<span data-ttu-id="97f0d-106">Cmdleten **Remove-AzureRmVMDiskEncryptionExtension** tar bort disk krypterings tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="97f0d-106">The **Remove-AzureRmVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="97f0d-107">Om inget tilläggs namn anges tar denna cmdlet bort tillägget med standard namnet AzureDiskEncryption för virtuella datorer som kör operativ systemet Windows eller AzureDiskEncryptionForLinux för Linux-baserade virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="97f0d-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="97f0d-108">Denna cmdlet inaktiverar inte kryptering på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="97f0d-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="97f0d-109">Det tar bort tillägget och den associerade tilläggs konfigurationen från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="97f0d-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="97f0d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97f0d-110">EXAMPLES</span></span>

### <span data-ttu-id="97f0d-111">Exempel 1: ta bort disk krypterings tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="97f0d-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="97f0d-112">Det här kommandot tar bort tillägget med standard namnet AzureDiskEncryption för en virtuell dator som kör operativ systemet Windows eller AzureDiskEncryptionForLinux för Linux-baserad virtuell dator med namnet MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="97f0d-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="97f0d-113">Exempel 2: ta bort ett disk krypterings tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="97f0d-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="97f0d-114">Det här kommandot tar bort krypterings tillägget med namnet MyDiskEncryptionExtension från den virtuella datorn med namnet MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="97f0d-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="97f0d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97f0d-115">PARAMETERS</span></span>

### <span data-ttu-id="97f0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97f0d-116">-DefaultProfile</span></span>
<span data-ttu-id="97f0d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97f0d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97f0d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="97f0d-118">-Force</span></span>
<span data-ttu-id="97f0d-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="97f0d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="97f0d-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="97f0d-120">-Name</span></span>
<span data-ttu-id="97f0d-121">Anger namnet på Azure Resource Manager-resursen som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="97f0d-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="97f0d-122">Den Set-AzureRmVMDiskEncryptionExtension cmdleten ställer in det här namnet på AzureDiskEncryption för virtuella datorer som kör operativ systemet Windows och AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="97f0d-122">The Set-AzureRmVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="97f0d-123">Ange endast den här parametern om du har ändrat standard namnet i cmdleten **set-AzureRmVMDiskEncryptionExtension** eller använt ett annat resurs namn i en resurs hanterares mall.</span><span class="sxs-lookup"><span data-stu-id="97f0d-123">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="97f0d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97f0d-124">-ResourceGroupName</span></span>
<span data-ttu-id="97f0d-125">Anger namnet på resurs gruppen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="97f0d-125">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="97f0d-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="97f0d-126">-VMName</span></span>
<span data-ttu-id="97f0d-127">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="97f0d-127">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="97f0d-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="97f0d-128">-Confirm</span></span>
<span data-ttu-id="97f0d-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97f0d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97f0d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97f0d-130">-WhatIf</span></span>
<span data-ttu-id="97f0d-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="97f0d-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="97f0d-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="97f0d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97f0d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f0d-133">CommonParameters</span></span>
<span data-ttu-id="97f0d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97f0d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f0d-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97f0d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f0d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97f0d-136">INPUTS</span></span>

## <span data-ttu-id="97f0d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97f0d-137">OUTPUTS</span></span>

## <span data-ttu-id="97f0d-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97f0d-138">NOTES</span></span>

## <span data-ttu-id="97f0d-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97f0d-139">RELATED LINKS</span></span>

[<span data-ttu-id="97f0d-140">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="97f0d-140">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="97f0d-141">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="97f0d-141">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: d054cb84ccd4e77ca47caf653c5a3d9322691929
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917297"
---
# <span data-ttu-id="95fd2-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="95fd2-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="95fd2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="95fd2-103">Tar bort en DSC-tilläggsprovider från en virtuell dator i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="95fd2-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="95fd2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95fd2-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95fd2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95fd2-105">DESCRIPTION</span></span>
<span data-ttu-id="95fd2-106">Cmdleten **Remove-AzVMDscExtension** tar bort en fil tilläggs hanterare för önskad tillstånds konfiguration (DSC) från en virtuell dator i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="95fd2-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="95fd2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95fd2-107">EXAMPLES</span></span>

### <span data-ttu-id="95fd2-108">Exempel 1: ta bort ett DSC-tillägg</span><span class="sxs-lookup"><span data-stu-id="95fd2-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="95fd2-109">Det här kommandot tar bort tillägget DSC på den virtuella datorn med namnet VM07.</span><span class="sxs-lookup"><span data-stu-id="95fd2-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="95fd2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95fd2-110">PARAMETERS</span></span>

### <span data-ttu-id="95fd2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95fd2-111">-DefaultProfile</span></span>
<span data-ttu-id="95fd2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95fd2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95fd2-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="95fd2-113">-Name</span></span>
<span data-ttu-id="95fd2-114">Anger namnet på det DSC-tillägg som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="95fd2-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="95fd2-115">Set-AzVMDscExtension cmdlet anger det här namnet till Microsoft. PowerShell. DSC, vilket är det standardvärde som används av **Remove-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="95fd2-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="95fd2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95fd2-116">-ResourceGroupName</span></span>
<span data-ttu-id="95fd2-117">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="95fd2-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="95fd2-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="95fd2-118">-VMName</span></span>
<span data-ttu-id="95fd2-119">Anger namnet på en virtuell dator från vilken denna cmdlet tar bort DSC-tillägget.</span><span class="sxs-lookup"><span data-stu-id="95fd2-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95fd2-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="95fd2-120">-Confirm</span></span>
<span data-ttu-id="95fd2-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="95fd2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95fd2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95fd2-122">-WhatIf</span></span>
<span data-ttu-id="95fd2-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="95fd2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95fd2-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="95fd2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95fd2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95fd2-125">CommonParameters</span></span>
<span data-ttu-id="95fd2-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95fd2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95fd2-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95fd2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95fd2-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95fd2-128">INPUTS</span></span>

### <span data-ttu-id="95fd2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="95fd2-129">System.String</span></span>

## <span data-ttu-id="95fd2-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95fd2-130">OUTPUTS</span></span>

### <span data-ttu-id="95fd2-131">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="95fd2-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="95fd2-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95fd2-132">NOTES</span></span>

## <span data-ttu-id="95fd2-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95fd2-133">RELATED LINKS</span></span>

[<span data-ttu-id="95fd2-134">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="95fd2-134">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="95fd2-135">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="95fd2-135">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)



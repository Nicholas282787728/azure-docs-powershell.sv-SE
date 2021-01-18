---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 13140b5434cdc29754b8041a32f328e0b855fed2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526747"
---
# <span data-ttu-id="6a69f-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6a69f-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="6a69f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a69f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a69f-103">Tar bort en DSC-tilläggsprovider från en virtuell dator i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6a69f-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="6a69f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a69f-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a69f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a69f-105">DESCRIPTION</span></span>
<span data-ttu-id="6a69f-106">Cmdleten **Remove-AzVMDscExtension** tar bort en fil tilläggs hanterare för önskad tillstånds konfiguration (DSC) från en virtuell dator i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6a69f-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="6a69f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a69f-107">EXAMPLES</span></span>

### <span data-ttu-id="6a69f-108">Exempel 1: ta bort ett DSC-tillägg</span><span class="sxs-lookup"><span data-stu-id="6a69f-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="6a69f-109">Det här kommandot tar bort tillägget DSC på den virtuella datorn med namnet VM07.</span><span class="sxs-lookup"><span data-stu-id="6a69f-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="6a69f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a69f-110">PARAMETERS</span></span>

### <span data-ttu-id="6a69f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a69f-111">-DefaultProfile</span></span>
<span data-ttu-id="6a69f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6a69f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a69f-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="6a69f-113">-Name</span></span>
<span data-ttu-id="6a69f-114">Anger namnet på det DSC-tillägg som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="6a69f-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="6a69f-115">Set-AzVMDscExtension cmdlet anger det här namnet till Microsoft. PowerShell. DSC, vilket är det standardvärde som används av **Remove-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="6a69f-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="6a69f-116">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6a69f-116">-NoWait</span></span>
<span data-ttu-id="6a69f-117">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="6a69f-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="6a69f-118">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="6a69f-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="6a69f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a69f-119">-ResourceGroupName</span></span>
<span data-ttu-id="6a69f-120">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6a69f-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6a69f-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="6a69f-121">-VMName</span></span>
<span data-ttu-id="6a69f-122">Anger namnet på en virtuell dator från vilken denna cmdlet tar bort DSC-tillägget.</span><span class="sxs-lookup"><span data-stu-id="6a69f-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="6a69f-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6a69f-123">-Confirm</span></span>
<span data-ttu-id="6a69f-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6a69f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a69f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a69f-125">-WhatIf</span></span>
<span data-ttu-id="6a69f-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6a69f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a69f-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6a69f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a69f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a69f-128">CommonParameters</span></span>
<span data-ttu-id="6a69f-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a69f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a69f-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a69f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a69f-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a69f-131">INPUTS</span></span>

### <span data-ttu-id="6a69f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6a69f-132">System.String</span></span>

## <span data-ttu-id="6a69f-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a69f-133">OUTPUTS</span></span>

### <span data-ttu-id="6a69f-134">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6a69f-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6a69f-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a69f-135">NOTES</span></span>

## <span data-ttu-id="6a69f-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a69f-136">RELATED LINKS</span></span>

[<span data-ttu-id="6a69f-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6a69f-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="6a69f-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6a69f-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)



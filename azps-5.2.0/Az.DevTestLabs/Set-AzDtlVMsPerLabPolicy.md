---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 3e06b4f1236863e208a167024e9d0562dc82ca89
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390522"
---
# <span data-ttu-id="a5c80-101">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="a5c80-101">Set-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="a5c80-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5c80-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c80-103">Ställer in de virtuella datorerna per labb policy för en laboratorie i DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="a5c80-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="a5c80-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5c80-104">SYNTAX</span></span>

### <span data-ttu-id="a5c80-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="a5c80-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c80-106">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="a5c80-106">Disable</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5c80-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5c80-107">DESCRIPTION</span></span>
<span data-ttu-id="a5c80-108">Cmdleten **set-AzDtlVMsPerLabPolicy** anger de virtuella datorerna per Lab-princip för en labb lista som anger totalt antal virtuella datorer som är tillåtna i ett labb.</span><span class="sxs-lookup"><span data-stu-id="a5c80-108">The **Set-AzDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="a5c80-109">Cmdleten använder den angivna resurs gruppen och namnet på laboratoriet för att ange principen.</span><span class="sxs-lookup"><span data-stu-id="a5c80-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="a5c80-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5c80-110">EXAMPLES</span></span>

## <span data-ttu-id="a5c80-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5c80-111">PARAMETERS</span></span>

### <span data-ttu-id="a5c80-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c80-112">-DefaultProfile</span></span>
<span data-ttu-id="a5c80-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a5c80-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5c80-114">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="a5c80-114">-Disable</span></span>
<span data-ttu-id="a5c80-115">Anger att denna cmdlet inaktiverar policyn för labbet.</span><span class="sxs-lookup"><span data-stu-id="a5c80-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c80-116">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="a5c80-116">-Enable</span></span>
<span data-ttu-id="a5c80-117">Anger att denna cmdlet aktiverar policyn för labbet.</span><span class="sxs-lookup"><span data-stu-id="a5c80-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c80-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="a5c80-118">-LabName</span></span>
<span data-ttu-id="a5c80-119">Anger namnet på den laboratorie som den här cmdleten ställer in de virtuella datorerna per Lab-princip för.</span><span class="sxs-lookup"><span data-stu-id="a5c80-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="a5c80-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="a5c80-120">-MaxVMs</span></span>
<span data-ttu-id="a5c80-121">Anger maximalt antal virtuella datorer som kan skapas i laboratorium.</span><span class="sxs-lookup"><span data-stu-id="a5c80-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c80-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c80-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5c80-123">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="a5c80-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="a5c80-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5c80-124">-Confirm</span></span>
<span data-ttu-id="a5c80-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5c80-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5c80-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c80-126">-WhatIf</span></span>
<span data-ttu-id="a5c80-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5c80-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5c80-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5c80-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5c80-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c80-129">CommonParameters</span></span>
<span data-ttu-id="a5c80-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5c80-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c80-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5c80-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c80-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5c80-132">INPUTS</span></span>

### <span data-ttu-id="a5c80-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a5c80-133">System.String</span></span>

## <span data-ttu-id="a5c80-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5c80-134">OUTPUTS</span></span>

### <span data-ttu-id="a5c80-135">Microsoft. Azure. commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="a5c80-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="a5c80-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5c80-136">NOTES</span></span>

## <span data-ttu-id="a5c80-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5c80-137">RELATED LINKS</span></span>

[<span data-ttu-id="a5c80-138">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="a5c80-138">Get-AzDtlVMsPerLabPolicy</span></span>](./Get-AzDtlVMsPerLabPolicy.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: bcf15e36ae428277293c174df6b7a3cd55c36252
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917342"
---
# <span data-ttu-id="f2ecd-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f2ecd-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="f2ecd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ecd-103">Tar bort en tillgänglighets uppsättning från Azure.</span><span class="sxs-lookup"><span data-stu-id="f2ecd-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="f2ecd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2ecd-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2ecd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2ecd-105">DESCRIPTION</span></span>
<span data-ttu-id="f2ecd-106">Cmdleten **Remove-AzAvailabilitySet** tar bort en tillgänglighets uppsättning från Azure.</span><span class="sxs-lookup"><span data-stu-id="f2ecd-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="f2ecd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2ecd-107">EXAMPLES</span></span>

### <span data-ttu-id="f2ecd-108">Exempel 1: ta bort en tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="f2ecd-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f2ecd-109">Det här kommandot tar bort en tillgänglighets uppsättning med namnet AvailablitySet03 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f2ecd-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="f2ecd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2ecd-110">PARAMETERS</span></span>

### <span data-ttu-id="f2ecd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2ecd-111">-AsJob</span></span>
<span data-ttu-id="f2ecd-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="f2ecd-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f2ecd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ecd-113">-DefaultProfile</span></span>
<span data-ttu-id="f2ecd-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2ecd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2ecd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f2ecd-115">-Force</span></span>
<span data-ttu-id="f2ecd-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f2ecd-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2ecd-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2ecd-117">-Name</span></span>
<span data-ttu-id="f2ecd-118">Namnet på tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="f2ecd-118">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2ecd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2ecd-119">-ResourceGroupName</span></span>
<span data-ttu-id="f2ecd-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f2ecd-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f2ecd-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f2ecd-121">-Confirm</span></span>
<span data-ttu-id="f2ecd-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f2ecd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2ecd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2ecd-123">-WhatIf</span></span>
<span data-ttu-id="f2ecd-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f2ecd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2ecd-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f2ecd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2ecd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ecd-126">CommonParameters</span></span>
<span data-ttu-id="f2ecd-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2ecd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ecd-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2ecd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ecd-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2ecd-129">INPUTS</span></span>

### <span data-ttu-id="f2ecd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f2ecd-130">System.String</span></span>

## <span data-ttu-id="f2ecd-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2ecd-131">OUTPUTS</span></span>

### <span data-ttu-id="f2ecd-132">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f2ecd-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f2ecd-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2ecd-133">NOTES</span></span>

## <span data-ttu-id="f2ecd-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2ecd-134">RELATED LINKS</span></span>

[<span data-ttu-id="f2ecd-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f2ecd-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="f2ecd-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f2ecd-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)



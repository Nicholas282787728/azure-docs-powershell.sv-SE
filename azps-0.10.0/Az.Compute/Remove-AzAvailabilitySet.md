---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 5a2a8157e69c1b50cc066bb24e8261c1748a6323
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925014"
---
# <span data-ttu-id="09c4c-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="09c4c-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="09c4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="09c4c-103">Tar bort en tillgänglighets uppsättning från Azure.</span><span class="sxs-lookup"><span data-stu-id="09c4c-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="09c4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09c4c-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09c4c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09c4c-105">DESCRIPTION</span></span>
<span data-ttu-id="09c4c-106">Cmdleten **Remove-AzAvailabilitySet** tar bort en tillgänglighets uppsättning från Azure.</span><span class="sxs-lookup"><span data-stu-id="09c4c-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="09c4c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09c4c-107">EXAMPLES</span></span>

### <span data-ttu-id="09c4c-108">Exempel 1: ta bort en tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="09c4c-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="09c4c-109">Det här kommandot tar bort en tillgänglighets uppsättning med namnet AvailablitySet03 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="09c4c-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="09c4c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09c4c-110">PARAMETERS</span></span>

### <span data-ttu-id="09c4c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09c4c-111">-AsJob</span></span>
<span data-ttu-id="09c4c-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="09c4c-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="09c4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c4c-113">-DefaultProfile</span></span>
<span data-ttu-id="09c4c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09c4c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09c4c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="09c4c-115">-Force</span></span>
<span data-ttu-id="09c4c-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="09c4c-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09c4c-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="09c4c-117">-Name</span></span>
<span data-ttu-id="09c4c-118">Namnet på tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="09c4c-118">The availability set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c4c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09c4c-119">-ResourceGroupName</span></span>
<span data-ttu-id="09c4c-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="09c4c-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="09c4c-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09c4c-121">-Confirm</span></span>
<span data-ttu-id="09c4c-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09c4c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09c4c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09c4c-123">-WhatIf</span></span>
<span data-ttu-id="09c4c-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="09c4c-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="09c4c-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="09c4c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09c4c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c4c-126">CommonParameters</span></span>
<span data-ttu-id="09c4c-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09c4c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c4c-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09c4c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c4c-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09c4c-129">INPUTS</span></span>

### <span data-ttu-id="09c4c-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="09c4c-130">None</span></span>
<span data-ttu-id="09c4c-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="09c4c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09c4c-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09c4c-132">OUTPUTS</span></span>

### <span data-ttu-id="09c4c-133">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="09c4c-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="09c4c-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09c4c-134">NOTES</span></span>

## <span data-ttu-id="09c4c-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09c4c-135">RELATED LINKS</span></span>

[<span data-ttu-id="09c4c-136">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="09c4c-136">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="09c4c-137">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="09c4c-137">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)



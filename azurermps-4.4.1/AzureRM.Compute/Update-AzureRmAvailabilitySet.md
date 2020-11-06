---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: c7b33e3f2afd013b6fd54f6d425c0aa1d0d08bd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585712"
---
# <span data-ttu-id="e5756-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e5756-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="e5756-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5756-102">SYNOPSIS</span></span>
<span data-ttu-id="e5756-103">Uppdaterar en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e5756-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5756-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5756-104">SYNTAX</span></span>

### <span data-ttu-id="e5756-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5756-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5756-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="e5756-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5756-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5756-107">DESCRIPTION</span></span>
<span data-ttu-id="e5756-108">Cmdleten **Update-AzureRmAvailabilitySet** uppdaterar en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e5756-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="e5756-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5756-109">EXAMPLES</span></span>

### <span data-ttu-id="e5756-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e5756-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="e5756-111">Det här kommandot uppdaterar tillgänglighets uppsättningen med namnet "AvSet01" i resurs gruppen med namnet "ResourceGroup01" till en hanterad tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e5756-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="e5756-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5756-112">PARAMETERS</span></span>

### <span data-ttu-id="e5756-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e5756-113">-AvailabilitySet</span></span>
<span data-ttu-id="e5756-114">Anger det tillgänglighets objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="e5756-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5756-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5756-115">-DefaultProfile</span></span>
<span data-ttu-id="e5756-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5756-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5756-117">-Hanteras</span><span class="sxs-lookup"><span data-stu-id="e5756-117">-Managed</span></span>
<span data-ttu-id="e5756-118">Hanterad tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="e5756-118">Managed Availability Set</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5756-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="e5756-119">-Sku</span></span>
<span data-ttu-id="e5756-120">Namnet på SKU</span><span class="sxs-lookup"><span data-stu-id="e5756-120">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5756-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e5756-121">-Confirm</span></span>
<span data-ttu-id="e5756-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e5756-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5756-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5756-123">-WhatIf</span></span>
<span data-ttu-id="e5756-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e5756-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5756-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e5756-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5756-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5756-126">CommonParameters</span></span>
<span data-ttu-id="e5756-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5756-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5756-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5756-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5756-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5756-129">INPUTS</span></span>

### <span data-ttu-id="e5756-130">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e5756-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="e5756-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5756-131">OUTPUTS</span></span>

### <span data-ttu-id="e5756-132">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e5756-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="e5756-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5756-133">NOTES</span></span>

## <span data-ttu-id="e5756-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5756-134">RELATED LINKS</span></span>


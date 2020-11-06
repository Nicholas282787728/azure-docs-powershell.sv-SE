---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 3e28cacc8dc6a27f20a93beb3e48ddcc0d0697cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580243"
---
# <span data-ttu-id="73f96-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="73f96-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="73f96-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73f96-102">SYNOPSIS</span></span>
<span data-ttu-id="73f96-103">Uppdaterar en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="73f96-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73f96-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73f96-104">SYNTAX</span></span>

### <span data-ttu-id="73f96-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="73f96-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73f96-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="73f96-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73f96-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73f96-107">DESCRIPTION</span></span>
<span data-ttu-id="73f96-108">Cmdleten **Update-AzureRmAvailabilitySet** uppdaterar en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="73f96-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="73f96-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73f96-109">EXAMPLES</span></span>

### <span data-ttu-id="73f96-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="73f96-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="73f96-111">Det här kommandot uppdaterar tillgänglighets uppsättningen med namnet "AvSet01" i resurs gruppen med namnet "ResourceGroup01" till en hanterad tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="73f96-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="73f96-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73f96-112">PARAMETERS</span></span>

### <span data-ttu-id="73f96-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73f96-113">-AsJob</span></span>
<span data-ttu-id="73f96-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="73f96-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="73f96-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="73f96-115">-AvailabilitySet</span></span>
<span data-ttu-id="73f96-116">Anger det tillgänglighets objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="73f96-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="73f96-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f96-117">-DefaultProfile</span></span>
<span data-ttu-id="73f96-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73f96-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73f96-119">-Hanteras</span><span class="sxs-lookup"><span data-stu-id="73f96-119">-Managed</span></span>
<span data-ttu-id="73f96-120">Hanterad tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="73f96-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="73f96-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="73f96-121">-Sku</span></span>
<span data-ttu-id="73f96-122">Namnet på SKU</span><span class="sxs-lookup"><span data-stu-id="73f96-122">The Name of Sku</span></span>

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

### <span data-ttu-id="73f96-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="73f96-123">-Tag</span></span>
<span data-ttu-id="73f96-124">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="73f96-124">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f96-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="73f96-125">-Confirm</span></span>
<span data-ttu-id="73f96-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="73f96-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73f96-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73f96-127">-WhatIf</span></span>
<span data-ttu-id="73f96-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="73f96-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73f96-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="73f96-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73f96-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f96-130">CommonParameters</span></span>
<span data-ttu-id="73f96-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73f96-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f96-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73f96-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f96-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73f96-133">INPUTS</span></span>

### <span data-ttu-id="73f96-134">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="73f96-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="73f96-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73f96-135">OUTPUTS</span></span>

### <span data-ttu-id="73f96-136">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="73f96-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="73f96-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73f96-137">NOTES</span></span>

## <span data-ttu-id="73f96-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73f96-138">RELATED LINKS</span></span>

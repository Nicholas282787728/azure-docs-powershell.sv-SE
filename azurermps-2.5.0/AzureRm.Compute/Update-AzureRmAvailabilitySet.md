---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: f7d9181b5ec79434928fc8d291025aea9480b8e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931454"
---
# <span data-ttu-id="03100-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="03100-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="03100-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03100-102">SYNOPSIS</span></span>
<span data-ttu-id="03100-103">Uppdaterar en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="03100-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03100-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03100-104">SYNTAX</span></span>

### <span data-ttu-id="03100-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="03100-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03100-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="03100-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03100-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03100-107">DESCRIPTION</span></span>
<span data-ttu-id="03100-108">Cmdleten **Update-AzureRmAvailabilitySet** uppdaterar en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="03100-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="03100-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03100-109">EXAMPLES</span></span>

### <span data-ttu-id="03100-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="03100-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="03100-111">Det här kommandot uppdaterar tillgänglighets uppsättningen med namnet "AvSet01" i resurs gruppen med namnet "ResourceGroup01" till en hanterad tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="03100-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="03100-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03100-112">PARAMETERS</span></span>

### <span data-ttu-id="03100-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03100-113">-AsJob</span></span>
<span data-ttu-id="03100-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="03100-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="03100-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="03100-115">-AvailabilitySet</span></span>
<span data-ttu-id="03100-116">Anger det tillgänglighets objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="03100-116">Specifies the availability set object to be updated.</span></span>

```yaml
Type: PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03100-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03100-117">-DefaultProfile</span></span>
<span data-ttu-id="03100-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03100-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03100-119">-Hanteras</span><span class="sxs-lookup"><span data-stu-id="03100-119">-Managed</span></span>
<span data-ttu-id="03100-120">Hanterad tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="03100-120">Managed Availability Set</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03100-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="03100-121">-Sku</span></span>
<span data-ttu-id="03100-122">Namnet på SKU</span><span class="sxs-lookup"><span data-stu-id="03100-122">The Name of Sku</span></span>

```yaml
Type: String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03100-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="03100-123">-Confirm</span></span>
<span data-ttu-id="03100-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="03100-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03100-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03100-125">-WhatIf</span></span>
<span data-ttu-id="03100-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="03100-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03100-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="03100-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03100-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03100-128">CommonParameters</span></span>
<span data-ttu-id="03100-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03100-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03100-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03100-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03100-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03100-131">INPUTS</span></span>

### <span data-ttu-id="03100-132">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="03100-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="03100-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03100-133">OUTPUTS</span></span>

### <span data-ttu-id="03100-134">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="03100-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="03100-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03100-135">NOTES</span></span>

## <span data-ttu-id="03100-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03100-136">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: e8bd36cd9c054d155dca034f49be8cd422a244bc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923022"
---
# <span data-ttu-id="313e3-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="313e3-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="313e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="313e3-102">SYNOPSIS</span></span>
<span data-ttu-id="313e3-103">Uppdaterar en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="313e3-103">Updates an availability set.</span></span>

## <span data-ttu-id="313e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="313e3-104">SYNTAX</span></span>

### <span data-ttu-id="313e3-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="313e3-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="313e3-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="313e3-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="313e3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="313e3-107">DESCRIPTION</span></span>
<span data-ttu-id="313e3-108">Cmdleten **Update-AzAvailabilitySet** uppdaterar en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="313e3-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="313e3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="313e3-109">EXAMPLES</span></span>

### <span data-ttu-id="313e3-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="313e3-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="313e3-111">Det här kommandot uppdaterar tillgänglighets uppsättningen med namnet "AvSet01" i resurs gruppen med namnet "ResourceGroup01" till en hanterad tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="313e3-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="313e3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="313e3-112">PARAMETERS</span></span>

### <span data-ttu-id="313e3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="313e3-113">-AsJob</span></span>
<span data-ttu-id="313e3-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="313e3-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="313e3-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="313e3-115">-AvailabilitySet</span></span>
<span data-ttu-id="313e3-116">Anger det tillgänglighets objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="313e3-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="313e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313e3-117">-DefaultProfile</span></span>
<span data-ttu-id="313e3-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="313e3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="313e3-119">-Hanteras</span><span class="sxs-lookup"><span data-stu-id="313e3-119">-Managed</span></span>
<span data-ttu-id="313e3-120">Hanterad tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="313e3-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="313e3-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="313e3-121">-Sku</span></span>
<span data-ttu-id="313e3-122">Namnet på SKU</span><span class="sxs-lookup"><span data-stu-id="313e3-122">The Name of Sku</span></span>

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

### <span data-ttu-id="313e3-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="313e3-123">-Confirm</span></span>
<span data-ttu-id="313e3-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="313e3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="313e3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="313e3-125">-WhatIf</span></span>
<span data-ttu-id="313e3-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="313e3-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="313e3-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="313e3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="313e3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313e3-128">CommonParameters</span></span>
<span data-ttu-id="313e3-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="313e3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313e3-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="313e3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313e3-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="313e3-131">INPUTS</span></span>

### <span data-ttu-id="313e3-132">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="313e3-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="313e3-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="313e3-133">OUTPUTS</span></span>

### <span data-ttu-id="313e3-134">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="313e3-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="313e3-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="313e3-135">NOTES</span></span>

## <span data-ttu-id="313e3-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="313e3-136">RELATED LINKS</span></span>


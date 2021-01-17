---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: faadb14259dd397f713480c771d2d450260d99cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390264"
---
# <span data-ttu-id="e3f23-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="e3f23-101">New-AzHpcCache</span></span>

## <span data-ttu-id="e3f23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3f23-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f23-103">Skapar ett HPC-cacheminne.</span><span class="sxs-lookup"><span data-stu-id="e3f23-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="e3f23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3f23-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3f23-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3f23-105">DESCRIPTION</span></span>
<span data-ttu-id="e3f23-106">Cmdleten **New-AzHpcCache** skapar en Azure HPC-cache.</span><span class="sxs-lookup"><span data-stu-id="e3f23-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="e3f23-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3f23-107">EXAMPLES</span></span>

### <span data-ttu-id="e3f23-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e3f23-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="e3f23-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3f23-109">PARAMETERS</span></span>

### <span data-ttu-id="e3f23-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3f23-110">-AsJob</span></span>
<span data-ttu-id="e3f23-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e3f23-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3f23-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="e3f23-112">-CacheSize</span></span>
<span data-ttu-id="e3f23-113">CacheSize.</span><span class="sxs-lookup"><span data-stu-id="e3f23-113">CacheSize.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f23-114">-DefaultProfile</span></span>
<span data-ttu-id="e3f23-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3f23-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3f23-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="e3f23-116">-Location</span></span>
<span data-ttu-id="e3f23-117">Plats.</span><span class="sxs-lookup"><span data-stu-id="e3f23-117">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f23-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3f23-118">-Name</span></span>
<span data-ttu-id="e3f23-119">Cacheminnets namn.</span><span class="sxs-lookup"><span data-stu-id="e3f23-119">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f23-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3f23-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3f23-121">Namnet på den resurs grupp som du vill skapa cache under.</span><span class="sxs-lookup"><span data-stu-id="e3f23-121">Name of resource group under which you want to create cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f23-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="e3f23-122">-Sku</span></span>
<span data-ttu-id="e3f23-123">N.</span><span class="sxs-lookup"><span data-stu-id="e3f23-123">Sku.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f23-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="e3f23-124">-SubnetUri</span></span>
<span data-ttu-id="e3f23-125">SubnetURI.</span><span class="sxs-lookup"><span data-stu-id="e3f23-125">SubnetURI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f23-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e3f23-126">-Tag</span></span>
<span data-ttu-id="e3f23-127">De taggar som ska associeras med HPC-cache.</span><span class="sxs-lookup"><span data-stu-id="e3f23-127">The tags to associate with HPC Cache.</span></span>

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

### <span data-ttu-id="e3f23-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3f23-128">-Confirm</span></span>
<span data-ttu-id="e3f23-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e3f23-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3f23-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3f23-130">-WhatIf</span></span>
<span data-ttu-id="e3f23-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e3f23-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3f23-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e3f23-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3f23-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f23-133">CommonParameters</span></span>
<span data-ttu-id="e3f23-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3f23-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f23-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3f23-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f23-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3f23-136">INPUTS</span></span>

### <span data-ttu-id="e3f23-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e3f23-137">System.String</span></span>

### <span data-ttu-id="e3f23-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e3f23-138">System.Int32</span></span>

## <span data-ttu-id="e3f23-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3f23-139">OUTPUTS</span></span>

### <span data-ttu-id="e3f23-140">Microsoft. Azure. PowerShell. cmdletar. HPCCache. Models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="e3f23-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="e3f23-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3f23-141">NOTES</span></span>

## <span data-ttu-id="e3f23-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3f23-142">RELATED LINKS</span></span>

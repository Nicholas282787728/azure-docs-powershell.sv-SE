---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 22813d762fe575f7f34b6c8eb81f1b5c1c167047
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409403"
---
# <span data-ttu-id="0d230-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="0d230-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="0d230-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d230-102">SYNOPSIS</span></span>
<span data-ttu-id="0d230-103">Stoppar HPC-cache.</span><span class="sxs-lookup"><span data-stu-id="0d230-103">Stops HPC cache.</span></span>

## <span data-ttu-id="0d230-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d230-104">SYNTAX</span></span>

### <span data-ttu-id="0d230-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0d230-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d230-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d230-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d230-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d230-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d230-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d230-108">DESCRIPTION</span></span>
<span data-ttu-id="0d230-109">Cmdleten **Stop-AzHpcCache** stoppar en Azure HPC-cache.</span><span class="sxs-lookup"><span data-stu-id="0d230-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="0d230-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d230-110">EXAMPLES</span></span>

### <span data-ttu-id="0d230-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0d230-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="0d230-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d230-112">PARAMETERS</span></span>

### <span data-ttu-id="0d230-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d230-113">-DefaultProfile</span></span>
<span data-ttu-id="0d230-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d230-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d230-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0d230-115">-Force</span></span>
<span data-ttu-id="0d230-116">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="0d230-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="0d230-117">Denna cmdlet uppmanar dig som standard att bekräfta att du vill stoppa cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="0d230-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="0d230-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d230-118">-InputObject</span></span>
<span data-ttu-id="0d230-119">Cacheobjektet att stoppa.</span><span class="sxs-lookup"><span data-stu-id="0d230-119">The cache object to stop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d230-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="0d230-120">-Name</span></span>
<span data-ttu-id="0d230-121">Cacheminnets namn.</span><span class="sxs-lookup"><span data-stu-id="0d230-121">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d230-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d230-122">-PassThru</span></span>
<span data-ttu-id="0d230-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="0d230-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0d230-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0d230-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d230-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d230-125">-ResourceGroupName</span></span>
<span data-ttu-id="0d230-126">Namnet på den resurs grupp under vilket du vill stoppa cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="0d230-126">Name of resource group under which you want to stop cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d230-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d230-127">-ResourceId</span></span>
<span data-ttu-id="0d230-128">Resurs-ID för cacheminnet</span><span class="sxs-lookup"><span data-stu-id="0d230-128">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d230-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0d230-129">-Confirm</span></span>
<span data-ttu-id="0d230-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0d230-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d230-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d230-131">-WhatIf</span></span>
<span data-ttu-id="0d230-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0d230-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d230-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0d230-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d230-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d230-134">CommonParameters</span></span>
<span data-ttu-id="0d230-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d230-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d230-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d230-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d230-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d230-137">INPUTS</span></span>

### <span data-ttu-id="0d230-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0d230-138">System.String</span></span>

## <span data-ttu-id="0d230-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d230-139">OUTPUTS</span></span>

## <span data-ttu-id="0d230-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d230-140">NOTES</span></span>

## <span data-ttu-id="0d230-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d230-141">RELATED LINKS</span></span>

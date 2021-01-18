---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 22813d762fe575f7f34b6c8eb81f1b5c1c167047
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522608"
---
# <span data-ttu-id="16baf-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="16baf-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="16baf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16baf-102">SYNOPSIS</span></span>
<span data-ttu-id="16baf-103">Stoppar HPC-cache.</span><span class="sxs-lookup"><span data-stu-id="16baf-103">Stops HPC cache.</span></span>

## <span data-ttu-id="16baf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16baf-104">SYNTAX</span></span>

### <span data-ttu-id="16baf-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="16baf-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16baf-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16baf-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16baf-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16baf-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16baf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16baf-108">DESCRIPTION</span></span>
<span data-ttu-id="16baf-109">Cmdleten **Stop-AzHpcCache** stoppar en Azure HPC-cache.</span><span class="sxs-lookup"><span data-stu-id="16baf-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="16baf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16baf-110">EXAMPLES</span></span>

### <span data-ttu-id="16baf-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="16baf-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="16baf-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16baf-112">PARAMETERS</span></span>

### <span data-ttu-id="16baf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16baf-113">-DefaultProfile</span></span>
<span data-ttu-id="16baf-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16baf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16baf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="16baf-115">-Force</span></span>
<span data-ttu-id="16baf-116">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="16baf-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="16baf-117">Denna cmdlet uppmanar dig som standard att bekräfta att du vill stoppa cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="16baf-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="16baf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16baf-118">-InputObject</span></span>
<span data-ttu-id="16baf-119">Cacheobjektet att stoppa.</span><span class="sxs-lookup"><span data-stu-id="16baf-119">The cache object to stop.</span></span>

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

### <span data-ttu-id="16baf-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="16baf-120">-Name</span></span>
<span data-ttu-id="16baf-121">Cacheminnets namn.</span><span class="sxs-lookup"><span data-stu-id="16baf-121">Name of cache.</span></span>

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

### <span data-ttu-id="16baf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16baf-122">-PassThru</span></span>
<span data-ttu-id="16baf-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="16baf-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="16baf-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="16baf-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="16baf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16baf-125">-ResourceGroupName</span></span>
<span data-ttu-id="16baf-126">Namnet på den resurs grupp under vilket du vill stoppa cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="16baf-126">Name of resource group under which you want to stop cache.</span></span>

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

### <span data-ttu-id="16baf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16baf-127">-ResourceId</span></span>
<span data-ttu-id="16baf-128">Resurs-ID för cacheminnet</span><span class="sxs-lookup"><span data-stu-id="16baf-128">The resource id of the Cache</span></span>

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

### <span data-ttu-id="16baf-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="16baf-129">-Confirm</span></span>
<span data-ttu-id="16baf-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="16baf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16baf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16baf-131">-WhatIf</span></span>
<span data-ttu-id="16baf-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="16baf-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16baf-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="16baf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16baf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16baf-134">CommonParameters</span></span>
<span data-ttu-id="16baf-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16baf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16baf-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16baf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16baf-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16baf-137">INPUTS</span></span>

### <span data-ttu-id="16baf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="16baf-138">System.String</span></span>

## <span data-ttu-id="16baf-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16baf-139">OUTPUTS</span></span>

## <span data-ttu-id="16baf-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16baf-140">NOTES</span></span>

## <span data-ttu-id="16baf-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16baf-141">RELATED LINKS</span></span>

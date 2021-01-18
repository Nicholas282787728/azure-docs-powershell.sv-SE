---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520567"
---
# <span data-ttu-id="b2f63-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="b2f63-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="b2f63-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2f63-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f63-103">Startar HPC-cachen.</span><span class="sxs-lookup"><span data-stu-id="b2f63-103">Starts HPC cache.</span></span>

## <span data-ttu-id="b2f63-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2f63-104">SYNTAX</span></span>

### <span data-ttu-id="b2f63-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b2f63-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2f63-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2f63-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2f63-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2f63-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2f63-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2f63-108">DESCRIPTION</span></span>
<span data-ttu-id="b2f63-109">Cmdleten **Start-AzHpcCache** startar en Azure HPC-cache.</span><span class="sxs-lookup"><span data-stu-id="b2f63-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="b2f63-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2f63-110">EXAMPLES</span></span>

### <span data-ttu-id="b2f63-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b2f63-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="b2f63-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2f63-112">PARAMETERS</span></span>

### <span data-ttu-id="b2f63-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2f63-113">-AsJob</span></span>
<span data-ttu-id="b2f63-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b2f63-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2f63-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f63-115">-DefaultProfile</span></span>
<span data-ttu-id="b2f63-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2f63-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2f63-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b2f63-117">-Force</span></span>
<span data-ttu-id="b2f63-118">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="b2f63-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="b2f63-119">Som standard ber denna cmdlet dig att bekräfta att du vill starta cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="b2f63-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="b2f63-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2f63-120">-InputObject</span></span>
<span data-ttu-id="b2f63-121">Cacheobjektet att starta.</span><span class="sxs-lookup"><span data-stu-id="b2f63-121">The cache object to start.</span></span>

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

### <span data-ttu-id="b2f63-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2f63-122">-Name</span></span>
<span data-ttu-id="b2f63-123">Cacheminnets namn.</span><span class="sxs-lookup"><span data-stu-id="b2f63-123">Name of cache.</span></span>

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

### <span data-ttu-id="b2f63-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2f63-124">-PassThru</span></span>
<span data-ttu-id="b2f63-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="b2f63-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b2f63-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b2f63-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b2f63-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2f63-127">-ResourceGroupName</span></span>
<span data-ttu-id="b2f63-128">Namnet på den resurs grupp som du vill starta cache för.</span><span class="sxs-lookup"><span data-stu-id="b2f63-128">Name of resource group under which you want to start cache.</span></span>

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

### <span data-ttu-id="b2f63-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2f63-129">-ResourceId</span></span>
<span data-ttu-id="b2f63-130">Resurs-ID för cacheminnet</span><span class="sxs-lookup"><span data-stu-id="b2f63-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="b2f63-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b2f63-131">-Confirm</span></span>
<span data-ttu-id="b2f63-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b2f63-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2f63-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2f63-133">-WhatIf</span></span>
<span data-ttu-id="b2f63-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b2f63-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2f63-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b2f63-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2f63-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f63-136">CommonParameters</span></span>
<span data-ttu-id="b2f63-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2f63-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f63-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2f63-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f63-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2f63-139">INPUTS</span></span>

### <span data-ttu-id="b2f63-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b2f63-140">System.String</span></span>

## <span data-ttu-id="b2f63-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2f63-141">OUTPUTS</span></span>

## <span data-ttu-id="b2f63-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2f63-142">NOTES</span></span>

## <span data-ttu-id="b2f63-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2f63-143">RELATED LINKS</span></span>

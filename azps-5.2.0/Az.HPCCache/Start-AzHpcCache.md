---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416691"
---
# <span data-ttu-id="1bef6-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="1bef6-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="1bef6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1bef6-102">SYNOPSIS</span></span>
<span data-ttu-id="1bef6-103">Startar HPC-cachen.</span><span class="sxs-lookup"><span data-stu-id="1bef6-103">Starts HPC cache.</span></span>

## <span data-ttu-id="1bef6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1bef6-104">SYNTAX</span></span>

### <span data-ttu-id="1bef6-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1bef6-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bef6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bef6-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bef6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bef6-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bef6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1bef6-108">DESCRIPTION</span></span>
<span data-ttu-id="1bef6-109">Cmdleten **Start-AzHpcCache** startar en Azure HPC-cache.</span><span class="sxs-lookup"><span data-stu-id="1bef6-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="1bef6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1bef6-110">EXAMPLES</span></span>

### <span data-ttu-id="1bef6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1bef6-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="1bef6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1bef6-112">PARAMETERS</span></span>

### <span data-ttu-id="1bef6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bef6-113">-AsJob</span></span>
<span data-ttu-id="1bef6-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1bef6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1bef6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bef6-115">-DefaultProfile</span></span>
<span data-ttu-id="1bef6-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1bef6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bef6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1bef6-117">-Force</span></span>
<span data-ttu-id="1bef6-118">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1bef6-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="1bef6-119">Som standard ber denna cmdlet dig att bekräfta att du vill starta cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="1bef6-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="1bef6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bef6-120">-InputObject</span></span>
<span data-ttu-id="1bef6-121">Cacheobjektet att starta.</span><span class="sxs-lookup"><span data-stu-id="1bef6-121">The cache object to start.</span></span>

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

### <span data-ttu-id="1bef6-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="1bef6-122">-Name</span></span>
<span data-ttu-id="1bef6-123">Cacheminnets namn.</span><span class="sxs-lookup"><span data-stu-id="1bef6-123">Name of cache.</span></span>

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

### <span data-ttu-id="1bef6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bef6-124">-PassThru</span></span>
<span data-ttu-id="1bef6-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="1bef6-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1bef6-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="1bef6-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1bef6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bef6-127">-ResourceGroupName</span></span>
<span data-ttu-id="1bef6-128">Namnet på den resurs grupp som du vill starta cache för.</span><span class="sxs-lookup"><span data-stu-id="1bef6-128">Name of resource group under which you want to start cache.</span></span>

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

### <span data-ttu-id="1bef6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bef6-129">-ResourceId</span></span>
<span data-ttu-id="1bef6-130">Resurs-ID för cacheminnet</span><span class="sxs-lookup"><span data-stu-id="1bef6-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="1bef6-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1bef6-131">-Confirm</span></span>
<span data-ttu-id="1bef6-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1bef6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bef6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bef6-133">-WhatIf</span></span>
<span data-ttu-id="1bef6-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1bef6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bef6-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1bef6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bef6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bef6-136">CommonParameters</span></span>
<span data-ttu-id="1bef6-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bef6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bef6-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1bef6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bef6-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1bef6-139">INPUTS</span></span>

### <span data-ttu-id="1bef6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1bef6-140">System.String</span></span>

## <span data-ttu-id="1bef6-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1bef6-141">OUTPUTS</span></span>

## <span data-ttu-id="1bef6-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1bef6-142">NOTES</span></span>

## <span data-ttu-id="1bef6-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1bef6-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: 8f84323df269d8e0fbd0f60525e54595ef89f3e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392360"
---
# <span data-ttu-id="1faa9-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="1faa9-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="1faa9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1faa9-102">SYNOPSIS</span></span>
<span data-ttu-id="1faa9-103">Uppdaterar en HPC-cache.</span><span class="sxs-lookup"><span data-stu-id="1faa9-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="1faa9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1faa9-104">SYNTAX</span></span>

### <span data-ttu-id="1faa9-105">FlushParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1faa9-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1faa9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1faa9-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1faa9-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="1faa9-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1faa9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1faa9-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1faa9-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1faa9-109">DESCRIPTION</span></span>
<span data-ttu-id="1faa9-110">Cmdleten **Update-AzHpcCache** uppdaterar en Azure HPC-cache.</span><span class="sxs-lookup"><span data-stu-id="1faa9-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="1faa9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1faa9-111">EXAMPLES</span></span>

### <span data-ttu-id="1faa9-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1faa9-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="1faa9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1faa9-113">PARAMETERS</span></span>

### <span data-ttu-id="1faa9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1faa9-114">-AsJob</span></span>
<span data-ttu-id="1faa9-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1faa9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1faa9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1faa9-116">-DefaultProfile</span></span>
<span data-ttu-id="1faa9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1faa9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1faa9-118">-Töm</span><span class="sxs-lookup"><span data-stu-id="1faa9-118">-Flush</span></span>
<span data-ttu-id="1faa9-119">Rensar HPC-cache.</span><span class="sxs-lookup"><span data-stu-id="1faa9-119">Flushes HPC Cache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FlushParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1faa9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1faa9-120">-Force</span></span>
<span data-ttu-id="1faa9-121">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1faa9-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="1faa9-122">Denna cmdlet uppmanar dig som standard att bekräfta att du vill uppdatera cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="1faa9-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="1faa9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1faa9-123">-InputObject</span></span>
<span data-ttu-id="1faa9-124">Cacheobjektet att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="1faa9-124">The cache object to update.</span></span>

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

### <span data-ttu-id="1faa9-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="1faa9-125">-Name</span></span>
<span data-ttu-id="1faa9-126">Cacheminnets namn.</span><span class="sxs-lookup"><span data-stu-id="1faa9-126">Name of cache.</span></span>

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

### <span data-ttu-id="1faa9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1faa9-127">-PassThru</span></span>
<span data-ttu-id="1faa9-128">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="1faa9-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1faa9-129">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="1faa9-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1faa9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1faa9-130">-ResourceGroupName</span></span>
<span data-ttu-id="1faa9-131">Namnet på den resurs grupp som du vill uppdatera cache under.</span><span class="sxs-lookup"><span data-stu-id="1faa9-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="1faa9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1faa9-132">-ResourceId</span></span>
<span data-ttu-id="1faa9-133">Resurs-ID för cacheminnet</span><span class="sxs-lookup"><span data-stu-id="1faa9-133">The resource id of the Cache</span></span>

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

### <span data-ttu-id="1faa9-134">-Uppgradera</span><span class="sxs-lookup"><span data-stu-id="1faa9-134">-Upgrade</span></span>
<span data-ttu-id="1faa9-135">Uppgradera HpcCache.</span><span class="sxs-lookup"><span data-stu-id="1faa9-135">Upgrade HpcCache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpgradeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1faa9-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1faa9-136">-Confirm</span></span>
<span data-ttu-id="1faa9-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1faa9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1faa9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1faa9-138">-WhatIf</span></span>
<span data-ttu-id="1faa9-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1faa9-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1faa9-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1faa9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1faa9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1faa9-141">CommonParameters</span></span>
<span data-ttu-id="1faa9-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1faa9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1faa9-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1faa9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1faa9-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1faa9-144">INPUTS</span></span>

### <span data-ttu-id="1faa9-145">System. String</span><span class="sxs-lookup"><span data-stu-id="1faa9-145">System.String</span></span>

## <span data-ttu-id="1faa9-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1faa9-146">OUTPUTS</span></span>

## <span data-ttu-id="1faa9-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1faa9-147">NOTES</span></span>

## <span data-ttu-id="1faa9-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1faa9-148">RELATED LINKS</span></span>

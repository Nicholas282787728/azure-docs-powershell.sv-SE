---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: fa799a05b76f9f6941b19bf171beb77318b77d39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270622"
---
# <span data-ttu-id="98430-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="98430-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="98430-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98430-102">SYNOPSIS</span></span>
<span data-ttu-id="98430-103">Uppdaterar ett lagrings mål.</span><span class="sxs-lookup"><span data-stu-id="98430-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="98430-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98430-104">SYNTAX</span></span>

### <span data-ttu-id="98430-105">ClfsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="98430-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98430-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="98430-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98430-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98430-107">DESCRIPTION</span></span>
<span data-ttu-id="98430-108">Cmdleten **set-AzHpcCacheStorageTarget** uppdaterar ett lagrings mål som är kopplat till Azure HPC-cachen.</span><span class="sxs-lookup"><span data-stu-id="98430-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="98430-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98430-109">EXAMPLES</span></span>

### <span data-ttu-id="98430-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="98430-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="98430-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="98430-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="98430-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98430-112">PARAMETERS</span></span>

### <span data-ttu-id="98430-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98430-113">-AsJob</span></span>
<span data-ttu-id="98430-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="98430-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98430-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="98430-115">-CacheName</span></span>
<span data-ttu-id="98430-116">Cacheminnets namn.</span><span class="sxs-lookup"><span data-stu-id="98430-116">Name of cache.</span></span>

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

### <span data-ttu-id="98430-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="98430-117">-CLFS</span></span>
<span data-ttu-id="98430-118">Uppdatera CLFS.</span><span class="sxs-lookup"><span data-stu-id="98430-118">Update CLFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98430-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98430-119">-DefaultProfile</span></span>
<span data-ttu-id="98430-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98430-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98430-121">-Force</span><span class="sxs-lookup"><span data-stu-id="98430-121">-Force</span></span>
<span data-ttu-id="98430-122">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="98430-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="98430-123">Denna cmdlet uppmanar dig som standard att bekräfta att du vill tömma cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="98430-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="98430-124">-Koppling</span><span class="sxs-lookup"><span data-stu-id="98430-124">-Junction</span></span>
<span data-ttu-id="98430-125">Punkt.</span><span class="sxs-lookup"><span data-stu-id="98430-125">Junction.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98430-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="98430-126">-Name</span></span>
<span data-ttu-id="98430-127">Namn på lagrings målet.</span><span class="sxs-lookup"><span data-stu-id="98430-127">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98430-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="98430-128">-NFS</span></span>
<span data-ttu-id="98430-129">Uppdatera typen av NFS-lagring.</span><span class="sxs-lookup"><span data-stu-id="98430-129">Update NFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98430-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98430-130">-ResourceGroupName</span></span>
<span data-ttu-id="98430-131">Namnet på den resurs grupp under vilket du vill uppdatera lagrings målet.</span><span class="sxs-lookup"><span data-stu-id="98430-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="98430-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="98430-132">-Confirm</span></span>
<span data-ttu-id="98430-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="98430-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98430-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98430-134">-WhatIf</span></span>
<span data-ttu-id="98430-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="98430-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98430-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="98430-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98430-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98430-137">CommonParameters</span></span>
<span data-ttu-id="98430-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98430-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98430-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98430-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98430-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98430-140">INPUTS</span></span>

### <span data-ttu-id="98430-141">System. String</span><span class="sxs-lookup"><span data-stu-id="98430-141">System.String</span></span>

## <span data-ttu-id="98430-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98430-142">OUTPUTS</span></span>

### <span data-ttu-id="98430-143">Microsoft. Azure. PowerShell. cmdletar. HPCCache. Models. PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="98430-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="98430-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98430-144">NOTES</span></span>

## <span data-ttu-id="98430-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98430-145">RELATED LINKS</span></span>

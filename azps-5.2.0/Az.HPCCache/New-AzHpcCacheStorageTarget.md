---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412531"
---
# <span data-ttu-id="fb42c-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="fb42c-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="fb42c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb42c-102">SYNOPSIS</span></span>
<span data-ttu-id="fb42c-103">Skapar ett lagrings mål.</span><span class="sxs-lookup"><span data-stu-id="fb42c-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="fb42c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb42c-104">SYNTAX</span></span>

### <span data-ttu-id="fb42c-105">ClfsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fb42c-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb42c-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb42c-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb42c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb42c-107">DESCRIPTION</span></span>
<span data-ttu-id="fb42c-108">Cmdleten **New-AzHpcCacheStorageTarget** lägger till ett lagrings mål för Azure HPC-cachen.</span><span class="sxs-lookup"><span data-stu-id="fb42c-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="fb42c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb42c-109">EXAMPLES</span></span>

### <span data-ttu-id="fb42c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fb42c-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="fb42c-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fb42c-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="fb42c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb42c-112">PARAMETERS</span></span>

### <span data-ttu-id="fb42c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb42c-113">-AsJob</span></span>
<span data-ttu-id="fb42c-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="fb42c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb42c-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="fb42c-115">-CacheName</span></span>
<span data-ttu-id="fb42c-116">Cacheminnets namn.</span><span class="sxs-lookup"><span data-stu-id="fb42c-116">Name of cache.</span></span>

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

### <span data-ttu-id="fb42c-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="fb42c-117">-CLFS</span></span>
<span data-ttu-id="fb42c-118">Uppdatera CLFS.</span><span class="sxs-lookup"><span data-stu-id="fb42c-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="fb42c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb42c-119">-DefaultProfile</span></span>
<span data-ttu-id="fb42c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb42c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb42c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fb42c-121">-Force</span></span>
<span data-ttu-id="fb42c-122">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="fb42c-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="fb42c-123">Denna cmdlet uppmanar dig som standard att bekräfta att du vill tömma cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="fb42c-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="fb42c-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="fb42c-124">-HostName</span></span>
<span data-ttu-id="fb42c-125">NFS-värdnamn.</span><span class="sxs-lookup"><span data-stu-id="fb42c-125">NFS host name.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb42c-126">-Koppling</span><span class="sxs-lookup"><span data-stu-id="fb42c-126">-Junction</span></span>
<span data-ttu-id="fb42c-127">Punkt.</span><span class="sxs-lookup"><span data-stu-id="fb42c-127">Junction.</span></span>

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

### <span data-ttu-id="fb42c-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb42c-128">-Name</span></span>
<span data-ttu-id="fb42c-129">Namn på lagrings målet.</span><span class="sxs-lookup"><span data-stu-id="fb42c-129">Name of storage target.</span></span>

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

### <span data-ttu-id="fb42c-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="fb42c-130">-NFS</span></span>
<span data-ttu-id="fb42c-131">Uppdatera typen av NFS-lagring.</span><span class="sxs-lookup"><span data-stu-id="fb42c-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="fb42c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb42c-132">-ResourceGroupName</span></span>
<span data-ttu-id="fb42c-133">"Namnet på den resurs grupp som du vill skapa ett lagrings mål för.</span><span class="sxs-lookup"><span data-stu-id="fb42c-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="fb42c-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="fb42c-134">-StorageContainerID</span></span>
<span data-ttu-id="fb42c-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="fb42c-135">StorageContainerID</span></span>

```yaml
Type: System.String
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb42c-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="fb42c-136">-UsageModel</span></span>
<span data-ttu-id="fb42c-137">Modell för NFS-användning.</span><span class="sxs-lookup"><span data-stu-id="fb42c-137">NFS usage model.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb42c-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb42c-138">-Confirm</span></span>
<span data-ttu-id="fb42c-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb42c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb42c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb42c-140">-WhatIf</span></span>
<span data-ttu-id="fb42c-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb42c-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb42c-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb42c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb42c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb42c-143">CommonParameters</span></span>
<span data-ttu-id="fb42c-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb42c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb42c-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb42c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb42c-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb42c-146">INPUTS</span></span>

### <span data-ttu-id="fb42c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="fb42c-147">System.String</span></span>

## <span data-ttu-id="fb42c-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb42c-148">OUTPUTS</span></span>

### <span data-ttu-id="fb42c-149">Microsoft. Azure. PowerShell. cmdletar. HPCCache. Models. PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="fb42c-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="fb42c-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb42c-150">NOTES</span></span>

## <span data-ttu-id="fb42c-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb42c-151">RELATED LINKS</span></span>

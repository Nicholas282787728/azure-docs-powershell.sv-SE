---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 1e50bba7c00c94daac983511f6fcea0ed1319759
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521695"
---
# <span data-ttu-id="bd551-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="bd551-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="bd551-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd551-102">SYNOPSIS</span></span>
<span data-ttu-id="bd551-103">Exporterar en databas fil från mål databasen.</span><span class="sxs-lookup"><span data-stu-id="bd551-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="bd551-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd551-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="bd551-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd551-105">DESCRIPTION</span></span>
<span data-ttu-id="bd551-106">Exporterar en databas fil från mål databasen.</span><span class="sxs-lookup"><span data-stu-id="bd551-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="bd551-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd551-107">EXAMPLES</span></span>

### <span data-ttu-id="bd551-108">Exempel 1: exportera databas</span><span class="sxs-lookup"><span data-stu-id="bd551-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="bd551-109">Det här kommandot exporterar databasen för Redis företags-cache med namnet mina cacheminne till en databas fil.</span><span class="sxs-lookup"><span data-stu-id="bd551-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="bd551-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd551-110">PARAMETERS</span></span>

### <span data-ttu-id="bd551-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd551-111">-AsJob</span></span>
<span data-ttu-id="bd551-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="bd551-112">Run the command as a job</span></span>

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

### <span data-ttu-id="bd551-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="bd551-113">-ClusterName</span></span>
<span data-ttu-id="bd551-114">Namnet på RedisEnterprise-klustret.</span><span class="sxs-lookup"><span data-stu-id="bd551-114">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd551-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd551-115">-DefaultProfile</span></span>
<span data-ttu-id="bd551-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd551-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd551-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bd551-117">-NoWait</span></span>
<span data-ttu-id="bd551-118">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="bd551-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bd551-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd551-119">-PassThru</span></span>
<span data-ttu-id="bd551-120">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="bd551-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bd551-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd551-121">-ResourceGroupName</span></span>
<span data-ttu-id="bd551-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bd551-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd551-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="bd551-123">-SasUri</span></span>
<span data-ttu-id="bd551-124">SAS URI för mål katalogen att exportera till</span><span class="sxs-lookup"><span data-stu-id="bd551-124">SAS Uri for the target directory to export to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd551-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd551-125">-SubscriptionId</span></span>
<span data-ttu-id="bd551-126">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="bd551-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="bd551-127">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="bd551-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd551-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bd551-128">-Confirm</span></span>
<span data-ttu-id="bd551-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bd551-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd551-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd551-130">-WhatIf</span></span>
<span data-ttu-id="bd551-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bd551-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd551-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bd551-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd551-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd551-133">CommonParameters</span></span>
<span data-ttu-id="bd551-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd551-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd551-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd551-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd551-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd551-136">INPUTS</span></span>

## <span data-ttu-id="bd551-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd551-137">OUTPUTS</span></span>

### <span data-ttu-id="bd551-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bd551-138">System.Boolean</span></span>

## <span data-ttu-id="bd551-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd551-139">NOTES</span></span>

<span data-ttu-id="bd551-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bd551-140">ALIASES</span></span>

## <span data-ttu-id="bd551-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd551-141">RELATED LINKS</span></span>


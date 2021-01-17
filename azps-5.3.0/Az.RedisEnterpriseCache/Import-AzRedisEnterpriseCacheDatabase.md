---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/import-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 6ab4babd894a3c639db6e41e6088653604072c7e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421195"
---
# <span data-ttu-id="3fb62-101">Import-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="3fb62-101">Import-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="3fb62-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3fb62-102">SYNOPSIS</span></span>
<span data-ttu-id="3fb62-103">Importerar en databas fil till mål databasen.</span><span class="sxs-lookup"><span data-stu-id="3fb62-103">Imports a database file to target database.</span></span>

## <span data-ttu-id="3fb62-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3fb62-104">SYNTAX</span></span>

```
Import-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3fb62-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3fb62-105">DESCRIPTION</span></span>
<span data-ttu-id="3fb62-106">Importerar en databas fil till mål databasen.</span><span class="sxs-lookup"><span data-stu-id="3fb62-106">Imports a database file to target database.</span></span>

## <span data-ttu-id="3fb62-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3fb62-107">EXAMPLES</span></span>

### <span data-ttu-id="3fb62-108">Exempel 1: importera databas</span><span class="sxs-lookup"><span data-stu-id="3fb62-108">Example 1: Import database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/myfilename?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="3fb62-109">Det här kommandot importerar en databas fil till databasen i Redis företags-cache med namnet mina cacheminne.</span><span class="sxs-lookup"><span data-stu-id="3fb62-109">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="3fb62-110">Exempel 2: importera databas (med exempel fil namn)</span><span class="sxs-lookup"><span data-stu-id="3fb62-110">Example 2: Import database (using example filename)</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/bk20201130-223654-1-db-1_of_1-2-0-16383.rdb.gz?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="3fb62-111">Det här kommandot importerar en databas fil till databasen i Redis företags-cache med namnet mina cacheminne.</span><span class="sxs-lookup"><span data-stu-id="3fb62-111">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="3fb62-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3fb62-112">PARAMETERS</span></span>

### <span data-ttu-id="3fb62-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fb62-113">-AsJob</span></span>
<span data-ttu-id="3fb62-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="3fb62-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3fb62-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="3fb62-115">-ClusterName</span></span>
<span data-ttu-id="3fb62-116">Namnet på RedisEnterprise-klustret.</span><span class="sxs-lookup"><span data-stu-id="3fb62-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="3fb62-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fb62-117">-DefaultProfile</span></span>
<span data-ttu-id="3fb62-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3fb62-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fb62-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3fb62-119">-NoWait</span></span>
<span data-ttu-id="3fb62-120">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="3fb62-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3fb62-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fb62-121">-PassThru</span></span>
<span data-ttu-id="3fb62-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="3fb62-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3fb62-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fb62-123">-ResourceGroupName</span></span>
<span data-ttu-id="3fb62-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3fb62-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="3fb62-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="3fb62-125">-SasUri</span></span>
<span data-ttu-id="3fb62-126">SAS URI för mål-BLOB att importera från</span><span class="sxs-lookup"><span data-stu-id="3fb62-126">SAS Uri for the target blob to import from</span></span>

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

### <span data-ttu-id="3fb62-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3fb62-127">-SubscriptionId</span></span>
<span data-ttu-id="3fb62-128">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3fb62-128">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3fb62-129">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="3fb62-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3fb62-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3fb62-130">-Confirm</span></span>
<span data-ttu-id="3fb62-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3fb62-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fb62-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fb62-132">-WhatIf</span></span>
<span data-ttu-id="3fb62-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3fb62-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fb62-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3fb62-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fb62-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fb62-135">CommonParameters</span></span>
<span data-ttu-id="3fb62-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fb62-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fb62-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fb62-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fb62-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3fb62-138">INPUTS</span></span>

## <span data-ttu-id="3fb62-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3fb62-139">OUTPUTS</span></span>

### <span data-ttu-id="3fb62-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3fb62-140">System.Boolean</span></span>

## <span data-ttu-id="3fb62-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3fb62-141">NOTES</span></span>

<span data-ttu-id="3fb62-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3fb62-142">ALIASES</span></span>

## <span data-ttu-id="3fb62-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3fb62-143">RELATED LINKS</span></span>


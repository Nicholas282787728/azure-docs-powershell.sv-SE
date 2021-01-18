---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: ab5985a7302834f4f7184a43ac2f5ebf795a3d83
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521680"
---
# <span data-ttu-id="79fc3-101">New-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="79fc3-101">New-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="79fc3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="79fc3-103">Återskapar RedisEnterprise-databasens Access-nycklar.</span><span class="sxs-lookup"><span data-stu-id="79fc3-103">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="79fc3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79fc3-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 -KeyType <AccessKeyType> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="79fc3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="79fc3-106">Återskapar RedisEnterprise-databasens Access-nycklar.</span><span class="sxs-lookup"><span data-stu-id="79fc3-106">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="79fc3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79fc3-107">EXAMPLES</span></span>

### <span data-ttu-id="79fc3-108">Exempel 1: återskapa primär åtkomst nyckeln</span><span class="sxs-lookup"><span data-stu-id="79fc3-108">Example 1: Regenerate primary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Primary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
new-primary-key                              secondary-key

```

<span data-ttu-id="79fc3-109">Det här kommandot återskapar den primära nyckeln för hemlig åtkomst som används för att autentisera anslutningar till databasen för Redis företags-cache med namnetin cache.</span><span class="sxs-lookup"><span data-stu-id="79fc3-109">This command regenerates the primary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="79fc3-110">Exempel 2: återskapa sekundär åtkomst nyckeln</span><span class="sxs-lookup"><span data-stu-id="79fc3-110">Example 2: Regenerate secondary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Secondary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  new-secondary-key

```

<span data-ttu-id="79fc3-111">Det här kommandot återskapar den sekundära nyckeln för hemlig åtkomst som används för att autentisera anslutningar till databasen för Redis företags-cache med namnetin cache.</span><span class="sxs-lookup"><span data-stu-id="79fc3-111">This command regenerates the secondary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="79fc3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79fc3-112">PARAMETERS</span></span>

### <span data-ttu-id="79fc3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79fc3-113">-AsJob</span></span>
<span data-ttu-id="79fc3-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="79fc3-114">Run the command as a job</span></span>

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

### <span data-ttu-id="79fc3-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="79fc3-115">-ClusterName</span></span>
<span data-ttu-id="79fc3-116">Namnet på RedisEnterprise-klustret.</span><span class="sxs-lookup"><span data-stu-id="79fc3-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="79fc3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79fc3-117">-DefaultProfile</span></span>
<span data-ttu-id="79fc3-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79fc3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79fc3-119">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="79fc3-119">-KeyType</span></span>
<span data-ttu-id="79fc3-120">Vilken åtkomst-nyckeln som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="79fc3-120">Which access key to regenerate.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.AccessKeyType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc3-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="79fc3-121">-NoWait</span></span>
<span data-ttu-id="79fc3-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="79fc3-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="79fc3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79fc3-123">-ResourceGroupName</span></span>
<span data-ttu-id="79fc3-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="79fc3-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="79fc3-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="79fc3-125">-SubscriptionId</span></span>
<span data-ttu-id="79fc3-126">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="79fc3-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="79fc3-127">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="79fc3-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="79fc3-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="79fc3-128">-Confirm</span></span>
<span data-ttu-id="79fc3-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="79fc3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79fc3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79fc3-130">-WhatIf</span></span>
<span data-ttu-id="79fc3-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="79fc3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79fc3-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="79fc3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79fc3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79fc3-133">CommonParameters</span></span>
<span data-ttu-id="79fc3-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79fc3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79fc3-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79fc3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79fc3-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79fc3-136">INPUTS</span></span>

## <span data-ttu-id="79fc3-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79fc3-137">OUTPUTS</span></span>

### <span data-ttu-id="79fc3-138">Microsoft. Azure. PowerShell. cmdletar. RedisEnterpriseCache. Models. Api20201001Preview. IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="79fc3-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="79fc3-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79fc3-139">NOTES</span></span>

<span data-ttu-id="79fc3-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="79fc3-140">ALIASES</span></span>

## <span data-ttu-id="79fc3-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79fc3-141">RELATED LINKS</span></span>


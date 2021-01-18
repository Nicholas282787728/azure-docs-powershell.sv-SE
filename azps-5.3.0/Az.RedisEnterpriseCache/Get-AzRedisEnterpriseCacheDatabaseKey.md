---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: e602cb4fc86ede6a4e1f7cc894c1825fd1d560fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521683"
---
# <span data-ttu-id="95547-101">Get-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="95547-101">Get-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="95547-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95547-102">SYNOPSIS</span></span>
<span data-ttu-id="95547-103">Hämtar åtkomst nycklar för RedisEnterprise-databasen.</span><span class="sxs-lookup"><span data-stu-id="95547-103">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="95547-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95547-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="95547-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95547-105">DESCRIPTION</span></span>
<span data-ttu-id="95547-106">Hämtar åtkomst nycklar för RedisEnterprise-databasen.</span><span class="sxs-lookup"><span data-stu-id="95547-106">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="95547-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95547-107">EXAMPLES</span></span>

### <span data-ttu-id="95547-108">Exempel 1: Hämta databas åtkomst nycklar</span><span class="sxs-lookup"><span data-stu-id="95547-108">Example 1: Get database access keys</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  secondary-key

```

<span data-ttu-id="95547-109">Det här kommandot får de hemliga åtkomst nycklar som används för att autentisera anslutningar till databasen för Redis företags-cache med namnetin-cache.</span><span class="sxs-lookup"><span data-stu-id="95547-109">This command gets the secret access keys used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="95547-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95547-110">PARAMETERS</span></span>

### <span data-ttu-id="95547-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="95547-111">-ClusterName</span></span>
<span data-ttu-id="95547-112">Namnet på RedisEnterprise-klustret.</span><span class="sxs-lookup"><span data-stu-id="95547-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="95547-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95547-113">-DefaultProfile</span></span>
<span data-ttu-id="95547-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95547-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95547-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95547-115">-ResourceGroupName</span></span>
<span data-ttu-id="95547-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="95547-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="95547-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95547-117">-SubscriptionId</span></span>
<span data-ttu-id="95547-118">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="95547-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="95547-119">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="95547-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95547-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="95547-120">-Confirm</span></span>
<span data-ttu-id="95547-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="95547-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95547-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95547-122">-WhatIf</span></span>
<span data-ttu-id="95547-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="95547-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95547-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="95547-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95547-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95547-125">CommonParameters</span></span>
<span data-ttu-id="95547-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95547-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95547-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95547-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95547-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95547-128">INPUTS</span></span>

## <span data-ttu-id="95547-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95547-129">OUTPUTS</span></span>

### <span data-ttu-id="95547-130">Microsoft. Azure. PowerShell. cmdletar. RedisEnterpriseCache. Models. Api20201001Preview. IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="95547-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="95547-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95547-131">NOTES</span></span>

<span data-ttu-id="95547-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="95547-132">ALIASES</span></span>

## <span data-ttu-id="95547-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95547-133">RELATED LINKS</span></span>


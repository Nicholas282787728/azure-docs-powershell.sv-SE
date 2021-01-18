---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 99956b752b71309278af4c1f9b43b8efa9015f21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521687"
---
# <span data-ttu-id="31c9f-101">Get-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="31c9f-101">Get-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="31c9f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31c9f-102">SYNOPSIS</span></span>
<span data-ttu-id="31c9f-103">Hämtar information om en databas i ett RedisEnterprise-kluster.</span><span class="sxs-lookup"><span data-stu-id="31c9f-103">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="31c9f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31c9f-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="31c9f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31c9f-105">DESCRIPTION</span></span>
<span data-ttu-id="31c9f-106">Hämtar information om en databas i ett RedisEnterprise-kluster.</span><span class="sxs-lookup"><span data-stu-id="31c9f-106">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="31c9f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31c9f-107">EXAMPLES</span></span>

### <span data-ttu-id="31c9f-108">Exempel 1: Hämta databas</span><span class="sxs-lookup"><span data-stu-id="31c9f-108">Example 1: Get database</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="31c9f-109">Det här kommandot får databasen för Redis företags-cachen med namnet mina cacheminne.</span><span class="sxs-lookup"><span data-stu-id="31c9f-109">This command gets the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="31c9f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31c9f-110">PARAMETERS</span></span>

### <span data-ttu-id="31c9f-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="31c9f-111">-ClusterName</span></span>
<span data-ttu-id="31c9f-112">Namnet på RedisEnterprise-klustret.</span><span class="sxs-lookup"><span data-stu-id="31c9f-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="31c9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31c9f-113">-DefaultProfile</span></span>
<span data-ttu-id="31c9f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31c9f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31c9f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31c9f-115">-ResourceGroupName</span></span>
<span data-ttu-id="31c9f-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="31c9f-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="31c9f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31c9f-117">-SubscriptionId</span></span>
<span data-ttu-id="31c9f-118">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="31c9f-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="31c9f-119">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="31c9f-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="31c9f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31c9f-120">CommonParameters</span></span>
<span data-ttu-id="31c9f-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31c9f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31c9f-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31c9f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31c9f-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31c9f-123">INPUTS</span></span>

## <span data-ttu-id="31c9f-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31c9f-124">OUTPUTS</span></span>

### <span data-ttu-id="31c9f-125">Microsoft. Azure. PowerShell. cmdletar. RedisEnterpriseCache. Models. Api20201001Preview. IDatabase</span><span class="sxs-lookup"><span data-stu-id="31c9f-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="31c9f-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31c9f-126">NOTES</span></span>

<span data-ttu-id="31c9f-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="31c9f-127">ALIASES</span></span>

## <span data-ttu-id="31c9f-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31c9f-128">RELATED LINKS</span></span>


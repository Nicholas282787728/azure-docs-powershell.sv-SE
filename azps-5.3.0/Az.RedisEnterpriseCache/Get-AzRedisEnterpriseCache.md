---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: a6fe478aa8221060974f54e75b63a64edf0beae4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521684"
---
# <span data-ttu-id="4305a-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="4305a-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="4305a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4305a-102">SYNOPSIS</span></span>
<span data-ttu-id="4305a-103">Hämtar information om ett RedisEnterprise-kluster och dess associerade databas</span><span class="sxs-lookup"><span data-stu-id="4305a-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="4305a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4305a-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4305a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4305a-105">DESCRIPTION</span></span>
<span data-ttu-id="4305a-106">Hämtar information om ett RedisEnterprise-kluster och dess associerade databas</span><span class="sxs-lookup"><span data-stu-id="4305a-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="4305a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4305a-107">EXAMPLES</span></span>

### <span data-ttu-id="4305a-108">Exempel 1: skaffa en Redis företags-cache efter namn</span><span class="sxs-lookup"><span data-stu-id="4305a-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="4305a-109">Det här kommandot hämtar Redis företags-cache med namnetin-cache.</span><span class="sxs-lookup"><span data-stu-id="4305a-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="4305a-110">Exempel 2: Hämta alla Redis företags-cache i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="4305a-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="4305a-111">Det här kommandot får alla Redis företags-cachen i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4305a-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="4305a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4305a-112">PARAMETERS</span></span>

### <span data-ttu-id="4305a-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="4305a-113">-ClusterName</span></span>
<span data-ttu-id="4305a-114">Namnet på RedisEnterprise-klustret.</span><span class="sxs-lookup"><span data-stu-id="4305a-114">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4305a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4305a-115">-DefaultProfile</span></span>
<span data-ttu-id="4305a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4305a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4305a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4305a-117">-ResourceGroupName</span></span>
<span data-ttu-id="4305a-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4305a-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="4305a-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4305a-119">-SubscriptionId</span></span>
<span data-ttu-id="4305a-120">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4305a-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4305a-121">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="4305a-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4305a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4305a-122">CommonParameters</span></span>
<span data-ttu-id="4305a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4305a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4305a-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4305a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4305a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4305a-125">INPUTS</span></span>

## <span data-ttu-id="4305a-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4305a-126">OUTPUTS</span></span>

### <span data-ttu-id="4305a-127">Microsoft. Azure. PowerShell. cmdletar. RedisEnterpriseCache. Models. Api20201001Preview. ICluster</span><span class="sxs-lookup"><span data-stu-id="4305a-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="4305a-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4305a-128">NOTES</span></span>

<span data-ttu-id="4305a-129">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4305a-129">ALIASES</span></span>

## <span data-ttu-id="4305a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4305a-130">RELATED LINKS</span></span>


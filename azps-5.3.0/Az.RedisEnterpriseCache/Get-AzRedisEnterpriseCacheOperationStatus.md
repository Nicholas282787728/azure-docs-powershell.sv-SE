---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecacheoperationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
ms.openlocfilehash: 8416c18ac945eaab5ae9dbd758d2660c4f950417
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421200"
---
# <span data-ttu-id="7e1bd-101">Get-AzRedisEnterpriseCacheOperationStatus</span><span class="sxs-lookup"><span data-stu-id="7e1bd-101">Get-AzRedisEnterpriseCacheOperationStatus</span></span>

## <span data-ttu-id="7e1bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="7e1bd-103">Får statusen.</span><span class="sxs-lookup"><span data-stu-id="7e1bd-103">Gets the status of operation.</span></span>

## <span data-ttu-id="7e1bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e1bd-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheOperationStatus -Location <String> -OperationId <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7e1bd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e1bd-105">DESCRIPTION</span></span>
<span data-ttu-id="7e1bd-106">Får statusen.</span><span class="sxs-lookup"><span data-stu-id="7e1bd-106">Gets the status of operation.</span></span>

## <span data-ttu-id="7e1bd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e1bd-107">EXAMPLES</span></span>

### <span data-ttu-id="7e1bd-108">Exempel 1: Hämta åtgärds status</span><span class="sxs-lookup"><span data-stu-id="7e1bd-108">Example 1: Get operation status</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheOperationStatus -Location "East US" -OperationId "6432a8f9-0fe6-4339-9303-772c92f35d02"

EndTime                           Name                                 StartTime                         Status
-------                           ----                                 ---------                         ------
2020-12-01T00:12:45.7107366+00:00 6432a8f9-0fe6-4339-9303-772c92f35d02 2020-12-01T00:04:35.7061294+00:00 Succeeded

```

<span data-ttu-id="7e1bd-109">Det här kommandot får statusen för en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="7e1bd-109">This command gets the status of an operation.</span></span>

## <span data-ttu-id="7e1bd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e1bd-110">PARAMETERS</span></span>

### <span data-ttu-id="7e1bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e1bd-111">-DefaultProfile</span></span>
<span data-ttu-id="7e1bd-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e1bd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e1bd-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="7e1bd-113">-Location</span></span>
<span data-ttu-id="7e1bd-114">Regionen som operationen befinner sig i.</span><span class="sxs-lookup"><span data-stu-id="7e1bd-114">The region the operation is in.</span></span>

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

### <span data-ttu-id="7e1bd-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7e1bd-115">-OperationId</span></span>
<span data-ttu-id="7e1bd-116">Åtgärdens unika identifierare.</span><span class="sxs-lookup"><span data-stu-id="7e1bd-116">The operation's unique identifier.</span></span>

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

### <span data-ttu-id="7e1bd-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e1bd-117">-SubscriptionId</span></span>
<span data-ttu-id="7e1bd-118">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7e1bd-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7e1bd-119">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="7e1bd-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7e1bd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e1bd-120">CommonParameters</span></span>
<span data-ttu-id="7e1bd-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e1bd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e1bd-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e1bd-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e1bd-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e1bd-123">INPUTS</span></span>

## <span data-ttu-id="7e1bd-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e1bd-124">OUTPUTS</span></span>

### <span data-ttu-id="7e1bd-125">Microsoft. Azure. PowerShell. cmdletar. RedisEnterpriseCache. Models. Api20201001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="7e1bd-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span></span>

## <span data-ttu-id="7e1bd-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e1bd-126">NOTES</span></span>

<span data-ttu-id="7e1bd-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7e1bd-127">ALIASES</span></span>

## <span data-ttu-id="7e1bd-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e1bd-128">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390267"
---
# <span data-ttu-id="311ac-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="311ac-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="311ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="311ac-102">SYNOPSIS</span></span>
<span data-ttu-id="311ac-103">Skaffa lagrings mål för HPC-cachen.</span><span class="sxs-lookup"><span data-stu-id="311ac-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="311ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="311ac-104">SYNTAX</span></span>

### <span data-ttu-id="311ac-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="311ac-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="311ac-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="311ac-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="311ac-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="311ac-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="311ac-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="311ac-108">DESCRIPTION</span></span>
<span data-ttu-id="311ac-109">Cmdleten **Get-AzHpcCacheStorageTarget** hämtar lagrings mål som finns i cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="311ac-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="311ac-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="311ac-110">EXAMPLES</span></span>

### <span data-ttu-id="311ac-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="311ac-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="311ac-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="311ac-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="311ac-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="311ac-113">PARAMETERS</span></span>

### <span data-ttu-id="311ac-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="311ac-114">-CacheId</span></span>
<span data-ttu-id="311ac-115">Resurs-ID för cacheminnet</span><span class="sxs-lookup"><span data-stu-id="311ac-115">The resource id of the Cache</span></span>

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

### <span data-ttu-id="311ac-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="311ac-116">-CacheName</span></span>
<span data-ttu-id="311ac-117">Cacheminnets namn.</span><span class="sxs-lookup"><span data-stu-id="311ac-117">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="311ac-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="311ac-118">-CacheObject</span></span>
<span data-ttu-id="311ac-119">Cacheobjektet att starta.</span><span class="sxs-lookup"><span data-stu-id="311ac-119">The cache object to start.</span></span>

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

### <span data-ttu-id="311ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="311ac-120">-DefaultProfile</span></span>
<span data-ttu-id="311ac-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="311ac-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="311ac-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="311ac-122">-Name</span></span>
<span data-ttu-id="311ac-123">Namn på lagrings målet.</span><span class="sxs-lookup"><span data-stu-id="311ac-123">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: StorageTargetName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="311ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="311ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="311ac-125">Namnet på resurs gruppens cacheminne är in.</span><span class="sxs-lookup"><span data-stu-id="311ac-125">Name of resource group cache is in.</span></span>


```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="311ac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="311ac-126">CommonParameters</span></span>
<span data-ttu-id="311ac-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="311ac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="311ac-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="311ac-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="311ac-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="311ac-129">INPUTS</span></span>

### <span data-ttu-id="311ac-130">System. String</span><span class="sxs-lookup"><span data-stu-id="311ac-130">System.String</span></span>

## <span data-ttu-id="311ac-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="311ac-131">OUTPUTS</span></span>

### <span data-ttu-id="311ac-132">Microsoft. Azure. PowerShell. cmdletar. HPCCache. Models. PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="311ac-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="311ac-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="311ac-133">NOTES</span></span>

## <span data-ttu-id="311ac-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="311ac-134">RELATED LINKS</span></span>

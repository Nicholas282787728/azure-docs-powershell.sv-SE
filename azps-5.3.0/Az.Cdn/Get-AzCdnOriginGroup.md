---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524625"
---
# <span data-ttu-id="3af82-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="3af82-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="3af82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3af82-102">SYNOPSIS</span></span>
<span data-ttu-id="3af82-103">Hämtar en CDN-underlaget</span><span class="sxs-lookup"><span data-stu-id="3af82-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="3af82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3af82-104">SYNTAX</span></span>

### <span data-ttu-id="3af82-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3af82-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3af82-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3af82-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3af82-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3af82-107">DESCRIPTION</span></span>
<span data-ttu-id="3af82-108">I Get-AzCdnOriginGroup cmdlet hämtas en CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="3af82-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="3af82-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3af82-109">EXAMPLES</span></span>

### <span data-ttu-id="3af82-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3af82-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="3af82-111">Det här kommandot hämtar ursprungs gruppen inom den angivna slut punkten.</span><span class="sxs-lookup"><span data-stu-id="3af82-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="3af82-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3af82-112">PARAMETERS</span></span>

### <span data-ttu-id="3af82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af82-113">-DefaultProfile</span></span>
<span data-ttu-id="3af82-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3af82-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3af82-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3af82-115">-EndpointName</span></span>
<span data-ttu-id="3af82-116">Namn på Azure CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="3af82-116">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af82-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="3af82-117">-OriginGroupName</span></span>
<span data-ttu-id="3af82-118">Namn på en grupp med Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="3af82-118">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af82-119">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="3af82-119">-ProfileName</span></span>
<span data-ttu-id="3af82-120">Namn på Azure CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="3af82-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af82-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af82-121">-ResourceGroupName</span></span>
<span data-ttu-id="3af82-122">Resurs gruppen för Azure CDN-profilen.</span><span class="sxs-lookup"><span data-stu-id="3af82-122">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af82-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3af82-123">-ResourceId</span></span>
<span data-ttu-id="3af82-124">Resurs-ID för gruppen ursprung</span><span class="sxs-lookup"><span data-stu-id="3af82-124">Resource Id for the the origin group</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af82-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af82-125">CommonParameters</span></span>
<span data-ttu-id="3af82-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3af82-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af82-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3af82-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af82-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3af82-128">INPUTS</span></span>

### <span data-ttu-id="3af82-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="3af82-129">None</span></span>

## <span data-ttu-id="3af82-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3af82-130">OUTPUTS</span></span>

### <span data-ttu-id="3af82-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="3af82-131">System.Object</span></span>

## <span data-ttu-id="3af82-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3af82-132">NOTES</span></span>

## <span data-ttu-id="3af82-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3af82-133">RELATED LINKS</span></span>

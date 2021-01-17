---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422792"
---
# <span data-ttu-id="da8ed-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="da8ed-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="da8ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="da8ed-103">Hämtar en privat länk resurs.</span><span class="sxs-lookup"><span data-stu-id="da8ed-103">Gets a private link resource.</span></span>

## <span data-ttu-id="da8ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da8ed-104">SYNTAX</span></span>

### <span data-ttu-id="da8ed-105">ByPrivateLinkResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="da8ed-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da8ed-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="da8ed-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="da8ed-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da8ed-107">DESCRIPTION</span></span>
<span data-ttu-id="da8ed-108">Cmdleten **Get-AzPrivateLinkResource** hämtar alla länk resurser tillhör PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="da8ed-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="da8ed-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da8ed-109">EXAMPLES</span></span>

### <span data-ttu-id="da8ed-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="da8ed-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="da8ed-111">I det här exemplet listas alla nbelong för privata länkar till SQL Server med namnet mySql.</span><span class="sxs-lookup"><span data-stu-id="da8ed-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="da8ed-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da8ed-112">PARAMETERS</span></span>

### <span data-ttu-id="da8ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da8ed-113">-DefaultProfile</span></span>
<span data-ttu-id="da8ed-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da8ed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da8ed-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="da8ed-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="da8ed-116">Azure Resource Manager-ID för den privata länk resursen.</span><span class="sxs-lookup"><span data-stu-id="da8ed-116">The Azure resource manager id of the private link resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da8ed-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="da8ed-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="da8ed-118">Resurs typen privat länk.</span><span class="sxs-lookup"><span data-stu-id="da8ed-118">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da8ed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da8ed-119">-ResourceGroupName</span></span>
<span data-ttu-id="da8ed-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="da8ed-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da8ed-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="da8ed-121">-ServiceName</span></span>
<span data-ttu-id="da8ed-122">Namnet på den privata länk tjänsten.</span><span class="sxs-lookup"><span data-stu-id="da8ed-122">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da8ed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da8ed-123">CommonParameters</span></span>
<span data-ttu-id="da8ed-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da8ed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da8ed-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da8ed-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da8ed-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da8ed-126">INPUTS</span></span>

### <span data-ttu-id="da8ed-127">System. String</span><span class="sxs-lookup"><span data-stu-id="da8ed-127">System.String</span></span>

## <span data-ttu-id="da8ed-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da8ed-128">OUTPUTS</span></span>

### <span data-ttu-id="da8ed-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da8ed-129">System.Boolean</span></span>

## <span data-ttu-id="da8ed-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da8ed-130">NOTES</span></span>

## <span data-ttu-id="da8ed-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da8ed-131">RELATED LINKS</span></span>

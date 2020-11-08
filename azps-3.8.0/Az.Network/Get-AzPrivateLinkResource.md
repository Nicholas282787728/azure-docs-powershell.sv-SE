---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 3ba277ccee3a07f71677628fdc0a985225cdf724
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091029"
---
# <span data-ttu-id="46b85-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="46b85-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="46b85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46b85-102">SYNOPSIS</span></span>
<span data-ttu-id="46b85-103">Hämtar en privat länk resurs.</span><span class="sxs-lookup"><span data-stu-id="46b85-103">Gets a private link resource.</span></span>

## <span data-ttu-id="46b85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46b85-104">SYNTAX</span></span>

### <span data-ttu-id="46b85-105">ByPrivateLinkResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="46b85-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46b85-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46b85-106">DESCRIPTION</span></span>
<span data-ttu-id="46b85-107">Cmdleten **Get-AzPrivateLinkResource** hämtar alla länk resurser tillhör PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="46b85-107">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="46b85-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46b85-108">EXAMPLES</span></span>

### <span data-ttu-id="46b85-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="46b85-109">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="46b85-110">I det här exemplet listas alla nbelong för privata länkar till SQL Server med namnet mySql.</span><span class="sxs-lookup"><span data-stu-id="46b85-110">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="46b85-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46b85-111">PARAMETERS</span></span>

### <span data-ttu-id="46b85-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b85-112">-DefaultProfile</span></span>
<span data-ttu-id="46b85-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46b85-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46b85-114">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="46b85-114">-PrivateLinkResourceId</span></span>
<span data-ttu-id="46b85-115">Azure Resource Manager-ID för den privata länk resursen.</span><span class="sxs-lookup"><span data-stu-id="46b85-115">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="46b85-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b85-116">CommonParameters</span></span>
<span data-ttu-id="46b85-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b85-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b85-118">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46b85-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b85-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46b85-119">INPUTS</span></span>

### <span data-ttu-id="46b85-120">System. String</span><span class="sxs-lookup"><span data-stu-id="46b85-120">System.String</span></span>

## <span data-ttu-id="46b85-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46b85-121">OUTPUTS</span></span>

### <span data-ttu-id="46b85-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46b85-122">System.Boolean</span></span>

## <span data-ttu-id="46b85-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46b85-123">NOTES</span></span>

## <span data-ttu-id="46b85-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46b85-124">RELATED LINKS</span></span>

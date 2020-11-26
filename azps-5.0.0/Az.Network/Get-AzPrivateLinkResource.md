---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323849"
---
# <span data-ttu-id="93a6d-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="93a6d-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="93a6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="93a6d-103">Hämtar en privat länk resurs.</span><span class="sxs-lookup"><span data-stu-id="93a6d-103">Gets a private link resource.</span></span>

## <span data-ttu-id="93a6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93a6d-104">SYNTAX</span></span>

### <span data-ttu-id="93a6d-105">ByPrivateLinkResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="93a6d-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93a6d-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="93a6d-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="93a6d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93a6d-107">DESCRIPTION</span></span>
<span data-ttu-id="93a6d-108">Cmdleten **Get-AzPrivateLinkResource** hämtar alla länk resurser tillhör PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="93a6d-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="93a6d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93a6d-109">EXAMPLES</span></span>

### <span data-ttu-id="93a6d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="93a6d-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="93a6d-111">I det här exemplet listas alla nbelong för privata länkar till SQL Server med namnet mySql.</span><span class="sxs-lookup"><span data-stu-id="93a6d-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="93a6d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93a6d-112">PARAMETERS</span></span>

### <span data-ttu-id="93a6d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93a6d-113">-DefaultProfile</span></span>
<span data-ttu-id="93a6d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="93a6d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93a6d-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="93a6d-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="93a6d-116">Azure Resource Manager-ID för den privata länk resursen.</span><span class="sxs-lookup"><span data-stu-id="93a6d-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="93a6d-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="93a6d-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="93a6d-118">Resurs typen privat länk.</span><span class="sxs-lookup"><span data-stu-id="93a6d-118">The private link resource type.</span></span>

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

### <span data-ttu-id="93a6d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93a6d-119">-ResourceGroupName</span></span>
<span data-ttu-id="93a6d-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="93a6d-120">The resource group name.</span></span>

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

### <span data-ttu-id="93a6d-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="93a6d-121">-ServiceName</span></span>
<span data-ttu-id="93a6d-122">Namnet på den privata länk tjänsten.</span><span class="sxs-lookup"><span data-stu-id="93a6d-122">The private link service name.</span></span>

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

### <span data-ttu-id="93a6d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a6d-123">CommonParameters</span></span>
<span data-ttu-id="93a6d-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93a6d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a6d-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93a6d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a6d-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93a6d-126">INPUTS</span></span>

### <span data-ttu-id="93a6d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="93a6d-127">System.String</span></span>

## <span data-ttu-id="93a6d-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93a6d-128">OUTPUTS</span></span>

### <span data-ttu-id="93a6d-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93a6d-129">System.Boolean</span></span>

## <span data-ttu-id="93a6d-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93a6d-130">NOTES</span></span>

## <span data-ttu-id="93a6d-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93a6d-131">RELATED LINKS</span></span>
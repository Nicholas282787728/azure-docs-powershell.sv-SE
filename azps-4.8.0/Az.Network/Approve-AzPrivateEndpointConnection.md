---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262132"
---
# <span data-ttu-id="4b7d7-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4b7d7-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="4b7d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b7d7-102">SYNOPSIS</span></span>
<span data-ttu-id="4b7d7-103">Godkänner en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="4b7d7-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="4b7d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b7d7-104">SYNTAX</span></span>

### <span data-ttu-id="4b7d7-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="4b7d7-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b7d7-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="4b7d7-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b7d7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b7d7-107">DESCRIPTION</span></span>
<span data-ttu-id="4b7d7-108">Cmdleten **Godkänn-AzPrivateEndpointConnection** godkänner en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="4b7d7-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="4b7d7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b7d7-109">EXAMPLES</span></span>

### <span data-ttu-id="4b7d7-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4b7d7-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="4b7d7-111">I det här exemplet godkänns en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="4b7d7-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="4b7d7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b7d7-112">PARAMETERS</span></span>

### <span data-ttu-id="4b7d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b7d7-113">-DefaultProfile</span></span>
<span data-ttu-id="4b7d7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4b7d7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b7d7-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="4b7d7-115">-Description</span></span>
<span data-ttu-id="4b7d7-116">Skälet till åtgärden.</span><span class="sxs-lookup"><span data-stu-id="4b7d7-116">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b7d7-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="4b7d7-117">-Name</span></span>
<span data-ttu-id="4b7d7-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="4b7d7-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b7d7-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="4b7d7-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="4b7d7-120">Resurs typen privat länk.</span><span class="sxs-lookup"><span data-stu-id="4b7d7-120">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b7d7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b7d7-121">-ResourceGroupName</span></span>
<span data-ttu-id="4b7d7-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4b7d7-122">The resource group name.</span></span>

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

### <span data-ttu-id="4b7d7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b7d7-123">-ResourceId</span></span>
<span data-ttu-id="4b7d7-124">Azure Resource Manager-ID för den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="4b7d7-124">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b7d7-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4b7d7-125">-ServiceName</span></span>
<span data-ttu-id="4b7d7-126">Namnet på den privata länk tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4b7d7-126">The private link service name.</span></span>

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


### <span data-ttu-id="4b7d7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b7d7-127">CommonParameters</span></span>
<span data-ttu-id="4b7d7-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b7d7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b7d7-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b7d7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b7d7-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b7d7-130">INPUTS</span></span>

### <span data-ttu-id="4b7d7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4b7d7-131">System.String</span></span>

## <span data-ttu-id="4b7d7-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b7d7-132">OUTPUTS</span></span>

### <span data-ttu-id="4b7d7-133">Microsoft. Azure. commands. Networks. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4b7d7-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="4b7d7-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b7d7-134">NOTES</span></span>

## <span data-ttu-id="4b7d7-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b7d7-135">RELATED LINKS</span></span>

[<span data-ttu-id="4b7d7-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4b7d7-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="4b7d7-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4b7d7-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="4b7d7-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4b7d7-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="4b7d7-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4b7d7-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
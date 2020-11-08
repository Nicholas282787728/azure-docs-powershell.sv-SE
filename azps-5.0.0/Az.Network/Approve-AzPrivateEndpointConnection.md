---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272078"
---
# <span data-ttu-id="395fb-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="395fb-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="395fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="395fb-102">SYNOPSIS</span></span>
<span data-ttu-id="395fb-103">Godkänner en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="395fb-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="395fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="395fb-104">SYNTAX</span></span>

### <span data-ttu-id="395fb-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="395fb-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="395fb-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="395fb-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="395fb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="395fb-107">DESCRIPTION</span></span>
<span data-ttu-id="395fb-108">Cmdleten **Godkänn-AzPrivateEndpointConnection** godkänner en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="395fb-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="395fb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="395fb-109">EXAMPLES</span></span>

### <span data-ttu-id="395fb-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="395fb-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="395fb-111">I det här exemplet godkänns en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="395fb-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="395fb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="395fb-112">PARAMETERS</span></span>

### <span data-ttu-id="395fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395fb-113">-DefaultProfile</span></span>
<span data-ttu-id="395fb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="395fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="395fb-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="395fb-115">-Description</span></span>
<span data-ttu-id="395fb-116">Skälet till åtgärden.</span><span class="sxs-lookup"><span data-stu-id="395fb-116">The reason of action.</span></span>

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

### <span data-ttu-id="395fb-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="395fb-117">-Name</span></span>
<span data-ttu-id="395fb-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="395fb-118">The resource name.</span></span>

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

### <span data-ttu-id="395fb-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="395fb-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="395fb-120">Resurs typen privat länk.</span><span class="sxs-lookup"><span data-stu-id="395fb-120">The private link resource type.</span></span>

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

### <span data-ttu-id="395fb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="395fb-121">-ResourceGroupName</span></span>
<span data-ttu-id="395fb-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="395fb-122">The resource group name.</span></span>

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

### <span data-ttu-id="395fb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="395fb-123">-ResourceId</span></span>
<span data-ttu-id="395fb-124">Azure Resource Manager-ID för den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="395fb-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="395fb-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="395fb-125">-ServiceName</span></span>
<span data-ttu-id="395fb-126">Namnet på den privata länk tjänsten.</span><span class="sxs-lookup"><span data-stu-id="395fb-126">The private link service name.</span></span>

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


### <span data-ttu-id="395fb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395fb-127">CommonParameters</span></span>
<span data-ttu-id="395fb-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="395fb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395fb-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="395fb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395fb-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="395fb-130">INPUTS</span></span>

### <span data-ttu-id="395fb-131">System. String</span><span class="sxs-lookup"><span data-stu-id="395fb-131">System.String</span></span>

## <span data-ttu-id="395fb-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="395fb-132">OUTPUTS</span></span>

### <span data-ttu-id="395fb-133">Microsoft. Azure. commands. Networks. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="395fb-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="395fb-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="395fb-134">NOTES</span></span>

## <span data-ttu-id="395fb-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="395fb-135">RELATED LINKS</span></span>

[<span data-ttu-id="395fb-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="395fb-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="395fb-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="395fb-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="395fb-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="395fb-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="395fb-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="395fb-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
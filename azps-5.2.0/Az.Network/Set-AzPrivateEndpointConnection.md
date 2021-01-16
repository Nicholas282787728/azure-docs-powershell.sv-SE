---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400571"
---
# <span data-ttu-id="ba0ae-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ba0ae-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="ba0ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba0ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ba0ae-103">Uppdaterar ett privat slut punkts anslutnings tillstånd i Private Link service.</span><span class="sxs-lookup"><span data-stu-id="ba0ae-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="ba0ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba0ae-104">SYNTAX</span></span>

### <span data-ttu-id="ba0ae-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="ba0ae-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba0ae-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="ba0ae-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba0ae-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba0ae-107">DESCRIPTION</span></span>
<span data-ttu-id="ba0ae-108">Cmdleten **set-AzPrivateEndpointConnection** uppdaterar ett privat slut punkts anslutnings status i en privat länk tjänst</span><span class="sxs-lookup"><span data-stu-id="ba0ae-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="ba0ae-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba0ae-109">EXAMPLES</span></span>

### <span data-ttu-id="ba0ae-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ba0ae-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="ba0ae-111">I det här exemplet uppdateras statusen för en privat slut punkt till godkänd.</span><span class="sxs-lookup"><span data-stu-id="ba0ae-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="ba0ae-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba0ae-112">PARAMETERS</span></span>

### <span data-ttu-id="ba0ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba0ae-113">-DefaultProfile</span></span>
<span data-ttu-id="ba0ae-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ba0ae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba0ae-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ba0ae-115">-Description</span></span>
<span data-ttu-id="ba0ae-116">Skälet till åtgärden.</span><span class="sxs-lookup"><span data-stu-id="ba0ae-116">The reason of action.</span></span>

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

### <span data-ttu-id="ba0ae-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="ba0ae-117">-Name</span></span>
<span data-ttu-id="ba0ae-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="ba0ae-118">The resource name.</span></span>

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

### <span data-ttu-id="ba0ae-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="ba0ae-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="ba0ae-120">Resurs typen privat länk.</span><span class="sxs-lookup"><span data-stu-id="ba0ae-120">The private link resource type.</span></span>

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

### <span data-ttu-id="ba0ae-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="ba0ae-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="ba0ae-122">Godkänd eller avvisad resursen.</span><span class="sxs-lookup"><span data-stu-id="ba0ae-122">Approved or rejected the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba0ae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba0ae-123">-ResourceGroupName</span></span>
<span data-ttu-id="ba0ae-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ba0ae-124">The resource group name.</span></span>

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

### <span data-ttu-id="ba0ae-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba0ae-125">-ResourceId</span></span>
<span data-ttu-id="ba0ae-126">Azure Resource Manager-ID för den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="ba0ae-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="ba0ae-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ba0ae-127">-ServiceName</span></span>
<span data-ttu-id="ba0ae-128">Namnet på den privata länk tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ba0ae-128">The private link service name.</span></span>

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

### <span data-ttu-id="ba0ae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba0ae-129">CommonParameters</span></span>
<span data-ttu-id="ba0ae-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba0ae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba0ae-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba0ae-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba0ae-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba0ae-132">INPUTS</span></span>

### <span data-ttu-id="ba0ae-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ba0ae-133">System.String</span></span>

## <span data-ttu-id="ba0ae-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba0ae-134">OUTPUTS</span></span>

### <span data-ttu-id="ba0ae-135">Microsoft. Azure. commands. Networks. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ba0ae-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="ba0ae-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba0ae-136">NOTES</span></span>

## <span data-ttu-id="ba0ae-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba0ae-137">RELATED LINKS</span></span>

[<span data-ttu-id="ba0ae-138">Godkänn-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ba0ae-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="ba0ae-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ba0ae-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="ba0ae-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ba0ae-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="ba0ae-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ba0ae-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)
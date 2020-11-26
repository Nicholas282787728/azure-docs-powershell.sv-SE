---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 159b320b24ff1e9ab1b4c71e6c374931ecfeffdd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271608"
---
# <span data-ttu-id="df6ab-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="df6ab-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="df6ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="df6ab-103">nekar en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="df6ab-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="df6ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df6ab-104">SYNTAX</span></span>

### <span data-ttu-id="df6ab-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="df6ab-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df6ab-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="df6ab-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df6ab-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df6ab-107">DESCRIPTION</span></span>
<span data-ttu-id="df6ab-108">Cmdleten **Deny-AzPrivateEndpointConnection** nekar en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="df6ab-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="df6ab-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df6ab-109">EXAMPLES</span></span>

### <span data-ttu-id="df6ab-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="df6ab-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="df6ab-111">Det här exemplet nekar en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="df6ab-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="df6ab-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df6ab-112">PARAMETERS</span></span>

### <span data-ttu-id="df6ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df6ab-113">-DefaultProfile</span></span>
<span data-ttu-id="df6ab-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df6ab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df6ab-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="df6ab-115">-Description</span></span>
<span data-ttu-id="df6ab-116">Skälet till åtgärden.</span><span class="sxs-lookup"><span data-stu-id="df6ab-116">The reason of action.</span></span>

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

### <span data-ttu-id="df6ab-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="df6ab-117">-Name</span></span>
<span data-ttu-id="df6ab-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="df6ab-118">The resource name.</span></span>

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

### <span data-ttu-id="df6ab-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="df6ab-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="df6ab-120">Resurs typen privat länk.</span><span class="sxs-lookup"><span data-stu-id="df6ab-120">The private link resource type.</span></span>

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

### <span data-ttu-id="df6ab-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df6ab-121">-ResourceGroupName</span></span>
<span data-ttu-id="df6ab-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="df6ab-122">The resource group name.</span></span>

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

### <span data-ttu-id="df6ab-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df6ab-123">-ResourceId</span></span>
<span data-ttu-id="df6ab-124">Azure Resource Manager-ID för den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="df6ab-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="df6ab-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="df6ab-125">-ServiceName</span></span>
<span data-ttu-id="df6ab-126">Namnet på tjänsten som den privata slut punkts anslutningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="df6ab-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="df6ab-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df6ab-127">CommonParameters</span></span>
<span data-ttu-id="df6ab-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df6ab-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df6ab-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df6ab-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df6ab-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df6ab-130">INPUTS</span></span>

### <span data-ttu-id="df6ab-131">System. String</span><span class="sxs-lookup"><span data-stu-id="df6ab-131">System.String</span></span>

## <span data-ttu-id="df6ab-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df6ab-132">OUTPUTS</span></span>

### <span data-ttu-id="df6ab-133">Microsoft. Azure. commands. Networks. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="df6ab-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="df6ab-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df6ab-134">NOTES</span></span>

## <span data-ttu-id="df6ab-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df6ab-135">RELATED LINKS</span></span>

[<span data-ttu-id="df6ab-136">Godkänn-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="df6ab-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="df6ab-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="df6ab-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="df6ab-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="df6ab-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="df6ab-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="df6ab-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
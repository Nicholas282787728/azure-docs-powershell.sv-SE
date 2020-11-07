---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 4a67914fd3709ef972adac8eba6b1b2fa211fbf6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918553"
---
# <span data-ttu-id="095f5-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="095f5-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="095f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="095f5-102">SYNOPSIS</span></span>
<span data-ttu-id="095f5-103">nekar en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="095f5-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="095f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="095f5-104">SYNTAX</span></span>

### <span data-ttu-id="095f5-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="095f5-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="095f5-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="095f5-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="095f5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="095f5-107">DESCRIPTION</span></span>
<span data-ttu-id="095f5-108">Cmdleten **Deny-AzPrivateEndpointConnection** nekar en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="095f5-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="095f5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="095f5-109">EXAMPLES</span></span>

### <span data-ttu-id="095f5-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="095f5-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="095f5-111">Det här exemplet nekar en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="095f5-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="095f5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="095f5-112">PARAMETERS</span></span>

### <span data-ttu-id="095f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095f5-113">-DefaultProfile</span></span>
<span data-ttu-id="095f5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="095f5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="095f5-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="095f5-115">-Description</span></span>
<span data-ttu-id="095f5-116">Skälet till åtgärden.</span><span class="sxs-lookup"><span data-stu-id="095f5-116">The reason of action.</span></span>

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

### <span data-ttu-id="095f5-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="095f5-117">-Name</span></span>
<span data-ttu-id="095f5-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="095f5-118">The resource name.</span></span>

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

### <span data-ttu-id="095f5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="095f5-119">-ResourceGroupName</span></span>
<span data-ttu-id="095f5-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="095f5-120">The resource group name.</span></span>

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

### <span data-ttu-id="095f5-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="095f5-121">-ResourceId</span></span>
<span data-ttu-id="095f5-122">Azure Resource Manager-ID för den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="095f5-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="095f5-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="095f5-123">-ServiceName</span></span>
<span data-ttu-id="095f5-124">Namnet på den privata länk tjänsten.</span><span class="sxs-lookup"><span data-stu-id="095f5-124">The private link service name.</span></span>

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

### <span data-ttu-id="095f5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095f5-125">CommonParameters</span></span>
<span data-ttu-id="095f5-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095f5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095f5-127">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="095f5-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095f5-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="095f5-128">INPUTS</span></span>

### <span data-ttu-id="095f5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="095f5-129">System.String</span></span>

## <span data-ttu-id="095f5-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="095f5-130">OUTPUTS</span></span>

### <span data-ttu-id="095f5-131">Microsoft. Azure. commands. Networks. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="095f5-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="095f5-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="095f5-132">NOTES</span></span>

## <span data-ttu-id="095f5-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="095f5-133">RELATED LINKS</span></span>

[<span data-ttu-id="095f5-134">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="095f5-134">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="095f5-135">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="095f5-135">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="095f5-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="095f5-136">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)
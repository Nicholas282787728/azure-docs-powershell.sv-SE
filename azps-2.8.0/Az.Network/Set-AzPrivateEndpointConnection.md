---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: 588402480cbd626a747208705ec59fd10c572075
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919493"
---
# <span data-ttu-id="deb4e-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="deb4e-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="deb4e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="deb4e-102">SYNOPSIS</span></span>
<span data-ttu-id="deb4e-103">Uppdaterar ett privat slut punkts anslutnings tillstånd i Private Link service.</span><span class="sxs-lookup"><span data-stu-id="deb4e-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="deb4e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="deb4e-104">SYNTAX</span></span>

```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="deb4e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="deb4e-105">DESCRIPTION</span></span>
<span data-ttu-id="deb4e-106">Cmdleten **set-AzPrivateEndpointConnection** uppdaterar ett privat slut punkts anslutnings status i en privat länk tjänst</span><span class="sxs-lookup"><span data-stu-id="deb4e-106">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="deb4e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="deb4e-107">EXAMPLES</span></span>

### <span data-ttu-id="deb4e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="deb4e-108">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="deb4e-109">I det här exemplet uppdateras statusen för en privat slut punkt till godkänd.</span><span class="sxs-lookup"><span data-stu-id="deb4e-109">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="deb4e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="deb4e-110">PARAMETERS</span></span>

### <span data-ttu-id="deb4e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb4e-111">-DefaultProfile</span></span>
<span data-ttu-id="deb4e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="deb4e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deb4e-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="deb4e-113">-Description</span></span>
<span data-ttu-id="deb4e-114">Skälet till åtgärden.</span><span class="sxs-lookup"><span data-stu-id="deb4e-114">The reason of action.</span></span>

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

### <span data-ttu-id="deb4e-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="deb4e-115">-Name</span></span>
<span data-ttu-id="deb4e-116">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="deb4e-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deb4e-117">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="deb4e-117">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="deb4e-118">Godkänd eller avvisad resursen.</span><span class="sxs-lookup"><span data-stu-id="deb4e-118">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="deb4e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deb4e-119">-ResourceGroupName</span></span>
<span data-ttu-id="deb4e-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="deb4e-120">The resource group name.</span></span>

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

### <span data-ttu-id="deb4e-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="deb4e-121">-ServiceName</span></span>
<span data-ttu-id="deb4e-122">Namnet på den privata länk tjänsten.</span><span class="sxs-lookup"><span data-stu-id="deb4e-122">The private link service name.</span></span>

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

### <span data-ttu-id="deb4e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb4e-123">CommonParameters</span></span>
<span data-ttu-id="deb4e-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deb4e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb4e-125">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="deb4e-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb4e-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="deb4e-126">INPUTS</span></span>

### <span data-ttu-id="deb4e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="deb4e-127">System.String</span></span>

## <span data-ttu-id="deb4e-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="deb4e-128">OUTPUTS</span></span>

### <span data-ttu-id="deb4e-129">Microsoft. Azure. commands. Networks. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="deb4e-129">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="deb4e-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="deb4e-130">NOTES</span></span>

## <span data-ttu-id="deb4e-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="deb4e-131">RELATED LINKS</span></span>

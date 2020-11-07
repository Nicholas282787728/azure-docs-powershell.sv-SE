---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
ms.openlocfilehash: 8669eed6e34b2f03d4da8f1f6490a95e4762241d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919086"
---
# <span data-ttu-id="2310a-101">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="2310a-101">New-AzPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="2310a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2310a-102">SYNOPSIS</span></span>
<span data-ttu-id="2310a-103">Skapar en konfiguration för en privat länks tjänst.</span><span class="sxs-lookup"><span data-stu-id="2310a-103">Creates a private link service connection configuration.</span></span>

## <span data-ttu-id="2310a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2310a-104">SYNTAX</span></span>

### <span data-ttu-id="2310a-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="2310a-105">SetByResource (Default)</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkService <PSPrivateLinkService>
 [-GroupId <String[]>] [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2310a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2310a-106">SetByResourceId</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkServiceId <String> [-GroupId <String[]>]
 [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2310a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2310a-107">DESCRIPTION</span></span>
<span data-ttu-id="2310a-108">Cmdleten **New-AzPrivateLinkServiceConnection** skapar en konfiguration för en privat anslutnings tjänst.</span><span class="sxs-lookup"><span data-stu-id="2310a-108">**The New-AzPrivateLinkServiceConnection** cmdlet creates a private link service connection configuration.</span></span>

## <span data-ttu-id="2310a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2310a-109">EXAMPLES</span></span>

### <span data-ttu-id="2310a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2310a-110">Example 1</span></span>
```
New-AzPrivateLinkServiceConnection -Name MyPLSConnection -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
```

<span data-ttu-id="2310a-111">I det här exemplet skapas ett Connection-objekt för privata länk tjänster i minnet för användning av privat slut punkt.</span><span class="sxs-lookup"><span data-stu-id="2310a-111">This example create a private link service connection object in memory for using in creating private endpoint.</span></span>

## <span data-ttu-id="2310a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2310a-112">PARAMETERS</span></span>

### <span data-ttu-id="2310a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2310a-113">-DefaultProfile</span></span>
<span data-ttu-id="2310a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2310a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2310a-115">-Kund-</span><span class="sxs-lookup"><span data-stu-id="2310a-115">-GroupId</span></span>
<span data-ttu-id="2310a-116">Listan med grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="2310a-116">The list of group id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2310a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2310a-117">-Name</span></span>
<span data-ttu-id="2310a-118">Namnet på den privata länk tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2310a-118">The name of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2310a-119">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2310a-119">-PrivateLinkService</span></span>
<span data-ttu-id="2310a-120">Den privata länk tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2310a-120">The private link service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2310a-121">-PrivateLinkServiceId</span><span class="sxs-lookup"><span data-stu-id="2310a-121">-PrivateLinkServiceId</span></span>
<span data-ttu-id="2310a-122">ID för Private Link service.</span><span class="sxs-lookup"><span data-stu-id="2310a-122">The id of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2310a-123">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="2310a-123">-RequestMessage</span></span>
<span data-ttu-id="2310a-124">Begäran.</span><span class="sxs-lookup"><span data-stu-id="2310a-124">The request message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2310a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2310a-125">CommonParameters</span></span>
<span data-ttu-id="2310a-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2310a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2310a-127">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2310a-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2310a-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2310a-128">INPUTS</span></span>

### <span data-ttu-id="2310a-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="2310a-129">None</span></span>

## <span data-ttu-id="2310a-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2310a-130">OUTPUTS</span></span>

### <span data-ttu-id="2310a-131">Microsoft. Azure. commands. Networks. Models. PSPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="2310a-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="2310a-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2310a-132">NOTES</span></span>

## <span data-ttu-id="2310a-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2310a-133">RELATED LINKS</span></span>

[<span data-ttu-id="2310a-134">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2310a-134">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)
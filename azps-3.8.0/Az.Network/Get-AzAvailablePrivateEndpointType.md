---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: c0bc2b5a14fd8e3dee8694a8564e831c0f39a229
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926017"
---
# <span data-ttu-id="fe3b0-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="fe3b0-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="fe3b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe3b0-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3b0-103">Returnera tillgängliga privata slut punkts typer på platsen.</span><span class="sxs-lookup"><span data-stu-id="fe3b0-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="fe3b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe3b0-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe3b0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe3b0-105">DESCRIPTION</span></span>
<span data-ttu-id="fe3b0-106">Cmdleten **Get-AzAvailablePrivateEndpointType** returnerar alla tillgängliga privata slut punkts typer på platsen.</span><span class="sxs-lookup"><span data-stu-id="fe3b0-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="fe3b0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe3b0-107">EXAMPLES</span></span>

### <span data-ttu-id="fe3b0-108">Exempel</span><span class="sxs-lookup"><span data-stu-id="fe3b0-108">Example</span></span>
```
Get-AzAvailablePrivateEndpointType -Location eastus

[
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename1",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Sql/servers"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename2",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Storage/accounts"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename3",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Cosmos/cosmosDbAccounts"
  }
]
```

<span data-ttu-id="fe3b0-109">I det här exemplet returneras alla tillgängliga privata slut punkts typer på platsen.</span><span class="sxs-lookup"><span data-stu-id="fe3b0-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="fe3b0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe3b0-110">PARAMETERS</span></span>

### <span data-ttu-id="fe3b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3b0-111">-DefaultProfile</span></span>
<span data-ttu-id="fe3b0-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe3b0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe3b0-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="fe3b0-113">-Location</span></span>
<span data-ttu-id="fe3b0-114">Platsen.</span><span class="sxs-lookup"><span data-stu-id="fe3b0-114">The location.</span></span>

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

### <span data-ttu-id="fe3b0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe3b0-115">-ResourceGroupName</span></span>
<span data-ttu-id="fe3b0-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="fe3b0-116">The resource group name.</span></span>

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

### <span data-ttu-id="fe3b0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3b0-117">CommonParameters</span></span>
<span data-ttu-id="fe3b0-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe3b0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3b0-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe3b0-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3b0-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe3b0-120">INPUTS</span></span>

### <span data-ttu-id="fe3b0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="fe3b0-121">System.String</span></span>

## <span data-ttu-id="fe3b0-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe3b0-122">OUTPUTS</span></span>

### <span data-ttu-id="fe3b0-123">Microsoft. Azure. commands. Networks. Models. PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="fe3b0-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="fe3b0-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe3b0-124">NOTES</span></span>

## <span data-ttu-id="fe3b0-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe3b0-125">RELATED LINKS</span></span>

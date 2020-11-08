---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: 1ca9e604a1371d83fdedd2986534fa8926b6286b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273194"
---
# <span data-ttu-id="8aef9-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8aef9-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="8aef9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8aef9-102">SYNOPSIS</span></span>
<span data-ttu-id="8aef9-103">Returnera tillgängliga privata slut punkts typer på platsen.</span><span class="sxs-lookup"><span data-stu-id="8aef9-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="8aef9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8aef9-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8aef9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8aef9-105">DESCRIPTION</span></span>
<span data-ttu-id="8aef9-106">Cmdleten **Get-AzAvailablePrivateEndpointType** returnerar alla tillgängliga privata slut punkts typer på platsen.</span><span class="sxs-lookup"><span data-stu-id="8aef9-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="8aef9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8aef9-107">EXAMPLES</span></span>

### <span data-ttu-id="8aef9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8aef9-108">Example 1</span></span>
```powershell
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

<span data-ttu-id="8aef9-109">I det här exemplet returneras alla tillgängliga privata slut punkts typer på platsen.</span><span class="sxs-lookup"><span data-stu-id="8aef9-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="8aef9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8aef9-110">PARAMETERS</span></span>

### <span data-ttu-id="8aef9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aef9-111">-DefaultProfile</span></span>
<span data-ttu-id="8aef9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8aef9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8aef9-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="8aef9-113">-Location</span></span>
<span data-ttu-id="8aef9-114">Platsen.</span><span class="sxs-lookup"><span data-stu-id="8aef9-114">The location.</span></span>

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

### <span data-ttu-id="8aef9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aef9-115">-ResourceGroupName</span></span>
<span data-ttu-id="8aef9-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="8aef9-116">The resource group name.</span></span>

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

### <span data-ttu-id="8aef9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aef9-117">CommonParameters</span></span>
<span data-ttu-id="8aef9-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aef9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aef9-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8aef9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aef9-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8aef9-120">INPUTS</span></span>

### <span data-ttu-id="8aef9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="8aef9-121">System.String</span></span>

## <span data-ttu-id="8aef9-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8aef9-122">OUTPUTS</span></span>

### <span data-ttu-id="8aef9-123">Microsoft. Azure. commands. Networks. Models. PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8aef9-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="8aef9-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8aef9-124">NOTES</span></span>

## <span data-ttu-id="8aef9-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8aef9-125">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: e4d9b8cd09aa1bf1528de1cd2179a76e7907e82b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323693"
---
# <span data-ttu-id="a072d-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="a072d-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="a072d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a072d-102">SYNOPSIS</span></span>
<span data-ttu-id="a072d-103">Skapar ett StaticRoute-objekt som sedan kan läggas till i ett RoutingConfiguration-objekt.</span><span class="sxs-lookup"><span data-stu-id="a072d-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="a072d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a072d-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a072d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a072d-105">DESCRIPTION</span></span>
<span data-ttu-id="a072d-106">Skapar ett StaticRoute-objekt.</span><span class="sxs-lookup"><span data-stu-id="a072d-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="a072d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a072d-107">EXAMPLES</span></span>

### <span data-ttu-id="a072d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a072d-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="a072d-109">Med kommandot ovan skapas ett StaticRoute-objekt som sedan kan läggas till i ett RoutingConfiguration-objekt.</span><span class="sxs-lookup"><span data-stu-id="a072d-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="a072d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a072d-110">PARAMETERS</span></span>

### <span data-ttu-id="a072d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a072d-111">-DefaultProfile</span></span>
<span data-ttu-id="a072d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a072d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a072d-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a072d-113">-AddressPrefix</span></span>
<span data-ttu-id="a072d-114">Lista med adressprefix.</span><span class="sxs-lookup"><span data-stu-id="a072d-114">List of address prefixes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a072d-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="a072d-115">-Name</span></span>
<span data-ttu-id="a072d-116">Vägens namn.</span><span class="sxs-lookup"><span data-stu-id="a072d-116">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a072d-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="a072d-117">-NextHopIpAddress</span></span>
<span data-ttu-id="a072d-118">Nästa hopp-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="a072d-118">The next hop ip address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a072d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a072d-119">CommonParameters</span></span>
<span data-ttu-id="a072d-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a072d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a072d-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a072d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a072d-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a072d-122">INPUTS</span></span>

### <span data-ttu-id="a072d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a072d-123">System.String</span></span>

## <span data-ttu-id="a072d-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a072d-124">OUTPUTS</span></span>

### <span data-ttu-id="a072d-125">Microsoft. Azure. commands. Networks. Models. PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="a072d-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="a072d-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a072d-126">NOTES</span></span>

## <span data-ttu-id="a072d-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a072d-127">RELATED LINKS</span></span>

[<span data-ttu-id="a072d-128">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="a072d-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
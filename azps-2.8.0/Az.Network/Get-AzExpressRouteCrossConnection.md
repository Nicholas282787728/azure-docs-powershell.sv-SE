---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: c15a8b57338a6c5e7c2f054e07a0d26d716627fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918762"
---
# <span data-ttu-id="d5384-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d5384-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="d5384-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5384-102">SYNOPSIS</span></span>
<span data-ttu-id="d5384-103">Får en Azure ExpressRoute-kors anslutning från Azure.</span><span class="sxs-lookup"><span data-stu-id="d5384-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="d5384-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5384-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5384-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5384-105">DESCRIPTION</span></span>
<span data-ttu-id="d5384-106">Cmdleten **Get-AzExpressRouteCrossConnection** används för att hämta ett ExpressRoute-kors anslutnings objekt från din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="d5384-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="d5384-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d5384-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="d5384-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5384-108">EXAMPLES</span></span>

### <span data-ttu-id="d5384-109">Exempel 1: få ExpressRoute kors koppling</span><span class="sxs-lookup"><span data-stu-id="d5384-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="d5384-110">Exempel 2: Visa en lista över ExpressRoute-kors kopplingar med hjälp av ett filter</span><span class="sxs-lookup"><span data-stu-id="d5384-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="d5384-111">Denna cmdlet visar alla ExpressRoute-kors anslutningar som börjar med "test"</span><span class="sxs-lookup"><span data-stu-id="d5384-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="d5384-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5384-112">PARAMETERS</span></span>

### <span data-ttu-id="d5384-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5384-113">-DefaultProfile</span></span>
<span data-ttu-id="d5384-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5384-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5384-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d5384-115">-Name</span></span>
<span data-ttu-id="d5384-116">Namnet på ExpressRoute-kors anslutningen.</span><span class="sxs-lookup"><span data-stu-id="d5384-116">The name of the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d5384-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5384-117">-ResourceGroupName</span></span>
<span data-ttu-id="d5384-118">Namnet på den resurs grupp som innehåller ExpressRoute-kors anslutningen.</span><span class="sxs-lookup"><span data-stu-id="d5384-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d5384-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5384-119">CommonParameters</span></span>
<span data-ttu-id="d5384-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5384-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5384-121">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5384-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5384-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5384-122">INPUTS</span></span>

### <span data-ttu-id="d5384-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="d5384-123">None</span></span>
<span data-ttu-id="d5384-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d5384-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d5384-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5384-125">OUTPUTS</span></span>

### <span data-ttu-id="d5384-126">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d5384-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="d5384-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5384-127">NOTES</span></span>

## <span data-ttu-id="d5384-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5384-128">RELATED LINKS</span></span>

[<span data-ttu-id="d5384-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d5384-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
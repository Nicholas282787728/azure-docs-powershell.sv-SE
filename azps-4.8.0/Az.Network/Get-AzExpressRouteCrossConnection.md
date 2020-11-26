---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: a6a3b973a893e3588b5df77700318a725bde11b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258826"
---
# <span data-ttu-id="16a6e-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="16a6e-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="16a6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="16a6e-103">Får en Azure ExpressRoute-kors anslutning från Azure.</span><span class="sxs-lookup"><span data-stu-id="16a6e-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="16a6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16a6e-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16a6e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16a6e-105">DESCRIPTION</span></span>
<span data-ttu-id="16a6e-106">Cmdleten **Get-AzExpressRouteCrossConnection** används för att hämta ett ExpressRoute-kors anslutnings objekt från din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="16a6e-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="16a6e-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="16a6e-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="16a6e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16a6e-108">EXAMPLES</span></span>

### <span data-ttu-id="16a6e-109">Exempel 1: få ExpressRoute kors koppling</span><span class="sxs-lookup"><span data-stu-id="16a6e-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="16a6e-110">Exempel 2: Visa en lista över ExpressRoute-kors kopplingar med hjälp av ett filter</span><span class="sxs-lookup"><span data-stu-id="16a6e-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="16a6e-111">Denna cmdlet visar alla ExpressRoute-kors anslutningar som börjar med "test"</span><span class="sxs-lookup"><span data-stu-id="16a6e-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="16a6e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16a6e-112">PARAMETERS</span></span>

### <span data-ttu-id="16a6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16a6e-113">-DefaultProfile</span></span>
<span data-ttu-id="16a6e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16a6e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16a6e-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="16a6e-115">-Name</span></span>
<span data-ttu-id="16a6e-116">Namnet på ExpressRoute-kors anslutningen.</span><span class="sxs-lookup"><span data-stu-id="16a6e-116">The name of the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="16a6e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16a6e-117">-ResourceGroupName</span></span>
<span data-ttu-id="16a6e-118">Namnet på den resurs grupp som innehåller ExpressRoute-kors anslutningen.</span><span class="sxs-lookup"><span data-stu-id="16a6e-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="16a6e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16a6e-119">CommonParameters</span></span>
<span data-ttu-id="16a6e-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16a6e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16a6e-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16a6e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16a6e-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16a6e-122">INPUTS</span></span>

### <span data-ttu-id="16a6e-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="16a6e-123">None</span></span>
<span data-ttu-id="16a6e-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="16a6e-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16a6e-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16a6e-125">OUTPUTS</span></span>

### <span data-ttu-id="16a6e-126">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="16a6e-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="16a6e-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16a6e-127">NOTES</span></span>

## <span data-ttu-id="16a6e-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16a6e-128">RELATED LINKS</span></span>

[<span data-ttu-id="16a6e-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="16a6e-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
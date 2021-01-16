---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396312"
---
# <span data-ttu-id="bd0e3-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="bd0e3-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="bd0e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd0e3-102">SYNOPSIS</span></span>
<span data-ttu-id="bd0e3-103">Hämtar de platser där ExpressRoutePort resurser är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="bd0e3-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="bd0e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd0e3-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd0e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd0e3-105">DESCRIPTION</span></span>
<span data-ttu-id="bd0e3-106">Cmdleten **Get-AzExpressRoutePortsLocation** används för att hämta platserna där ExpressRoutePort-resurser finns tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="bd0e3-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="bd0e3-107">Med en viss plats som inmatning visar cmdleten informationen om den platsen, till exempel en lista över tillgängliga bandbredder på den platsen.</span><span class="sxs-lookup"><span data-stu-id="bd0e3-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="bd0e3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd0e3-108">EXAMPLES</span></span>

### <span data-ttu-id="bd0e3-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bd0e3-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="bd0e3-110">Här listas de platser där ExpressRoutePort resurser är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="bd0e3-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="bd0e3-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bd0e3-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="bd0e3-112">Visar en lista över ExpressRoutePort-bandbredderna på plats $loc.</span><span class="sxs-lookup"><span data-stu-id="bd0e3-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="bd0e3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd0e3-113">PARAMETERS</span></span>

### <span data-ttu-id="bd0e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd0e3-114">-DefaultProfile</span></span>
<span data-ttu-id="bd0e3-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd0e3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd0e3-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="bd0e3-116">-LocationName</span></span>
<span data-ttu-id="bd0e3-117">Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="bd0e3-117">The name of the location.</span></span>

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

### <span data-ttu-id="bd0e3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd0e3-118">CommonParameters</span></span>
<span data-ttu-id="bd0e3-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd0e3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd0e3-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd0e3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd0e3-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd0e3-121">INPUTS</span></span>

### <span data-ttu-id="bd0e3-122">System. String</span><span class="sxs-lookup"><span data-stu-id="bd0e3-122">System.String</span></span>

## <span data-ttu-id="bd0e3-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd0e3-123">OUTPUTS</span></span>

### <span data-ttu-id="bd0e3-124">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="bd0e3-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="bd0e3-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd0e3-125">NOTES</span></span>

## <span data-ttu-id="bd0e3-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd0e3-126">RELATED LINKS</span></span>

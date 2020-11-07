---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
ms.openlocfilehash: 5d077991e42da0709019df1dccdd83f03659ca49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757852"
---
# <span data-ttu-id="98a42-101">Get-AzureRmExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="98a42-101">Get-AzureRmExpressRoutePortsLocation</span></span>

## <span data-ttu-id="98a42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98a42-102">SYNOPSIS</span></span>
<span data-ttu-id="98a42-103">Hämtar de platser där ExpressRoutePort resurser är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="98a42-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98a42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98a42-104">SYNTAX</span></span>

```
Get-AzureRmExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98a42-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98a42-105">DESCRIPTION</span></span>
<span data-ttu-id="98a42-106">Cmdleten **Get-AzureRmExpressRoutePortsLocation** används för att hämta platserna där ExpressRoutePort-resurser finns tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="98a42-106">The **Get-AzureRmExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="98a42-107">Med en viss plats som inmatning visar cmdleten informationen om den platsen, till exempel en lista över tillgängliga bandbredder på den platsen.</span><span class="sxs-lookup"><span data-stu-id="98a42-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>


## <span data-ttu-id="98a42-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98a42-108">EXAMPLES</span></span>

### <span data-ttu-id="98a42-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="98a42-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation
```

<span data-ttu-id="98a42-110">Här listas de platser där ExpressRoutePort resurser är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="98a42-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="98a42-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="98a42-111">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="98a42-112">Visar en lista över ExpressRoutePort-bandbredderna på plats $loc.</span><span class="sxs-lookup"><span data-stu-id="98a42-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="98a42-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98a42-113">PARAMETERS</span></span>

### <span data-ttu-id="98a42-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a42-114">-DefaultProfile</span></span>
<span data-ttu-id="98a42-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98a42-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a42-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="98a42-116">-LocationName</span></span>
<span data-ttu-id="98a42-117">Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="98a42-117">The name of the location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98a42-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a42-118">CommonParameters</span></span>
<span data-ttu-id="98a42-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98a42-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a42-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98a42-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a42-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98a42-121">INPUTS</span></span>

### <span data-ttu-id="98a42-122">System. String</span><span class="sxs-lookup"><span data-stu-id="98a42-122">System.String</span></span>

## <span data-ttu-id="98a42-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98a42-123">OUTPUTS</span></span>

### <span data-ttu-id="98a42-124">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="98a42-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="98a42-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98a42-125">NOTES</span></span>

## <span data-ttu-id="98a42-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98a42-126">RELATED LINKS</span></span>

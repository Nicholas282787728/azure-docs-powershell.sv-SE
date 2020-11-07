---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
ms.openlocfilehash: 83ee8e673271079690c24691f22badfe5193ba50
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929830"
---
# <span data-ttu-id="75dad-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="75dad-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="75dad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75dad-102">SYNOPSIS</span></span>
<span data-ttu-id="75dad-103">Hämtar alla tillgängliga regel uppsättningar för webb programs brand väggar.</span><span class="sxs-lookup"><span data-stu-id="75dad-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75dad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75dad-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75dad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75dad-105">DESCRIPTION</span></span>
<span data-ttu-id="75dad-106">Cmdleten **Get-AzureRmApplicationGatewayAvailableWafRuleSets** hämtar alla tillgängliga regel uppsättningar för webb program brand väggar.</span><span class="sxs-lookup"><span data-stu-id="75dad-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="75dad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75dad-107">EXAMPLES</span></span>

### <span data-ttu-id="75dad-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="75dad-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="75dad-109">Det här kommandot returnerar alla tillgängliga regel uppsättningar för webb program brand väggar.</span><span class="sxs-lookup"><span data-stu-id="75dad-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="75dad-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75dad-110">PARAMETERS</span></span>

### <span data-ttu-id="75dad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75dad-111">-DefaultProfile</span></span>
<span data-ttu-id="75dad-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75dad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75dad-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75dad-113">CommonParameters</span></span>
<span data-ttu-id="75dad-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75dad-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75dad-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75dad-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75dad-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75dad-116">INPUTS</span></span>

### <span data-ttu-id="75dad-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="75dad-117">None</span></span>

## <span data-ttu-id="75dad-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75dad-118">OUTPUTS</span></span>

### <span data-ttu-id="75dad-119">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="75dad-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="75dad-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75dad-120">NOTES</span></span>
<span data-ttu-id="75dad-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** är ett alias för cmdleten **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .</span><span class="sxs-lookup"><span data-stu-id="75dad-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="75dad-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75dad-122">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 2b470a9837fafbb20d2e83f6fa9e7b4308b12d3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919360"
---
# <span data-ttu-id="862ee-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="862ee-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="862ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="862ee-102">SYNOPSIS</span></span>
<span data-ttu-id="862ee-103">Hämta katalogen med tillgängliga reservationer</span><span class="sxs-lookup"><span data-stu-id="862ee-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="862ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="862ee-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="862ee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="862ee-105">DESCRIPTION</span></span>
<span data-ttu-id="862ee-106">Skaffa de regioner och SKU: er som är tillgängliga för reserverade instans köp för det angivna Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="862ee-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="862ee-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="862ee-107">EXAMPLES</span></span>

### <span data-ttu-id="862ee-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="862ee-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="862ee-109">Hämta VirtualMachines-katalogen i väst för standard abonnemanget</span><span class="sxs-lookup"><span data-stu-id="862ee-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="862ee-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="862ee-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="862ee-111">Hämta SuseLinux-katalogen för det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="862ee-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="862ee-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="862ee-112">PARAMETERS</span></span>

### <span data-ttu-id="862ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="862ee-113">-DefaultProfile</span></span>
<span data-ttu-id="862ee-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="862ee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="862ee-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="862ee-115">-Location</span></span>
<span data-ttu-id="862ee-116">Anger platsen för de reserverade resurserna i katalogen</span><span class="sxs-lookup"><span data-stu-id="862ee-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="862ee-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="862ee-117">-ReservedResourceType</span></span>
<span data-ttu-id="862ee-118">Anger typen för de reserverade resurserna i katalogen</span><span class="sxs-lookup"><span data-stu-id="862ee-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="862ee-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="862ee-119">-SubscriptionId</span></span>
<span data-ttu-id="862ee-120">ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="862ee-120">Id of the subscription</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862ee-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="862ee-121">CommonParameters</span></span>
<span data-ttu-id="862ee-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="862ee-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="862ee-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="862ee-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="862ee-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="862ee-124">INPUTS</span></span>

### <span data-ttu-id="862ee-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="862ee-125">None</span></span>

## <span data-ttu-id="862ee-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="862ee-126">OUTPUTS</span></span>

### <span data-ttu-id="862ee-127">Microsoft. Azure. commands. reservations. Models. PSCatalog</span><span class="sxs-lookup"><span data-stu-id="862ee-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="862ee-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="862ee-128">NOTES</span></span>

## <span data-ttu-id="862ee-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="862ee-129">RELATED LINKS</span></span>
---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F4BADE88-28A2-42FB-9578-93D65148709E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f73e47ec25d44d3965279066de98585ae2cbaee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099219"
---
# <span data-ttu-id="5affb-101">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="5affb-101">New-AzureRouteTable</span></span>

## <span data-ttu-id="5affb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5affb-102">SYNOPSIS</span></span>
<span data-ttu-id="5affb-103">Skapar en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="5affb-103">Creates a route table.</span></span>

## <span data-ttu-id="5affb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5affb-104">SYNTAX</span></span>

```
New-AzureRouteTable -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5affb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5affb-105">DESCRIPTION</span></span>
<span data-ttu-id="5affb-106">Cmdleten **New-AzureRouteTable** skapar en routningstabell på en angiven plats.</span><span class="sxs-lookup"><span data-stu-id="5affb-106">The **New-AzureRouteTable** cmdlet creates a route table in a specified location.</span></span>
<span data-ttu-id="5affb-107">Du kan lägga till användardefinierade vägar i routningstabellen.</span><span class="sxs-lookup"><span data-stu-id="5affb-107">You can add user-defined routes to the route table.</span></span>
<span data-ttu-id="5affb-108">Du kan koppla väg tabellen till ett undernät i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="5affb-108">You can associate the route table to a subnet in a virtual network.</span></span>

## <span data-ttu-id="5affb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5affb-109">EXAMPLES</span></span>

## <span data-ttu-id="5affb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5affb-110">PARAMETERS</span></span>

### <span data-ttu-id="5affb-111">-Etikett</span><span class="sxs-lookup"><span data-stu-id="5affb-111">-Label</span></span>
<span data-ttu-id="5affb-112">Anger en beskrivning för den nya routningstabellen.</span><span class="sxs-lookup"><span data-stu-id="5affb-112">Specifies a description for the new route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5affb-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="5affb-113">-Location</span></span>
<span data-ttu-id="5affb-114">Anger den plats där den här cmdleten skapar routningstabellen.</span><span class="sxs-lookup"><span data-stu-id="5affb-114">Specifies the location in which this cmdlet creates the route table.</span></span>

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

### <span data-ttu-id="5affb-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="5affb-115">-Name</span></span>
<span data-ttu-id="5affb-116">Anger ett namn för väg tabellen som skapas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5affb-116">Specifies a name for the route table that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5affb-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="5affb-117">-Profile</span></span>
<span data-ttu-id="5affb-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="5affb-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="5affb-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="5affb-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5affb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5affb-120">CommonParameters</span></span>
<span data-ttu-id="5affb-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5affb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5affb-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5affb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5affb-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5affb-123">INPUTS</span></span>

## <span data-ttu-id="5affb-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5affb-124">OUTPUTS</span></span>

## <span data-ttu-id="5affb-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5affb-125">NOTES</span></span>

## <span data-ttu-id="5affb-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5affb-126">RELATED LINKS</span></span>

[<span data-ttu-id="5affb-127">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="5affb-127">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="5affb-128">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="5affb-128">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)



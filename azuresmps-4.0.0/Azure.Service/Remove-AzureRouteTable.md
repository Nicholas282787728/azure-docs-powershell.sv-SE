---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 58329D8A-CB54-46FB-84A7-C31F00C13827
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6333430682de7693b6b87f9d037dea66725bfed8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099362"
---
# <span data-ttu-id="42b41-101">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="42b41-101">Remove-AzureRouteTable</span></span>

## <span data-ttu-id="42b41-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42b41-102">SYNOPSIS</span></span>
<span data-ttu-id="42b41-103">Tar bort en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="42b41-103">Removes a route table.</span></span>

## <span data-ttu-id="42b41-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42b41-104">SYNTAX</span></span>

```
Remove-AzureRouteTable -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="42b41-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42b41-105">DESCRIPTION</span></span>
<span data-ttu-id="42b41-106">Cmdleten **Remove-AzureRouteTable** tar bort en routningstabell från din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="42b41-106">The **Remove-AzureRouteTable** cmdlet removes a route table from your subscription.</span></span>
<span data-ttu-id="42b41-107">Om en routningstabell är kopplad till ett undernät kan du inte ta bort tabellen.</span><span class="sxs-lookup"><span data-stu-id="42b41-107">If a route table is associated to a subnet, you cannot remove the table.</span></span>

## <span data-ttu-id="42b41-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42b41-108">EXAMPLES</span></span>

### <span data-ttu-id="42b41-109">Exempel 1: ta bort en routningstabellen</span><span class="sxs-lookup"><span data-stu-id="42b41-109">Example 1: Remove a route table</span></span>
```
PS C:\> Remove-AzureRouteTable -Name "PublicRouteTable"
```

<span data-ttu-id="42b41-110">Det här kommandot tar bort routningstabellen som heter PublicRouteTable.</span><span class="sxs-lookup"><span data-stu-id="42b41-110">This command removes the route table named PublicRouteTable.</span></span>

## <span data-ttu-id="42b41-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42b41-111">PARAMETERS</span></span>

### <span data-ttu-id="42b41-112">-Force</span><span class="sxs-lookup"><span data-stu-id="42b41-112">-Force</span></span>
<span data-ttu-id="42b41-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="42b41-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b41-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="42b41-114">-Name</span></span>
<span data-ttu-id="42b41-115">Anger namnet på den routningstabell som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="42b41-115">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b41-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42b41-116">-PassThru</span></span>
<span data-ttu-id="42b41-117">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="42b41-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="42b41-118">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="42b41-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b41-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="42b41-119">-Profile</span></span>
<span data-ttu-id="42b41-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="42b41-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="42b41-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="42b41-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="42b41-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b41-122">CommonParameters</span></span>
<span data-ttu-id="42b41-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42b41-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b41-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42b41-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b41-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42b41-125">INPUTS</span></span>

## <span data-ttu-id="42b41-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42b41-126">OUTPUTS</span></span>

## <span data-ttu-id="42b41-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42b41-127">NOTES</span></span>

## <span data-ttu-id="42b41-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42b41-128">RELATED LINKS</span></span>

[<span data-ttu-id="42b41-129">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="42b41-129">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="42b41-130">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="42b41-130">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

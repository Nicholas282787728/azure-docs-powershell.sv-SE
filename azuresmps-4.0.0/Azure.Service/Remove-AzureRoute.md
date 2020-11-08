---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5C8A79D1-32D4-4B30-AAC8-C6EF3B68017E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c2f695022e3a03d90443ad9ac2eb36ef8cb22ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099365"
---
# <span data-ttu-id="c392b-101">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="c392b-101">Remove-AzureRoute</span></span>

## <span data-ttu-id="c392b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c392b-102">SYNOPSIS</span></span>
<span data-ttu-id="c392b-103">Tar bort en väg från en route-tabell.</span><span class="sxs-lookup"><span data-stu-id="c392b-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="c392b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c392b-104">SYNTAX</span></span>

```
Remove-AzureRoute -RouteName <String> [-Force] -RouteTable <IRouteTable> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c392b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c392b-105">DESCRIPTION</span></span>
<span data-ttu-id="c392b-106">Cmdleten **Remove-AzureRoute** tar bort en väg från en route-tabell.</span><span class="sxs-lookup"><span data-stu-id="c392b-106">The **Remove-AzureRoute** cmdlet removes a route from a route table.</span></span>

## <span data-ttu-id="c392b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c392b-107">EXAMPLES</span></span>

### <span data-ttu-id="c392b-108">Exempel 1: ta bort en väg</span><span class="sxs-lookup"><span data-stu-id="c392b-108">Example 1: Remove a route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Remove-AzureRoute -RouteName "InternetRoute"
Confirm
Are you sure you want to remove the Route "InternetRoute" from Route Table "ApplianceRouteTable"?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="c392b-109">Det här kommandot får en routningstabell med namnet ApplianceRouteTable.</span><span class="sxs-lookup"><span data-stu-id="c392b-109">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="c392b-110">Kommandot skickar den väg tabellen till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c392b-110">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="c392b-111">Den aktuella cmdleten tar bort en väg som heter InternetRoute.</span><span class="sxs-lookup"><span data-stu-id="c392b-111">The current cmdlet removes a route named InternetRoute.</span></span>

## <span data-ttu-id="c392b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c392b-112">PARAMETERS</span></span>

### <span data-ttu-id="c392b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c392b-113">-Force</span></span>
<span data-ttu-id="c392b-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c392b-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c392b-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="c392b-115">-Profile</span></span>
<span data-ttu-id="c392b-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c392b-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c392b-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c392b-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c392b-118">-RouteName</span><span class="sxs-lookup"><span data-stu-id="c392b-118">-RouteName</span></span>
<span data-ttu-id="c392b-119">Anger ett namn för den nya vägen som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c392b-119">Specifies a name for the new route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c392b-120">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c392b-120">-RouteTable</span></span>
<span data-ttu-id="c392b-121">Anger den routningstabell som den här cmdleten tar bort en väg från.</span><span class="sxs-lookup"><span data-stu-id="c392b-121">Specifies the route table from which this cmdlet removes a route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c392b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c392b-122">CommonParameters</span></span>
<span data-ttu-id="c392b-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c392b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c392b-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c392b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c392b-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c392b-125">INPUTS</span></span>

## <span data-ttu-id="c392b-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c392b-126">OUTPUTS</span></span>

## <span data-ttu-id="c392b-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c392b-127">NOTES</span></span>

## <span data-ttu-id="c392b-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c392b-128">RELATED LINKS</span></span>

[<span data-ttu-id="c392b-129">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="c392b-129">Set-AzureRoute</span></span>](./Set-AzureRoute.md)



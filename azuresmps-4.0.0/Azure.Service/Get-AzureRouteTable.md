---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7F8C2223-5F82-4E4E-8057-44B72F7D5803
online version: ''
schema: 2.0.0
ms.openlocfilehash: a02d80d46696ff635da95c6bc29875f697f65fd4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099543"
---
# <span data-ttu-id="880f8-101">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="880f8-101">Get-AzureRouteTable</span></span>

## <span data-ttu-id="880f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="880f8-102">SYNOPSIS</span></span>
<span data-ttu-id="880f8-103">Hämtar en väg tabell.</span><span class="sxs-lookup"><span data-stu-id="880f8-103">Gets a route table.</span></span>

## <span data-ttu-id="880f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="880f8-104">SYNTAX</span></span>

```
Get-AzureRouteTable [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="880f8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="880f8-105">DESCRIPTION</span></span>
<span data-ttu-id="880f8-106">Cmdleten **Get-AzureRouteTable** hämtar en route-tabell.</span><span class="sxs-lookup"><span data-stu-id="880f8-106">The **Get-AzureRouteTable** cmdlet gets a route table.</span></span>
<span data-ttu-id="880f8-107">Ange en *detaljerad* parameter för att Visa vägarna i routningstabellen.</span><span class="sxs-lookup"><span data-stu-id="880f8-107">Specify the *Detailed* parameter to list the routes in the route table.</span></span>

## <span data-ttu-id="880f8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="880f8-108">EXAMPLES</span></span>

### <span data-ttu-id="880f8-109">Exempel 1: få information om en routningstabell</span><span class="sxs-lookup"><span data-stu-id="880f8-109">Example 1: Get details of a route table</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    ApplianceRouteTable           Central US                    Appliance Route Table
```

<span data-ttu-id="880f8-110">Det här kommandot får information om en routningstabell som heter ApplianceRouteTable.</span><span class="sxs-lookup"><span data-stu-id="880f8-110">This command gets the details of a route table named ApplianceRouteTable.</span></span>

## <span data-ttu-id="880f8-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="880f8-111">PARAMETERS</span></span>

### <span data-ttu-id="880f8-112">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="880f8-112">-Detailed</span></span>
<span data-ttu-id="880f8-113">Anger att vägarna i routningstabellen visas i den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="880f8-113">Indicates that this cmdlet displays the routes in the route table.</span></span>

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

### <span data-ttu-id="880f8-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="880f8-114">-Name</span></span>
<span data-ttu-id="880f8-115">Anger namnet på den routningstabell som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="880f8-115">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="880f8-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="880f8-116">-Profile</span></span>
<span data-ttu-id="880f8-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="880f8-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="880f8-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="880f8-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="880f8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="880f8-119">CommonParameters</span></span>
<span data-ttu-id="880f8-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="880f8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="880f8-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="880f8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="880f8-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="880f8-122">INPUTS</span></span>

## <span data-ttu-id="880f8-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="880f8-123">OUTPUTS</span></span>

## <span data-ttu-id="880f8-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="880f8-124">NOTES</span></span>

## <span data-ttu-id="880f8-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="880f8-125">RELATED LINKS</span></span>

[<span data-ttu-id="880f8-126">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="880f8-126">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="880f8-127">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="880f8-127">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)



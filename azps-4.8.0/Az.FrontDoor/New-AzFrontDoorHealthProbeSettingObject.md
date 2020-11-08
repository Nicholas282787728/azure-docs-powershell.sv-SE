---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262670"
---
# <span data-ttu-id="d1334-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="d1334-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="d1334-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1334-102">SYNOPSIS</span></span>
<span data-ttu-id="d1334-103">Skapa ett PSHealthProbeSetting-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="d1334-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="d1334-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1334-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1334-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1334-105">DESCRIPTION</span></span>
<span data-ttu-id="d1334-106">Skapa ett PSHealthProbeSetting-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="d1334-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="d1334-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1334-107">EXAMPLES</span></span>

### <span data-ttu-id="d1334-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d1334-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
HealthProbeMethod : Head
EnabledState      : Enabled
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="d1334-109">Obs! HealthProbeMethod inställning är inte Skift läges känslig.</span><span class="sxs-lookup"><span data-stu-id="d1334-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="d1334-110">Skapa ett PSHealthProbeSetting-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="d1334-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="d1334-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1334-111">PARAMETERS</span></span>

### <span data-ttu-id="d1334-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1334-112">-DefaultProfile</span></span>
<span data-ttu-id="d1334-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1334-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1334-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="d1334-114">-EnabledState</span></span>
<span data-ttu-id="d1334-115">Om hälso avsökningar ska aktive ras mot bakändare som definieras under backendPools.</span><span class="sxs-lookup"><span data-stu-id="d1334-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="d1334-116">Hälso avsökningar kan bara avaktiveras om det finns en enda aktive rad server i en aktive rad Server del.</span><span class="sxs-lookup"><span data-stu-id="d1334-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1334-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="d1334-117">-HealthProbeMethod</span></span>
<span data-ttu-id="d1334-118">Konfigurerar vilken HTTP-metod som ska användas för att avsöka den bakände som definieras under backendPools.</span><span class="sxs-lookup"><span data-stu-id="d1334-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="d1334-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d1334-119">-IntervalInSeconds</span></span>
<span data-ttu-id="d1334-120">Antal sekunder mellan hälso avsökningarna.</span><span class="sxs-lookup"><span data-stu-id="d1334-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="d1334-121">Standardvärdet är 30</span><span class="sxs-lookup"><span data-stu-id="d1334-121">Default value is 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1334-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="d1334-122">-Name</span></span>
<span data-ttu-id="d1334-123">Inställnings namn för hälso avsökning.</span><span class="sxs-lookup"><span data-stu-id="d1334-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="d1334-124">-Path</span><span class="sxs-lookup"><span data-stu-id="d1334-124">-Path</span></span>
<span data-ttu-id="d1334-125">Sökvägen som ska användas för kontroll sonden.</span><span class="sxs-lookup"><span data-stu-id="d1334-125">The path to use for the health probe.</span></span>
<span data-ttu-id="d1334-126">Standard är/</span><span class="sxs-lookup"><span data-stu-id="d1334-126">Default is /</span></span>

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

### <span data-ttu-id="d1334-127">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d1334-127">-Protocol</span></span>
<span data-ttu-id="d1334-128">Protokoll schema som används för detta standardvärde för Avsök är HTTP</span><span class="sxs-lookup"><span data-stu-id="d1334-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1334-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1334-129">CommonParameters</span></span>
<span data-ttu-id="d1334-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1334-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1334-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1334-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1334-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1334-132">INPUTS</span></span>

### <span data-ttu-id="d1334-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="d1334-133">None</span></span>
## <span data-ttu-id="d1334-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1334-134">OUTPUTS</span></span>

### <span data-ttu-id="d1334-135">Microsoft. Azure. commands. FrontDoor. Models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="d1334-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="d1334-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1334-136">NOTES</span></span>

## <span data-ttu-id="d1334-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1334-137">RELATED LINKS</span></span>

<span data-ttu-id="d1334-138">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="d1334-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>

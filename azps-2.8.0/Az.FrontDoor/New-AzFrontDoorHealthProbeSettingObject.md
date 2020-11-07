---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 60eaa3b5482d6d1c13236560f797383d68d97b44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744149"
---
# <span data-ttu-id="1fee9-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="1fee9-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="1fee9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1fee9-102">SYNOPSIS</span></span>
<span data-ttu-id="1fee9-103">Skapa ett PSHealthProbeSetting-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="1fee9-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="1fee9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1fee9-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fee9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1fee9-105">DESCRIPTION</span></span>
<span data-ttu-id="1fee9-106">Skapa ett PSHealthProbeSetting-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="1fee9-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="1fee9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1fee9-107">EXAMPLES</span></span>

### <span data-ttu-id="1fee9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1fee9-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="1fee9-109">Skapa ett PSHealthProbeSetting-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="1fee9-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="1fee9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1fee9-110">PARAMETERS</span></span>

### <span data-ttu-id="1fee9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fee9-111">-DefaultProfile</span></span>
<span data-ttu-id="1fee9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1fee9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fee9-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1fee9-113">-IntervalInSeconds</span></span>
<span data-ttu-id="1fee9-114">Antal sekunder mellan hälso avsökningarna.</span><span class="sxs-lookup"><span data-stu-id="1fee9-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="1fee9-115">Standardvärdet är 30</span><span class="sxs-lookup"><span data-stu-id="1fee9-115">Default value is 30</span></span>

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

### <span data-ttu-id="1fee9-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="1fee9-116">-Name</span></span>
<span data-ttu-id="1fee9-117">inställnings namn för hälso avsökning.</span><span class="sxs-lookup"><span data-stu-id="1fee9-117">health probe setting name.</span></span>

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

### <span data-ttu-id="1fee9-118">-Path</span><span class="sxs-lookup"><span data-stu-id="1fee9-118">-Path</span></span>
<span data-ttu-id="1fee9-119">Sökvägen som ska användas för kontroll sonden.</span><span class="sxs-lookup"><span data-stu-id="1fee9-119">The path to use for the health probe.</span></span>
<span data-ttu-id="1fee9-120">Standard är/</span><span class="sxs-lookup"><span data-stu-id="1fee9-120">Default is /</span></span>

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

### <span data-ttu-id="1fee9-121">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="1fee9-121">-Protocol</span></span>
<span data-ttu-id="1fee9-122">Protokoll schema som används för detta standardvärde för Avsök är HTTP</span><span class="sxs-lookup"><span data-stu-id="1fee9-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="1fee9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fee9-123">CommonParameters</span></span>
<span data-ttu-id="1fee9-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fee9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fee9-125">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fee9-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fee9-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1fee9-126">INPUTS</span></span>

### <span data-ttu-id="1fee9-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="1fee9-127">None</span></span>

## <span data-ttu-id="1fee9-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1fee9-128">OUTPUTS</span></span>

### <span data-ttu-id="1fee9-129">Microsoft. Azure. commands. FrontDoor. Models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="1fee9-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="1fee9-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1fee9-130">NOTES</span></span>

## <span data-ttu-id="1fee9-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1fee9-131">RELATED LINKS</span></span>

<span data-ttu-id="1fee9-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="1fee9-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>

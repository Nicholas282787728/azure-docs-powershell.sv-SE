---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: dcaf61b9001093d25f351d03e8e50da4c4ca22ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577025"
---
# <span data-ttu-id="9f51f-101">New-AzureRmFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="9f51f-101">New-AzureRmFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="9f51f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f51f-102">SYNOPSIS</span></span>
<span data-ttu-id="9f51f-103">Skapa ett PSHealthProbeSetting-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="9f51f-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f51f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f51f-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f51f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f51f-105">DESCRIPTION</span></span>
<span data-ttu-id="9f51f-106">Skapa ett PSHealthProbeSetting-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="9f51f-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="9f51f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f51f-107">EXAMPLES</span></span>

### <span data-ttu-id="9f51f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9f51f-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="9f51f-109">Skapa ett PSHealthProbeSetting-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="9f51f-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="9f51f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f51f-110">PARAMETERS</span></span>

### <span data-ttu-id="9f51f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f51f-111">-DefaultProfile</span></span>
<span data-ttu-id="9f51f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f51f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f51f-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9f51f-113">-IntervalInSeconds</span></span>
<span data-ttu-id="9f51f-114">Antal sekunder mellan hälso avsökningarna.</span><span class="sxs-lookup"><span data-stu-id="9f51f-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="9f51f-115">Standardvärdet är 30</span><span class="sxs-lookup"><span data-stu-id="9f51f-115">Default value is 30</span></span>

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

### <span data-ttu-id="9f51f-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="9f51f-116">-Name</span></span>
<span data-ttu-id="9f51f-117">inställnings namn för hälso avsökning.</span><span class="sxs-lookup"><span data-stu-id="9f51f-117">health probe setting name.</span></span>

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

### <span data-ttu-id="9f51f-118">-Path</span><span class="sxs-lookup"><span data-stu-id="9f51f-118">-Path</span></span>
<span data-ttu-id="9f51f-119">Sökvägen som ska användas för kontroll sonden.</span><span class="sxs-lookup"><span data-stu-id="9f51f-119">The path to use for the health probe.</span></span>
<span data-ttu-id="9f51f-120">Standard är/</span><span class="sxs-lookup"><span data-stu-id="9f51f-120">Default is /</span></span>

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

### <span data-ttu-id="9f51f-121">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="9f51f-121">-Protocol</span></span>
<span data-ttu-id="9f51f-122">Protokoll schema som används för detta standardvärde för Avsök är HTTP</span><span class="sxs-lookup"><span data-stu-id="9f51f-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="9f51f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f51f-123">CommonParameters</span></span>
<span data-ttu-id="9f51f-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f51f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f51f-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f51f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f51f-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f51f-126">INPUTS</span></span>

### <span data-ttu-id="9f51f-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="9f51f-127">None</span></span>

## <span data-ttu-id="9f51f-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f51f-128">OUTPUTS</span></span>

### <span data-ttu-id="9f51f-129">Microsoft. Azure. commands. FrontDoor. Models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="9f51f-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="9f51f-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f51f-130">NOTES</span></span>

## <span data-ttu-id="9f51f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f51f-131">RELATED LINKS</span></span>

<span data-ttu-id="9f51f-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="9f51f-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>

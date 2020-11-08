---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259958"
---
# <span data-ttu-id="75a1b-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="75a1b-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="75a1b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="75a1b-103">Skapa ett PSBackendPoolsSetting-objekt för att skapa en front dörr.</span><span class="sxs-lookup"><span data-stu-id="75a1b-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="75a1b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75a1b-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75a1b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75a1b-105">DESCRIPTION</span></span>
<span data-ttu-id="75a1b-106">Cmdleten **New-AzFrontDoorBackendpoolsSettingObject** skapar ett nytt PSBackendPoolsSettings-objekt för skapande av front dörrar.</span><span class="sxs-lookup"><span data-stu-id="75a1b-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="75a1b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75a1b-107">EXAMPLES</span></span>

### <span data-ttu-id="75a1b-108">Exempel 1: skapa BackendPoolsSettings-objekt med standardvärden</span><span class="sxs-lookup"><span data-stu-id="75a1b-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="75a1b-109">Exempel 2: skapa BackendPoolsSettings-objekt med användardefinierade värden</span><span class="sxs-lookup"><span data-stu-id="75a1b-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="75a1b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75a1b-110">PARAMETERS</span></span>

### <span data-ttu-id="75a1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a1b-111">-DefaultProfile</span></span>
<span data-ttu-id="75a1b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75a1b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75a1b-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="75a1b-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="75a1b-114">Om certifikat namns kontrollen ska tillämpas på HTTPS-begäranden till alla backend-pooler.</span><span class="sxs-lookup"><span data-stu-id="75a1b-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="75a1b-115">Ingen effekt på icke-HTTPS-begäranden.</span><span class="sxs-lookup"><span data-stu-id="75a1b-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="75a1b-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="75a1b-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="75a1b-117">Skicka och ta emot timeout för vidarebefordran till Server delen.</span><span class="sxs-lookup"><span data-stu-id="75a1b-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="75a1b-118">Det går inte att returnera och returnerar en begäran.</span><span class="sxs-lookup"><span data-stu-id="75a1b-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="75a1b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a1b-119">CommonParameters</span></span>
<span data-ttu-id="75a1b-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75a1b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a1b-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75a1b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a1b-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75a1b-122">INPUTS</span></span>

### <span data-ttu-id="75a1b-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="75a1b-123">None</span></span>

## <span data-ttu-id="75a1b-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75a1b-124">OUTPUTS</span></span>

### <span data-ttu-id="75a1b-125">Microsoft. Azure. commands. FrontDoor. Models. PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="75a1b-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="75a1b-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75a1b-126">NOTES</span></span>

## <span data-ttu-id="75a1b-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75a1b-127">RELATED LINKS</span></span>

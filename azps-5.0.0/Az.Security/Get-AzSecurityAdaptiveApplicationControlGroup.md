---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: 9d36169439a2466ca50858f5b438822461259cf3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325505"
---
# <span data-ttu-id="b62a7-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="b62a7-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="b62a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b62a7-102">SYNOPSIS</span></span>
<span data-ttu-id="b62a7-103">Hämtar en program kontroll för virtuell dator/Server grupp.</span><span class="sxs-lookup"><span data-stu-id="b62a7-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="b62a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b62a7-104">SYNTAX</span></span>

### <span data-ttu-id="b62a7-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="b62a7-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b62a7-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b62a7-106">DESCRIPTION</span></span>
<span data-ttu-id="b62a7-107">Anpassade program kontroller beräknas automatiskt i Azure Security Center, Använd denna cmdlet för att få en program kontroll för virtuell dator/Server grupp.</span><span class="sxs-lookup"><span data-stu-id="b62a7-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="b62a7-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b62a7-108">EXAMPLES</span></span>

### <span data-ttu-id="b62a7-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b62a7-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="b62a7-110">Hämtar en program kontroll för virtuell dator/Server grupp.</span><span class="sxs-lookup"><span data-stu-id="b62a7-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="b62a7-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b62a7-111">PARAMETERS</span></span>

### <span data-ttu-id="b62a7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b62a7-112">-DefaultProfile</span></span>
<span data-ttu-id="b62a7-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b62a7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b62a7-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="b62a7-114">-AscLocation</span></span>
<span data-ttu-id="b62a7-115">Platsen där ASC lagrar data för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b62a7-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="b62a7-116">kan hämtas från hitta platser.</span><span class="sxs-lookup"><span data-stu-id="b62a7-116">can be retrieved from Get locations.</span></span>

```yaml
Type: System.String
Parameter Sets: AscLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b62a7-117">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="b62a7-117">-GroupName</span></span>
<span data-ttu-id="b62a7-118">Namn på en program kontroll för en virtuell dator/Server grupp.</span><span class="sxs-lookup"><span data-stu-id="b62a7-118">Name of an application control VM/server group.</span></span>

```yaml
Type: System.String
Parameter Sets: GroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b62a7-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b62a7-119">-SubscriptionId</span></span>
<span data-ttu-id="b62a7-120">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b62a7-120">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="b62a7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b62a7-121">CommonParameters</span></span>
<span data-ttu-id="b62a7-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b62a7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b62a7-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b62a7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b62a7-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b62a7-124">INPUTS</span></span>

### <span data-ttu-id="b62a7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b62a7-125">System.String</span></span>

## <span data-ttu-id="b62a7-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b62a7-126">OUTPUTS</span></span>

### <span data-ttu-id="b62a7-127">Microsoft. Azure. commands. Security. Models. AdaptiveApplicationControls. PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="b62a7-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="b62a7-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b62a7-128">NOTES</span></span>

## <span data-ttu-id="b62a7-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b62a7-129">RELATED LINKS</span></span>
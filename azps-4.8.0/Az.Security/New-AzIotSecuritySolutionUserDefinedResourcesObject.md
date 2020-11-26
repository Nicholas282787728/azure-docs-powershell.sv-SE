---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: e824c32ae2ae4f28972cdac9446eeeae6e410c75
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261707"
---
# <span data-ttu-id="92e31-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="92e31-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="92e31-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92e31-102">SYNOPSIS</span></span>
<span data-ttu-id="92e31-103">Skapa nya användardefinierade resurser för IoT-säkerhetslösning</span><span class="sxs-lookup"><span data-stu-id="92e31-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="92e31-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92e31-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92e31-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92e31-105">DESCRIPTION</span></span>
<span data-ttu-id="92e31-106">AzIotSecuritySolutionUserDefinedResourcesObject-cmdleten skapar ett nytt användardefinierat objekt för säkerhets lösning för IoT.</span><span class="sxs-lookup"><span data-stu-id="92e31-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="92e31-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92e31-107">EXAMPLES</span></span>

### <span data-ttu-id="92e31-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="92e31-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="92e31-109">Skapa nya användardefinierade resurser</span><span class="sxs-lookup"><span data-stu-id="92e31-109">Create new user defined resources</span></span>

## <span data-ttu-id="92e31-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92e31-110">PARAMETERS</span></span>

### <span data-ttu-id="92e31-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e31-111">-DefaultProfile</span></span>
<span data-ttu-id="92e31-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92e31-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92e31-113">-Fråga</span><span class="sxs-lookup"><span data-stu-id="92e31-113">-Query</span></span>
<span data-ttu-id="92e31-114">Frågeserver.</span><span class="sxs-lookup"><span data-stu-id="92e31-114">Query.</span></span>

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

### <span data-ttu-id="92e31-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="92e31-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="92e31-116">Fråga om abonnemang.</span><span class="sxs-lookup"><span data-stu-id="92e31-116">Query subscriptions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e31-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e31-117">CommonParameters</span></span>
<span data-ttu-id="92e31-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e31-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e31-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92e31-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e31-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92e31-120">INPUTS</span></span>

### <span data-ttu-id="92e31-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="92e31-121">None</span></span>

## <span data-ttu-id="92e31-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92e31-122">OUTPUTS</span></span>

### <span data-ttu-id="92e31-123">Microsoft. Azure. commands. Security. Models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="92e31-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="92e31-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92e31-124">NOTES</span></span>

## <span data-ttu-id="92e31-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92e31-125">RELATED LINKS</span></span>
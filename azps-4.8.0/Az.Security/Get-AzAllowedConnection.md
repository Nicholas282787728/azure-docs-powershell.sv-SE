---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101991"
---
# <span data-ttu-id="ef28d-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="ef28d-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="ef28d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef28d-102">SYNOPSIS</span></span>
<span data-ttu-id="ef28d-103">Används för att Visa tillåten trafik mellan resurser för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="ef28d-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="ef28d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef28d-104">SYNTAX</span></span>

### <span data-ttu-id="ef28d-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="ef28d-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef28d-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="ef28d-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef28d-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef28d-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef28d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef28d-108">DESCRIPTION</span></span>
<span data-ttu-id="ef28d-109">Hämtar listan över all möjlig trafik mellan resurser för abonnemanget och platsen, baserat på Anslutnings typ.</span><span class="sxs-lookup"><span data-stu-id="ef28d-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="ef28d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef28d-110">EXAMPLES</span></span>

### <span data-ttu-id="ef28d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ef28d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="ef28d-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ef28d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="ef28d-113">Hämtar listan över all möjlig trafik mellan resurser för abonnemanget och platsen, baserat på Anslutnings typ.</span><span class="sxs-lookup"><span data-stu-id="ef28d-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="ef28d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef28d-114">PARAMETERS</span></span>

### <span data-ttu-id="ef28d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef28d-115">-DefaultProfile</span></span>
<span data-ttu-id="ef28d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef28d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef28d-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="ef28d-117">-Location</span></span>
<span data-ttu-id="ef28d-118">Plats.</span><span class="sxs-lookup"><span data-stu-id="ef28d-118">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef28d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef28d-119">-Name</span></span>
<span data-ttu-id="ef28d-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="ef28d-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef28d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef28d-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef28d-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ef28d-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef28d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef28d-123">-ResourceId</span></span>
<span data-ttu-id="ef28d-124">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="ef28d-124">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef28d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef28d-125">CommonParameters</span></span>
<span data-ttu-id="ef28d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef28d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef28d-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef28d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef28d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef28d-128">INPUTS</span></span>

### <span data-ttu-id="ef28d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ef28d-129">System.String</span></span>

## <span data-ttu-id="ef28d-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef28d-130">OUTPUTS</span></span>

### <span data-ttu-id="ef28d-131">Microsoft. Azure. commands. Security. Models. AllowedConnection. PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="ef28d-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="ef28d-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef28d-132">NOTES</span></span>

## <span data-ttu-id="ef28d-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef28d-133">RELATED LINKS</span></span>

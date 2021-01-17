---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: ef984a1cbb1cf922ddc931a7924a5d39ba6c6a0b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396064"
---
# <span data-ttu-id="038ae-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="038ae-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="038ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="038ae-102">SYNOPSIS</span></span>
<span data-ttu-id="038ae-103">Hämtar en lista över säkerhetstopologier för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="038ae-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="038ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="038ae-104">SYNTAX</span></span>

### <span data-ttu-id="038ae-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="038ae-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="038ae-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="038ae-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="038ae-107">ID</span><span class="sxs-lookup"><span data-stu-id="038ae-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="038ae-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="038ae-108">DESCRIPTION</span></span>
<span data-ttu-id="038ae-109">Säkerhetstopologier identifieras automatiskt av Azure Security Center, Använd denna cmdlet för att Visa säkerhets topologier.</span><span class="sxs-lookup"><span data-stu-id="038ae-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="038ae-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="038ae-110">EXAMPLES</span></span>

### <span data-ttu-id="038ae-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="038ae-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="038ae-112">Visa alla säkerhetstopologier i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="038ae-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="038ae-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="038ae-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="038ae-114">Få en viss säkerhets topologi</span><span class="sxs-lookup"><span data-stu-id="038ae-114">Get a specific security topologies</span></span>

## <span data-ttu-id="038ae-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="038ae-115">PARAMETERS</span></span>

### <span data-ttu-id="038ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="038ae-116">-DefaultProfile</span></span>
<span data-ttu-id="038ae-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="038ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="038ae-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="038ae-118">-Location</span></span>
<span data-ttu-id="038ae-119">Plats.</span><span class="sxs-lookup"><span data-stu-id="038ae-119">Location.</span></span>

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

### <span data-ttu-id="038ae-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="038ae-120">-Name</span></span>
<span data-ttu-id="038ae-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="038ae-121">Resource name.</span></span>

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

### <span data-ttu-id="038ae-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="038ae-122">-ResourceGroupName</span></span>
<span data-ttu-id="038ae-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="038ae-123">Resource group name.</span></span>

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

### <span data-ttu-id="038ae-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="038ae-124">-ResourceId</span></span>
<span data-ttu-id="038ae-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="038ae-125">Resource ID.</span></span>

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

### <span data-ttu-id="038ae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="038ae-126">CommonParameters</span></span>
<span data-ttu-id="038ae-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="038ae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="038ae-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="038ae-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="038ae-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="038ae-129">INPUTS</span></span>

### <span data-ttu-id="038ae-130">System. String</span><span class="sxs-lookup"><span data-stu-id="038ae-130">System.String</span></span>

## <span data-ttu-id="038ae-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="038ae-131">OUTPUTS</span></span>

### <span data-ttu-id="038ae-132">Microsoft. Azure. commands. Security. Models. Topology. PSSecurityTopologies</span><span class="sxs-lookup"><span data-stu-id="038ae-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="038ae-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="038ae-133">NOTES</span></span>

## <span data-ttu-id="038ae-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="038ae-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: 338486954fe04b6497eb82bc5a11dbede1b25709
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416312"
---
# <span data-ttu-id="cada7-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="cada7-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="cada7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cada7-102">SYNOPSIS</span></span>
<span data-ttu-id="cada7-103">Skaffa IoT-säkerhetslösning</span><span class="sxs-lookup"><span data-stu-id="cada7-103">Get IoT security solution</span></span>

## <span data-ttu-id="cada7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cada7-104">SYNTAX</span></span>

### <span data-ttu-id="cada7-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="cada7-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cada7-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="cada7-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cada7-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="cada7-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cada7-108">ID</span><span class="sxs-lookup"><span data-stu-id="cada7-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cada7-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cada7-109">DESCRIPTION</span></span>
<span data-ttu-id="cada7-110">Get-AzIotSecuritySolution cmdlet returnerar en eller flera IoT-säkerhetslösningar.</span><span class="sxs-lookup"><span data-stu-id="cada7-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="cada7-111">IoT-säkerhetslösningen samlar in säkerhets data från IoT-enheter och IoT Hub för att förhindra och upptäcka hot.</span><span class="sxs-lookup"><span data-stu-id="cada7-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="cada7-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cada7-112">EXAMPLES</span></span>

### <span data-ttu-id="cada7-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cada7-113">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "centraluseuap"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="cada7-114">Få lösningen "Sample" i resurs gruppen "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="cada7-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="cada7-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cada7-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="cada7-116">Få en lista över alla säkerhetslösningar i resurs gruppen "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="cada7-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="cada7-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cada7-117">PARAMETERS</span></span>

### <span data-ttu-id="cada7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cada7-118">-DefaultProfile</span></span>
<span data-ttu-id="cada7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cada7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cada7-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="cada7-120">-Name</span></span>
<span data-ttu-id="cada7-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="cada7-121">Resource name.</span></span>

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

### <span data-ttu-id="cada7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cada7-122">-ResourceGroupName</span></span>
<span data-ttu-id="cada7-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="cada7-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cada7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cada7-124">-ResourceId</span></span>
<span data-ttu-id="cada7-125">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="cada7-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="cada7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cada7-126">CommonParameters</span></span>
<span data-ttu-id="cada7-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cada7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cada7-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cada7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cada7-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cada7-129">INPUTS</span></span>

### <span data-ttu-id="cada7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cada7-130">System.String</span></span>

## <span data-ttu-id="cada7-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cada7-131">OUTPUTS</span></span>

### <span data-ttu-id="cada7-132">Microsoft. Azure. commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="cada7-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="cada7-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cada7-133">NOTES</span></span>

## <span data-ttu-id="cada7-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cada7-134">RELATED LINKS</span></span>

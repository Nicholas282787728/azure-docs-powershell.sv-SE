---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: afb6a5bab6c2761095fb3ab69a2898aeeb53b45c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271971"
---
# <span data-ttu-id="b4424-101">Get-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="b4424-101">Get-AzConnectedMachine</span></span>

## <span data-ttu-id="b4424-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4424-102">SYNOPSIS</span></span>
<span data-ttu-id="b4424-103">Hämtar information om modell läget eller instans visningen av en hybrid dator.</span><span class="sxs-lookup"><span data-stu-id="b4424-103">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="b4424-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4424-104">SYNTAX</span></span>

### <span data-ttu-id="b4424-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="b4424-105">List1 (Default)</span></span>
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b4424-106">Lära</span><span class="sxs-lookup"><span data-stu-id="b4424-106">Get</span></span>
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b4424-107">Förteckning</span><span class="sxs-lookup"><span data-stu-id="b4424-107">List</span></span>
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4424-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4424-108">DESCRIPTION</span></span>
<span data-ttu-id="b4424-109">Hämtar information om modell läget eller instans visningen av en hybrid dator.</span><span class="sxs-lookup"><span data-stu-id="b4424-109">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="b4424-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4424-110">EXAMPLES</span></span>

### <span data-ttu-id="b4424-111">Exempel 1: lista alla anslutna datorer i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="b4424-111">Example 1: List all connected machines in a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

<span data-ttu-id="b4424-112">Visar en lista över alla anslutna datorer i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="b4424-112">Lists all connected machines in a subscription.</span></span>
<span data-ttu-id="b4424-113">Om abonnemang inte anges används prenumerationen från din nuvarande Azure PowerShell-kontext.</span><span class="sxs-lookup"><span data-stu-id="b4424-113">If subscription isn't specified, it will use the subscription from your current Azure PowerShell context.</span></span>

### <span data-ttu-id="b4424-114">Exempel 2: lista alla anslutna datorer i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="b4424-114">Example 2: List all connected machines in a resource group</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="b4424-115">Visa en lista med alla anslutna datorer i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b4424-115">List all connected machines in a resource group.</span></span>

### <span data-ttu-id="b4424-116">Exempel 3: skaffa en ansluten dator i en resurs grupp efter namn</span><span class="sxs-lookup"><span data-stu-id="b4424-116">Example 3: Get a connected machine in a resource group by name</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="b4424-117">Skaffa en ansluten dator i en resurs grupp efter namn.</span><span class="sxs-lookup"><span data-stu-id="b4424-117">Get a connected machine in a resource group by name.</span></span>

## <span data-ttu-id="b4424-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4424-118">PARAMETERS</span></span>

### <span data-ttu-id="b4424-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4424-119">-DefaultProfile</span></span>
<span data-ttu-id="b4424-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4424-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4424-121">-Expandera</span><span class="sxs-lookup"><span data-stu-id="b4424-121">-Expand</span></span>
<span data-ttu-id="b4424-122">Uttrycket expandera för åtgärden.</span><span class="sxs-lookup"><span data-stu-id="b4424-122">The expand expression to apply on the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Support.InstanceViewTypes
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4424-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4424-123">-Name</span></span>
<span data-ttu-id="b4424-124">Namnet på Hybrid datorn.</span><span class="sxs-lookup"><span data-stu-id="b4424-124">The name of the hybrid machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4424-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4424-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4424-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b4424-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4424-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4424-127">-SubscriptionId</span></span>
<span data-ttu-id="b4424-128">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b4424-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b4424-129">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="b4424-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4424-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4424-130">CommonParameters</span></span>
<span data-ttu-id="b4424-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4424-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4424-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4424-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4424-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4424-133">INPUTS</span></span>

## <span data-ttu-id="b4424-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4424-134">OUTPUTS</span></span>

### <span data-ttu-id="b4424-135">Microsoft. Azure. PowerShell. cmdletar. ConnectedMachine. Models. Api20200802. IMachine</span><span class="sxs-lookup"><span data-stu-id="b4424-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span></span>

## <span data-ttu-id="b4424-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4424-136">NOTES</span></span>

<span data-ttu-id="b4424-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b4424-137">ALIASES</span></span>

## <span data-ttu-id="b4424-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4424-138">RELATED LINKS</span></span>

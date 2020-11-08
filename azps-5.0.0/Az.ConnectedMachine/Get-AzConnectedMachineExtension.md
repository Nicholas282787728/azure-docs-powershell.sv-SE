---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271970"
---
# <span data-ttu-id="31cea-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="31cea-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="31cea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31cea-102">SYNOPSIS</span></span>
<span data-ttu-id="31cea-103">Åtgärden för att hämta tillägget.</span><span class="sxs-lookup"><span data-stu-id="31cea-103">The operation to get the extension.</span></span>

## <span data-ttu-id="31cea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31cea-104">SYNTAX</span></span>

### <span data-ttu-id="31cea-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="31cea-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="31cea-106">Lära</span><span class="sxs-lookup"><span data-stu-id="31cea-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="31cea-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31cea-107">DESCRIPTION</span></span>
<span data-ttu-id="31cea-108">Åtgärden för att hämta tillägget.</span><span class="sxs-lookup"><span data-stu-id="31cea-108">The operation to get the extension.</span></span>

## <span data-ttu-id="31cea-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31cea-109">EXAMPLES</span></span>

### <span data-ttu-id="31cea-110">Exempel 1: lista alla tillägg för en dator</span><span class="sxs-lookup"><span data-stu-id="31cea-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="31cea-111">Visar alla tillägg för en viss dator.</span><span class="sxs-lookup"><span data-stu-id="31cea-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="31cea-112">Exempel 2: skaffa en särskild anknytning på en dator</span><span class="sxs-lookup"><span data-stu-id="31cea-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="31cea-113">Hämtar ett specifikt tillägg på en dator.</span><span class="sxs-lookup"><span data-stu-id="31cea-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="31cea-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31cea-114">PARAMETERS</span></span>

### <span data-ttu-id="31cea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31cea-115">-DefaultProfile</span></span>
<span data-ttu-id="31cea-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31cea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31cea-117">-Expandera</span><span class="sxs-lookup"><span data-stu-id="31cea-117">-Expand</span></span>
<span data-ttu-id="31cea-118">Uttrycket expandera för åtgärden.</span><span class="sxs-lookup"><span data-stu-id="31cea-118">The expand expression to apply on the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31cea-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="31cea-119">-MachineName</span></span>
<span data-ttu-id="31cea-120">Namnet på den dator som innehåller tillägget.</span><span class="sxs-lookup"><span data-stu-id="31cea-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="31cea-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="31cea-121">-Name</span></span>
<span data-ttu-id="31cea-122">Namnet på dator tillägget.</span><span class="sxs-lookup"><span data-stu-id="31cea-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="31cea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31cea-123">-ResourceGroupName</span></span>
<span data-ttu-id="31cea-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="31cea-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="31cea-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31cea-125">-SubscriptionId</span></span>
<span data-ttu-id="31cea-126">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="31cea-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="31cea-127">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="31cea-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="31cea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31cea-128">CommonParameters</span></span>
<span data-ttu-id="31cea-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31cea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31cea-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31cea-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31cea-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31cea-131">INPUTS</span></span>

## <span data-ttu-id="31cea-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31cea-132">OUTPUTS</span></span>

### <span data-ttu-id="31cea-133">Microsoft. Azure. PowerShell. cmdletar. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="31cea-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="31cea-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31cea-134">NOTES</span></span>

<span data-ttu-id="31cea-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="31cea-135">ALIASES</span></span>

## <span data-ttu-id="31cea-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31cea-136">RELATED LINKS</span></span>


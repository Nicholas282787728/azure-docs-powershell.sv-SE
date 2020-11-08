---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261117"
---
# <span data-ttu-id="dbc16-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="dbc16-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="dbc16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dbc16-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc16-103">Åtgärden för att hämta tillägget.</span><span class="sxs-lookup"><span data-stu-id="dbc16-103">The operation to get the extension.</span></span>

## <span data-ttu-id="dbc16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dbc16-104">SYNTAX</span></span>

### <span data-ttu-id="dbc16-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="dbc16-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dbc16-106">Lära</span><span class="sxs-lookup"><span data-stu-id="dbc16-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dbc16-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dbc16-107">DESCRIPTION</span></span>
<span data-ttu-id="dbc16-108">Åtgärden för att hämta tillägget.</span><span class="sxs-lookup"><span data-stu-id="dbc16-108">The operation to get the extension.</span></span>

## <span data-ttu-id="dbc16-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dbc16-109">EXAMPLES</span></span>

### <span data-ttu-id="dbc16-110">Exempel 1: lista alla tillägg för en dator</span><span class="sxs-lookup"><span data-stu-id="dbc16-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="dbc16-111">Visar alla tillägg för en viss dator.</span><span class="sxs-lookup"><span data-stu-id="dbc16-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="dbc16-112">Exempel 2: skaffa en särskild anknytning på en dator</span><span class="sxs-lookup"><span data-stu-id="dbc16-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="dbc16-113">Hämtar ett specifikt tillägg på en dator.</span><span class="sxs-lookup"><span data-stu-id="dbc16-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="dbc16-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dbc16-114">PARAMETERS</span></span>

### <span data-ttu-id="dbc16-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc16-115">-DefaultProfile</span></span>
<span data-ttu-id="dbc16-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dbc16-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbc16-117">-Expandera</span><span class="sxs-lookup"><span data-stu-id="dbc16-117">-Expand</span></span>
<span data-ttu-id="dbc16-118">Uttrycket expandera för åtgärden.</span><span class="sxs-lookup"><span data-stu-id="dbc16-118">The expand expression to apply on the operation.</span></span>

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

### <span data-ttu-id="dbc16-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="dbc16-119">-MachineName</span></span>
<span data-ttu-id="dbc16-120">Namnet på den dator som innehåller tillägget.</span><span class="sxs-lookup"><span data-stu-id="dbc16-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="dbc16-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="dbc16-121">-Name</span></span>
<span data-ttu-id="dbc16-122">Namnet på dator tillägget.</span><span class="sxs-lookup"><span data-stu-id="dbc16-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="dbc16-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc16-123">-ResourceGroupName</span></span>
<span data-ttu-id="dbc16-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="dbc16-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="dbc16-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dbc16-125">-SubscriptionId</span></span>
<span data-ttu-id="dbc16-126">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="dbc16-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dbc16-127">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="dbc16-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dbc16-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc16-128">CommonParameters</span></span>
<span data-ttu-id="dbc16-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbc16-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc16-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbc16-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc16-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dbc16-131">INPUTS</span></span>

## <span data-ttu-id="dbc16-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dbc16-132">OUTPUTS</span></span>

### <span data-ttu-id="dbc16-133">Microsoft. Azure. PowerShell. cmdletar. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="dbc16-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="dbc16-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dbc16-134">NOTES</span></span>

<span data-ttu-id="dbc16-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="dbc16-135">ALIASES</span></span>

## <span data-ttu-id="dbc16-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dbc16-136">RELATED LINKS</span></span>


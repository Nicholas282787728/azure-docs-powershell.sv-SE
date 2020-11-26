---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: 6a3a421f1da374db1cc08635891bdeec4375855a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260498"
---
# <span data-ttu-id="4ce51-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="4ce51-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="4ce51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ce51-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce51-103">Hämtar funktions program i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="4ce51-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="4ce51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ce51-104">SYNTAX</span></span>

### <span data-ttu-id="4ce51-105">GetAll (standard)</span><span class="sxs-lookup"><span data-stu-id="4ce51-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ce51-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="4ce51-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ce51-107">ByName</span><span class="sxs-lookup"><span data-stu-id="4ce51-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4ce51-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce51-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4ce51-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ce51-109">DESCRIPTION</span></span>
<span data-ttu-id="4ce51-110">Hämtar funktions program i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="4ce51-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="4ce51-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ce51-111">EXAMPLES</span></span>

### <span data-ttu-id="4ce51-112">Exempel 1: Hämta alla program.</span><span class="sxs-lookup"><span data-stu-id="4ce51-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="4ce51-113">Exempel 2: Hämta programfunktionen efter namn.</span><span class="sxs-lookup"><span data-stu-id="4ce51-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="4ce51-114">Exempel 3: Hämta program efter resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="4ce51-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="4ce51-115">Exempel 4: Hämta programfunktioner för de angivna abonnemangen.</span><span class="sxs-lookup"><span data-stu-id="4ce51-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="4ce51-116">Exempel 5: Hämta program efter plats.</span><span class="sxs-lookup"><span data-stu-id="4ce51-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="4ce51-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ce51-117">PARAMETERS</span></span>

### <span data-ttu-id="4ce51-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce51-118">-DefaultProfile</span></span>
<span data-ttu-id="4ce51-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ce51-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ce51-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="4ce51-120">-IncludeSlot</span></span>
<span data-ttu-id="4ce51-121">Används för att ange om distributions platser ska ingå i resultaten.</span><span class="sxs-lookup"><span data-stu-id="4ce51-121">Use to specify whether to include deployment slots in results.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ce51-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="4ce51-122">-Location</span></span>
<span data-ttu-id="4ce51-123">Platsen för funktionen funktion.</span><span class="sxs-lookup"><span data-stu-id="4ce51-123">The location of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ce51-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ce51-124">-Name</span></span>
<span data-ttu-id="4ce51-125">Namnet på funktionen funktion.</span><span class="sxs-lookup"><span data-stu-id="4ce51-125">The name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ce51-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce51-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ce51-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4ce51-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ce51-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ce51-128">-SubscriptionId</span></span>
<span data-ttu-id="4ce51-129">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="4ce51-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="4ce51-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce51-130">CommonParameters</span></span>
<span data-ttu-id="4ce51-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ce51-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce51-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ce51-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce51-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ce51-133">INPUTS</span></span>

## <span data-ttu-id="4ce51-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ce51-134">OUTPUTS</span></span>

### <span data-ttu-id="4ce51-135">Microsoft. Azure. PowerShell. cmdletar. functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="4ce51-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="4ce51-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ce51-136">NOTES</span></span>

<span data-ttu-id="4ce51-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4ce51-137">ALIASES</span></span>

## <span data-ttu-id="4ce51-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ce51-138">RELATED LINKS</span></span>

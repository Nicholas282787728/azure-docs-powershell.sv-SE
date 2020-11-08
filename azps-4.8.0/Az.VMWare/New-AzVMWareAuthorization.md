---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
ms.openlocfilehash: b1e8ca1e5140470524ec83656ef0042bafa494b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261169"
---
# <span data-ttu-id="f6a8e-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="f6a8e-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="f6a8e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a8e-103">Skapa eller uppdatera en ExpressRoute i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="f6a8e-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="f6a8e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6a8e-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f6a8e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6a8e-105">DESCRIPTION</span></span>
<span data-ttu-id="f6a8e-106">Skapa eller uppdatera en ExpressRoute i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="f6a8e-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="f6a8e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6a8e-107">EXAMPLES</span></span>

### <span data-ttu-id="f6a8e-108">Exempel 1: skapa autorization</span><span class="sxs-lookup"><span data-stu-id="f6a8e-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="f6a8e-109">Denna cmdlet skapar auktorisering `azps-test-auth` under privat moln `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="f6a8e-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="f6a8e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6a8e-110">PARAMETERS</span></span>

### <span data-ttu-id="f6a8e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6a8e-111">-AsJob</span></span>
<span data-ttu-id="f6a8e-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="f6a8e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f6a8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a8e-113">-DefaultProfile</span></span>
<span data-ttu-id="f6a8e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6a8e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6a8e-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f6a8e-115">-Name</span></span>
<span data-ttu-id="f6a8e-116">Namn på ExpressRoute-kretsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="f6a8e-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a8e-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f6a8e-117">-NoWait</span></span>
<span data-ttu-id="f6a8e-118">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="f6a8e-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f6a8e-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="f6a8e-119">-PrivateCloudName</span></span>
<span data-ttu-id="f6a8e-120">Namnet på det privata molnet.</span><span class="sxs-lookup"><span data-stu-id="f6a8e-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="f6a8e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a8e-121">-ResourceGroupName</span></span>
<span data-ttu-id="f6a8e-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f6a8e-122">The name of the resource group.</span></span>
<span data-ttu-id="f6a8e-123">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="f6a8e-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f6a8e-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6a8e-124">-SubscriptionId</span></span>
<span data-ttu-id="f6a8e-125">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f6a8e-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a8e-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f6a8e-126">-Confirm</span></span>
<span data-ttu-id="f6a8e-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f6a8e-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a8e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6a8e-128">-WhatIf</span></span>
<span data-ttu-id="f6a8e-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f6a8e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6a8e-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f6a8e-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a8e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a8e-131">CommonParameters</span></span>
<span data-ttu-id="f6a8e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6a8e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a8e-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6a8e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a8e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6a8e-134">INPUTS</span></span>

## <span data-ttu-id="f6a8e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6a8e-135">OUTPUTS</span></span>

### <span data-ttu-id="f6a8e-136">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. Api20200320. IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="f6a8e-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="f6a8e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6a8e-137">NOTES</span></span>

<span data-ttu-id="f6a8e-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f6a8e-138">ALIASES</span></span>

## <span data-ttu-id="f6a8e-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6a8e-139">RELATED LINKS</span></span>


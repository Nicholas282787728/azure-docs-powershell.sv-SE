---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: ae630f053f6267a49477118786cf70b65782d68e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260283"
---
# <span data-ttu-id="2614c-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="2614c-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="2614c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2614c-102">SYNOPSIS</span></span>
<span data-ttu-id="2614c-103">Skapa eller uppdatera en koppling.</span><span class="sxs-lookup"><span data-stu-id="2614c-103">Create or update an association.</span></span>

## <span data-ttu-id="2614c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2614c-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2614c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2614c-105">DESCRIPTION</span></span>
<span data-ttu-id="2614c-106">Skapa eller uppdatera en koppling.</span><span class="sxs-lookup"><span data-stu-id="2614c-106">Create or update an association.</span></span>

## <span data-ttu-id="2614c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2614c-107">EXAMPLES</span></span>

### <span data-ttu-id="2614c-108">Exempel 1: skapa en anpassad leverantörs koppling</span><span class="sxs-lookup"><span data-stu-id="2614c-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="2614c-109">Skapa en anpassad leverantörs koppling måste den associerade mål provioder vara korrekt konfigurerad med en väg för "associationer"</span><span class="sxs-lookup"><span data-stu-id="2614c-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="2614c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2614c-110">PARAMETERS</span></span>

### <span data-ttu-id="2614c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2614c-111">-AsJob</span></span>
<span data-ttu-id="2614c-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="2614c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="2614c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2614c-113">-DefaultProfile</span></span>
<span data-ttu-id="2614c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2614c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2614c-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="2614c-115">-Name</span></span>
<span data-ttu-id="2614c-116">Namnet på kopplingen.</span><span class="sxs-lookup"><span data-stu-id="2614c-116">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2614c-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2614c-117">-NoWait</span></span>
<span data-ttu-id="2614c-118">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="2614c-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2614c-119">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="2614c-119">-Scope</span></span>
<span data-ttu-id="2614c-120">Associeringens omfattning.</span><span class="sxs-lookup"><span data-stu-id="2614c-120">The scope of the association.</span></span>
<span data-ttu-id="2614c-121">Omfattningen kan vara valfri giltig REST resurs instans.</span><span class="sxs-lookup"><span data-stu-id="2614c-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="2614c-122">Använd till exempel '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name} ' för en virtuell dator resurs.</span><span class="sxs-lookup"><span data-stu-id="2614c-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

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

### <span data-ttu-id="2614c-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2614c-123">-TargetResourceId</span></span>
<span data-ttu-id="2614c-124">REST-resursen för mål resursen för den här associationen.</span><span class="sxs-lookup"><span data-stu-id="2614c-124">The REST resource instance of the target resource for this association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2614c-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2614c-125">-Confirm</span></span>
<span data-ttu-id="2614c-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2614c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2614c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2614c-127">-WhatIf</span></span>
<span data-ttu-id="2614c-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2614c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2614c-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2614c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2614c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2614c-130">CommonParameters</span></span>
<span data-ttu-id="2614c-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2614c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2614c-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2614c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2614c-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2614c-133">INPUTS</span></span>

## <span data-ttu-id="2614c-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2614c-134">OUTPUTS</span></span>

### <span data-ttu-id="2614c-135">Microsoft. Azure. PowerShell. cmdletar. CustomProviders. Models. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="2614c-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="2614c-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2614c-136">NOTES</span></span>

<span data-ttu-id="2614c-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2614c-137">ALIASES</span></span>

## <span data-ttu-id="2614c-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2614c-138">RELATED LINKS</span></span>


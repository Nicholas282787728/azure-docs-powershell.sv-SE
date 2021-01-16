---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: ae630f053f6267a49477118786cf70b65782d68e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397547"
---
# <span data-ttu-id="5e81a-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="5e81a-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="5e81a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e81a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e81a-103">Skapa eller uppdatera en koppling.</span><span class="sxs-lookup"><span data-stu-id="5e81a-103">Create or update an association.</span></span>

## <span data-ttu-id="5e81a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e81a-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e81a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e81a-105">DESCRIPTION</span></span>
<span data-ttu-id="5e81a-106">Skapa eller uppdatera en koppling.</span><span class="sxs-lookup"><span data-stu-id="5e81a-106">Create or update an association.</span></span>

## <span data-ttu-id="5e81a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e81a-107">EXAMPLES</span></span>

### <span data-ttu-id="5e81a-108">Exempel 1: skapa en anpassad leverantörs koppling</span><span class="sxs-lookup"><span data-stu-id="5e81a-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="5e81a-109">Skapa en anpassad leverantörs koppling måste den associerade mål provioder vara korrekt konfigurerad med en väg för "associationer"</span><span class="sxs-lookup"><span data-stu-id="5e81a-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="5e81a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e81a-110">PARAMETERS</span></span>

### <span data-ttu-id="5e81a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e81a-111">-AsJob</span></span>
<span data-ttu-id="5e81a-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="5e81a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="5e81a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e81a-113">-DefaultProfile</span></span>
<span data-ttu-id="5e81a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e81a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e81a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="5e81a-115">-Name</span></span>
<span data-ttu-id="5e81a-116">Namnet på kopplingen.</span><span class="sxs-lookup"><span data-stu-id="5e81a-116">The name of the association.</span></span>

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

### <span data-ttu-id="5e81a-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5e81a-117">-NoWait</span></span>
<span data-ttu-id="5e81a-118">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="5e81a-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5e81a-119">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="5e81a-119">-Scope</span></span>
<span data-ttu-id="5e81a-120">Associeringens omfattning.</span><span class="sxs-lookup"><span data-stu-id="5e81a-120">The scope of the association.</span></span>
<span data-ttu-id="5e81a-121">Omfattningen kan vara valfri giltig REST resurs instans.</span><span class="sxs-lookup"><span data-stu-id="5e81a-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="5e81a-122">Använd till exempel '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name} ' för en virtuell dator resurs.</span><span class="sxs-lookup"><span data-stu-id="5e81a-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

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

### <span data-ttu-id="5e81a-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="5e81a-123">-TargetResourceId</span></span>
<span data-ttu-id="5e81a-124">REST-resursen för mål resursen för den här associationen.</span><span class="sxs-lookup"><span data-stu-id="5e81a-124">The REST resource instance of the target resource for this association.</span></span>

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

### <span data-ttu-id="5e81a-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e81a-125">-Confirm</span></span>
<span data-ttu-id="5e81a-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e81a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e81a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e81a-127">-WhatIf</span></span>
<span data-ttu-id="5e81a-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e81a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e81a-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e81a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e81a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e81a-130">CommonParameters</span></span>
<span data-ttu-id="5e81a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e81a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e81a-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e81a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e81a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e81a-133">INPUTS</span></span>

## <span data-ttu-id="5e81a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e81a-134">OUTPUTS</span></span>

### <span data-ttu-id="5e81a-135">Microsoft. Azure. PowerShell. cmdletar. CustomProviders. Models. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="5e81a-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="5e81a-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e81a-136">NOTES</span></span>

<span data-ttu-id="5e81a-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5e81a-137">ALIASES</span></span>

## <span data-ttu-id="5e81a-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e81a-138">RELATED LINKS</span></span>


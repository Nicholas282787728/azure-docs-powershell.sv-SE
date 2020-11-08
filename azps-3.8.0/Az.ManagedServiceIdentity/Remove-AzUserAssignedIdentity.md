---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 4e133ef82e61d34e4e2915a37cc3f0e0d1e61382
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091930"
---
# <span data-ttu-id="afba5-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="afba5-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="afba5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="afba5-102">SYNOPSIS</span></span>
<span data-ttu-id="afba5-103">Tar bort en tilldelad identitet.</span><span class="sxs-lookup"><span data-stu-id="afba5-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="afba5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="afba5-104">SYNTAX</span></span>

### <span data-ttu-id="afba5-105">ResourceGroupAndNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="afba5-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afba5-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afba5-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afba5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afba5-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afba5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="afba5-108">DESCRIPTION</span></span>
<span data-ttu-id="afba5-109">**Remove-AzUserAssignedIdentity** tar bort den angivna användarens identitet.</span><span class="sxs-lookup"><span data-stu-id="afba5-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="afba5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="afba5-110">EXAMPLES</span></span>

### <span data-ttu-id="afba5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="afba5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="afba5-112">Med den här cmdleten tar du bort identiteten **id1** under resurs grupp **PSRG**.</span><span class="sxs-lookup"><span data-stu-id="afba5-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="afba5-113">Sant</span><span class="sxs-lookup"><span data-stu-id="afba5-113">True</span></span>

## <span data-ttu-id="afba5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="afba5-114">PARAMETERS</span></span>

### <span data-ttu-id="afba5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afba5-115">-AsJob</span></span>
<span data-ttu-id="afba5-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="afba5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="afba5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afba5-117">-DefaultProfile</span></span>
<span data-ttu-id="afba5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="afba5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afba5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="afba5-119">-Force</span></span>
<span data-ttu-id="afba5-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="afba5-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="afba5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afba5-121">-InputObject</span></span>
<span data-ttu-id="afba5-122">Identity-objektet.</span><span class="sxs-lookup"><span data-stu-id="afba5-122">The Identity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afba5-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="afba5-123">-Name</span></span>
<span data-ttu-id="afba5-124">Identitets namnet.</span><span class="sxs-lookup"><span data-stu-id="afba5-124">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afba5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afba5-125">-ResourceGroupName</span></span>
<span data-ttu-id="afba5-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="afba5-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afba5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afba5-127">-ResourceId</span></span>
<span data-ttu-id="afba5-128">Identitetens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="afba5-128">The Identity's resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afba5-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="afba5-129">-Confirm</span></span>
<span data-ttu-id="afba5-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="afba5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afba5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afba5-131">-WhatIf</span></span>
<span data-ttu-id="afba5-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="afba5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afba5-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="afba5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afba5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afba5-134">CommonParameters</span></span>
<span data-ttu-id="afba5-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afba5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afba5-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afba5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afba5-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="afba5-137">INPUTS</span></span>

### <span data-ttu-id="afba5-138">Microsoft. Azure. commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="afba5-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="afba5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="afba5-139">System.String</span></span>

## <span data-ttu-id="afba5-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="afba5-140">OUTPUTS</span></span>

### <span data-ttu-id="afba5-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="afba5-141">System.Boolean</span></span>

## <span data-ttu-id="afba5-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="afba5-142">NOTES</span></span>

## <span data-ttu-id="afba5-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="afba5-143">RELATED LINKS</span></span>

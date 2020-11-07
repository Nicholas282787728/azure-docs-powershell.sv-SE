---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/remove-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 03d73ac28bc1869452ecc96b5c867fcbb8c372c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757589"
---
# <span data-ttu-id="58810-101">Remove-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="58810-101">Remove-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="58810-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58810-102">SYNOPSIS</span></span>
<span data-ttu-id="58810-103">Tar bort en tilldelad identitet.</span><span class="sxs-lookup"><span data-stu-id="58810-103">Removes a User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58810-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58810-104">SYNTAX</span></span>

### <span data-ttu-id="58810-105">ResourceGroupAndNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="58810-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58810-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58810-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58810-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58810-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58810-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58810-108">DESCRIPTION</span></span>
<span data-ttu-id="58810-109">**Remove-AzureRmUserAssignedIdentity** tar bort den angivna användarens identitet.</span><span class="sxs-lookup"><span data-stu-id="58810-109">The **Remove-AzureRmUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="58810-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58810-110">EXAMPLES</span></span>

### <span data-ttu-id="58810-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="58810-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzurRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="58810-112">Med den här cmdleten tar du bort identiteten **id1** under resurs grupp **PSRG**.</span><span class="sxs-lookup"><span data-stu-id="58810-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="58810-113">Sant</span><span class="sxs-lookup"><span data-stu-id="58810-113">True</span></span>

## <span data-ttu-id="58810-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58810-114">PARAMETERS</span></span>

### <span data-ttu-id="58810-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58810-115">-AsJob</span></span>
<span data-ttu-id="58810-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="58810-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58810-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58810-117">-DefaultProfile</span></span>
<span data-ttu-id="58810-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="58810-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58810-119">-Force</span><span class="sxs-lookup"><span data-stu-id="58810-119">-Force</span></span>
<span data-ttu-id="58810-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="58810-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="58810-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58810-121">-InputObject</span></span>
<span data-ttu-id="58810-122">Identity-objektet.</span><span class="sxs-lookup"><span data-stu-id="58810-122">The Identity object.</span></span>

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

### <span data-ttu-id="58810-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="58810-123">-Name</span></span>
<span data-ttu-id="58810-124">Identitets namnet.</span><span class="sxs-lookup"><span data-stu-id="58810-124">The Identity name.</span></span>

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

### <span data-ttu-id="58810-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58810-125">-ResourceGroupName</span></span>
<span data-ttu-id="58810-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="58810-126">The resource group name.</span></span>

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

### <span data-ttu-id="58810-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58810-127">-ResourceId</span></span>
<span data-ttu-id="58810-128">Identitetens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="58810-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="58810-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="58810-129">-Confirm</span></span>
<span data-ttu-id="58810-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="58810-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58810-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58810-131">-WhatIf</span></span>
<span data-ttu-id="58810-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="58810-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58810-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="58810-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58810-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58810-134">CommonParameters</span></span>
<span data-ttu-id="58810-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58810-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58810-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58810-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58810-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58810-137">INPUTS</span></span>

### <span data-ttu-id="58810-138">Microsoft. Azure. commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="58810-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>
<span data-ttu-id="58810-139">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="58810-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="58810-140">System. String</span><span class="sxs-lookup"><span data-stu-id="58810-140">System.String</span></span>

## <span data-ttu-id="58810-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58810-141">OUTPUTS</span></span>

### <span data-ttu-id="58810-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58810-142">System.Boolean</span></span>

## <span data-ttu-id="58810-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58810-143">NOTES</span></span>

## <span data-ttu-id="58810-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58810-144">RELATED LINKS</span></span>

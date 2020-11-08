---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
ms.openlocfilehash: 1f165177871a2d8b425829dddaef6d1f0298cfb4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270924"
---
# <span data-ttu-id="ee5b9-101">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ee5b9-101">New-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="ee5b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee5b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ee5b9-103">Skapar en ny användardefinierad identitet eller uppdaterar en befintlig tilldelad användares identitet.</span><span class="sxs-lookup"><span data-stu-id="ee5b9-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

## <span data-ttu-id="ee5b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee5b9-104">SYNTAX</span></span>

```
New-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee5b9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee5b9-105">DESCRIPTION</span></span>
<span data-ttu-id="ee5b9-106">Cmdleten **New-AzUserAssignedIdentity** skapar en ny tilldelad identitet.</span><span class="sxs-lookup"><span data-stu-id="ee5b9-106">The **New-AzUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="ee5b9-107">När den används med en befintlig identitet har den uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="ee5b9-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="ee5b9-108">Använd Set-AzResource cmdlet för att lägga till Azure Resource Manager-taggar till identiteten.</span><span class="sxs-lookup"><span data-stu-id="ee5b9-108">To add Azure Resource Manager tags to the identity, please use the Set-AzResource cmdlet.</span></span>

## <span data-ttu-id="ee5b9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee5b9-109">EXAMPLES</span></span>

### <span data-ttu-id="ee5b9-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ee5b9-110">Example 1</span></span>
<span data-ttu-id="ee5b9-111">Med den här cmdleten skapas en ny användare tilldelad identitet med namnet **id1** under resurs grupp **PSRG** i ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee5b9-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : centralus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="ee5b9-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ee5b9-112">Example 2</span></span>
<span data-ttu-id="ee5b9-113">Med den här cmdleten skapar du en ny användare tilldelad identitet med namnet **id1** under resurs gruppen **PSRG** i regionen region.</span><span class="sxs-lookup"><span data-stu-id="ee5b9-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1 -Location westus

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="ee5b9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee5b9-114">PARAMETERS</span></span>

### <span data-ttu-id="ee5b9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee5b9-115">-AsJob</span></span>
<span data-ttu-id="ee5b9-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ee5b9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee5b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee5b9-117">-DefaultProfile</span></span>
<span data-ttu-id="ee5b9-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee5b9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee5b9-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="ee5b9-119">-Location</span></span>
<span data-ttu-id="ee5b9-120">Det Azure region namn där identiteten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ee5b9-120">The Azure region name where the Identity should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee5b9-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ee5b9-121">-Name</span></span>
<span data-ttu-id="ee5b9-122">Identitets namnet.</span><span class="sxs-lookup"><span data-stu-id="ee5b9-122">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee5b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee5b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee5b9-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ee5b9-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee5b9-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ee5b9-125">-Tag</span></span>
<span data-ttu-id="ee5b9-126">Azure Resource Manager-märkningen som är associerad med identiteten.</span><span class="sxs-lookup"><span data-stu-id="ee5b9-126">The Azure Resource Manager tags associated with the identity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee5b9-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee5b9-127">-Confirm</span></span>
<span data-ttu-id="ee5b9-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee5b9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee5b9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee5b9-129">-WhatIf</span></span>
<span data-ttu-id="ee5b9-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ee5b9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee5b9-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ee5b9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee5b9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee5b9-132">CommonParameters</span></span>
<span data-ttu-id="ee5b9-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee5b9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee5b9-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee5b9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee5b9-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee5b9-135">INPUTS</span></span>

### <span data-ttu-id="ee5b9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ee5b9-136">System.String</span></span>

### <span data-ttu-id="ee5b9-137">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="ee5b9-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ee5b9-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee5b9-138">OUTPUTS</span></span>

### <span data-ttu-id="ee5b9-139">Microsoft. Azure. commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ee5b9-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="ee5b9-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee5b9-140">NOTES</span></span>

## <span data-ttu-id="ee5b9-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee5b9-141">RELATED LINKS</span></span>

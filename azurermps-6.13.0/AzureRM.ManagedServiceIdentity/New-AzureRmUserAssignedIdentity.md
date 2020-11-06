---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/new-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/New-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/New-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: c0175c63a9e7a7d5df448d644783ac4b7a003e27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576924"
---
# <span data-ttu-id="397f2-101">New-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="397f2-101">New-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="397f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="397f2-102">SYNOPSIS</span></span>
<span data-ttu-id="397f2-103">Skapar en ny användardefinierad identitet eller uppdaterar en befintlig tilldelad användares identitet.</span><span class="sxs-lookup"><span data-stu-id="397f2-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="397f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="397f2-104">SYNTAX</span></span>

```
New-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="397f2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="397f2-105">DESCRIPTION</span></span>
<span data-ttu-id="397f2-106">Cmdleten **New-AzureRmUserAssignedIdentity** skapar en ny tilldelad identitet.</span><span class="sxs-lookup"><span data-stu-id="397f2-106">The **New-AzureRmUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="397f2-107">När den används med en befintlig identitet har den uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="397f2-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="397f2-108">Använd Set-AzureRmResource cmdlet för att lägga till Azure Resource Manager-taggar till identiteten.</span><span class="sxs-lookup"><span data-stu-id="397f2-108">To add Azure Resource Manager tags to the identity, please use the Set-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="397f2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="397f2-109">EXAMPLES</span></span>

### <span data-ttu-id="397f2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="397f2-110">Example 1</span></span>
<span data-ttu-id="397f2-111">Med den här cmdleten skapas en ny användare tilldelad identitet med namnet **id1** under resurs grupp **PSRG** i ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="397f2-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

```powershell
PS C:\> New-AzureRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

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

### <span data-ttu-id="397f2-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="397f2-112">Example 2</span></span>
<span data-ttu-id="397f2-113">Med den här cmdleten skapar du en ny användare tilldelad identitet med namnet **id1** under resurs gruppen **PSRG** i regionen region.</span><span class="sxs-lookup"><span data-stu-id="397f2-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

```powershell
PS C:\> New-AzureRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1 -Location westus

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

## <span data-ttu-id="397f2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="397f2-114">PARAMETERS</span></span>

### <span data-ttu-id="397f2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="397f2-115">-AsJob</span></span>
<span data-ttu-id="397f2-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="397f2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="397f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="397f2-117">-DefaultProfile</span></span>
<span data-ttu-id="397f2-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="397f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="397f2-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="397f2-119">-Location</span></span>
<span data-ttu-id="397f2-120">Det Azure region namn där identiteten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="397f2-120">The Azure region name where the Identity should be created.</span></span>

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

### <span data-ttu-id="397f2-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="397f2-121">-Name</span></span>
<span data-ttu-id="397f2-122">Identitets namnet.</span><span class="sxs-lookup"><span data-stu-id="397f2-122">The Identity name.</span></span>

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

### <span data-ttu-id="397f2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="397f2-123">-ResourceGroupName</span></span>
<span data-ttu-id="397f2-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="397f2-124">The resource group name.</span></span>

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

### <span data-ttu-id="397f2-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="397f2-125">-Tag</span></span>
<span data-ttu-id="397f2-126">Azure Resource Manager-märkningen som är associerad med identiteten.</span><span class="sxs-lookup"><span data-stu-id="397f2-126">The Azure Resource Manager tags associated with the identity.</span></span>

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

### <span data-ttu-id="397f2-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="397f2-127">-Confirm</span></span>
<span data-ttu-id="397f2-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="397f2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="397f2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="397f2-129">-WhatIf</span></span>
<span data-ttu-id="397f2-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="397f2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="397f2-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="397f2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="397f2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="397f2-132">CommonParameters</span></span>
<span data-ttu-id="397f2-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="397f2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="397f2-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="397f2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="397f2-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="397f2-135">INPUTS</span></span>

### <span data-ttu-id="397f2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="397f2-136">System.String</span></span>

### <span data-ttu-id="397f2-137">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="397f2-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="397f2-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="397f2-138">OUTPUTS</span></span>

### <span data-ttu-id="397f2-139">Microsoft. Azure. commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="397f2-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="397f2-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="397f2-140">NOTES</span></span>

## <span data-ttu-id="397f2-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="397f2-141">RELATED LINKS</span></span>

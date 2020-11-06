---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/get-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Get-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Get-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 4d28b91ec4f05b39c6e348aff17bbb1bec1a2dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577182"
---
# <span data-ttu-id="055ae-101">Get-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="055ae-101">Get-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="055ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="055ae-102">SYNOPSIS</span></span>
<span data-ttu-id="055ae-103">Hämtar en användares tilldelade identitet/identiteter.</span><span class="sxs-lookup"><span data-stu-id="055ae-103">Gets User Assigned Identity/identities.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="055ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="055ae-104">SYNTAX</span></span>

### <span data-ttu-id="055ae-105">SuscriptionParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="055ae-105">SuscriptionParameterSet (Default)</span></span>
```
Get-AzureRmUserAssignedIdentity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="055ae-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="055ae-106">ResourceGroupParameterSet</span></span>
```
Get-AzureRmUserAssignedIdentity -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="055ae-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="055ae-107">DESCRIPTION</span></span>
<span data-ttu-id="055ae-108">Med **Get-AzureRmUserAssignedIdentity** blir befintliga användare tilldelade identiteter.</span><span class="sxs-lookup"><span data-stu-id="055ae-108">The **Get-AzureRmUserAssignedIdentity** gets existing user assigned identities.</span></span>

## <span data-ttu-id="055ae-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="055ae-109">EXAMPLES</span></span>

### <span data-ttu-id="055ae-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="055ae-110">Example 1</span></span>
<span data-ttu-id="055ae-111">Med den här cmdleten får användaren en tilldelad identitet med namnet **id1** under resurs gruppen **PSRG**</span><span class="sxs-lookup"><span data-stu-id="055ae-111">This example cmdlet gets the User Assigned Identity with name **ID1** under the resource group **PSRG**</span></span>

```powershell
PS C:\> Get-AzureRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

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

### <span data-ttu-id="055ae-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="055ae-112">Example 2</span></span>
<span data-ttu-id="055ae-113">Denna exempel-cmdlet får alla användare tilldelade identiteter under resurs gruppen **PSRG**</span><span class="sxs-lookup"><span data-stu-id="055ae-113">This example cmdlet gets all the User Assigned Identities under the resource group **PSRG**</span></span>

```powershell
PS C:\> Get-AzureRmUserAssignedIdentity -ResourceGroupName PSRG

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2

ResourceGroupName : PSRG

Name              : ID2

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="055ae-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="055ae-114">Example 3</span></span>
<span data-ttu-id="055ae-115">I det här exemplet får alla användare tilldelade identiteter under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="055ae-115">This example cmdlet gets all the User Assigned Identities under the subscription.</span></span>

```powershell
PS C:\> Get-AzureRmUserAssignedIdentity

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2

ResourceGroupName : PSRG

Name              : ID2

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG2/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG2

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG2/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="055ae-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="055ae-116">PARAMETERS</span></span>

### <span data-ttu-id="055ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="055ae-117">-DefaultProfile</span></span>
<span data-ttu-id="055ae-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="055ae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055ae-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="055ae-119">-Name</span></span>
<span data-ttu-id="055ae-120">Identitets namnet.</span><span class="sxs-lookup"><span data-stu-id="055ae-120">The Identity name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055ae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="055ae-121">-ResourceGroupName</span></span>
<span data-ttu-id="055ae-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="055ae-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055ae-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="055ae-123">CommonParameters</span></span>
<span data-ttu-id="055ae-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="055ae-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="055ae-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="055ae-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="055ae-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="055ae-126">INPUTS</span></span>

### <span data-ttu-id="055ae-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="055ae-127">None</span></span>

## <span data-ttu-id="055ae-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="055ae-128">OUTPUTS</span></span>

### <span data-ttu-id="055ae-129">Microsoft. Azure. commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="055ae-129">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="055ae-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="055ae-130">NOTES</span></span>

## <span data-ttu-id="055ae-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="055ae-131">RELATED LINKS</span></span>

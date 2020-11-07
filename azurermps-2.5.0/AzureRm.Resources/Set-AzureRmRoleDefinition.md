---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 6ca98bc3a459fada4c9ec7c48c216571fb038ba4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930061"
---
# <span data-ttu-id="b840b-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b840b-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="b840b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b840b-102">SYNOPSIS</span></span>
<span data-ttu-id="b840b-103">Ändrar en anpassad roll i Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="b840b-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="b840b-104">Ange den ändrade roll definitionen antingen som en JSON-fil eller som en PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="b840b-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="b840b-105">Använd först kommandot Get-AzureRmRoleDefinition för att hämta den anpassade rollen du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="b840b-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="b840b-106">Ändra sedan de egenskaper du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="b840b-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="b840b-107">Spara sedan roll definitionen med det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="b840b-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b840b-108">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b840b-108">SYNTAX</span></span>

### <span data-ttu-id="b840b-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="b840b-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b840b-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b840b-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b840b-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b840b-111">DESCRIPTION</span></span>
<span data-ttu-id="b840b-112">Set-AzureRmRoleDefinition cmdlet uppdaterar en befintlig anpassad roll i Azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="b840b-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="b840b-113">Ange den uppdaterade roll definitionen som indata för kommandot som en JSON-fil eller ett PSRoleDefinition-objekt.</span><span class="sxs-lookup"><span data-stu-id="b840b-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="b840b-114">Roll definitionen för den uppdaterade anpassade rollen måste innehålla ID och alla andra obligatoriska egenskaper för rollen även om de inte har uppdaterats: DisplayName, beskrivning, åtgärder, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="b840b-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="b840b-115">NotActions, DataActions, NotDataActions är valfria.</span><span class="sxs-lookup"><span data-stu-id="b840b-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="b840b-116">Nedan följer ett exempel på en uppdaterad roll definition JSON för Set-AzureRmRoleDefinition {"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "namn": "uppdaterad roll", "Beskrivning": "kan övervaka alla resurser och starta och starta om virtuella datorer", "åtgärder": \[ " */Read", "Microsoft. ClassicCompute/virtualmachines/restart/Action", "Microsoft. ClassicCompute/virtualmachines/start/åtgärd" \] , "NotActions": \[ "* /Write" \] , "DataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/container/BLOB/Read" \] , "NotDataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/container/blobbar/Write" \] , "AssignableScopes": \[ "/Subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX" \] }</span><span class="sxs-lookup"><span data-stu-id="b840b-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="b840b-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b840b-117">EXAMPLES</span></span>

### <span data-ttu-id="b840b-118">Uppdatera med PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="b840b-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="b840b-119">Skapa med en JSON-fil</span><span class="sxs-lookup"><span data-stu-id="b840b-119">Create using JSON file</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="b840b-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b840b-120">PARAMETERS</span></span>

### <span data-ttu-id="b840b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b840b-121">-DefaultProfile</span></span>
<span data-ttu-id="b840b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b840b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b840b-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="b840b-123">-InputFile</span></span>
<span data-ttu-id="b840b-124">Fil namn som innehåller en enda JSON-serverroll som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="b840b-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="b840b-125">Inkludera bara egenskaperna som ska uppdateras i JSON.</span><span class="sxs-lookup"><span data-stu-id="b840b-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="b840b-126">Egenskapen ID är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b840b-126">Id property is Required.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b840b-127">-Roll</span><span class="sxs-lookup"><span data-stu-id="b840b-127">-Role</span></span>
<span data-ttu-id="b840b-128">Roll definitions objekt som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="b840b-128">Role definition object to be updated</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b840b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b840b-129">CommonParameters</span></span>
<span data-ttu-id="b840b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b840b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b840b-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b840b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b840b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b840b-132">INPUTS</span></span>

### <span data-ttu-id="b840b-133">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b840b-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="b840b-134">Parametrar: roll (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b840b-134">Parameters: Role (ByValue)</span></span>

## <span data-ttu-id="b840b-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b840b-135">OUTPUTS</span></span>

### <span data-ttu-id="b840b-136">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b840b-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="b840b-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b840b-137">NOTES</span></span>
<span data-ttu-id="b840b-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="b840b-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b840b-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b840b-139">RELATED LINKS</span></span>

[<span data-ttu-id="b840b-140">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="b840b-140">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="b840b-141">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b840b-141">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="b840b-142">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b840b-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="b840b-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b840b-143">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)


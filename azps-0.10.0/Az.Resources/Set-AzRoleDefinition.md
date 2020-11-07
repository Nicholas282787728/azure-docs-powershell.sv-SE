---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: 79ff5a54da704e66895e280c8a2e8a93731d2083
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923754"
---
# <span data-ttu-id="3705b-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3705b-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="3705b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3705b-102">SYNOPSIS</span></span>
<span data-ttu-id="3705b-103">Ändrar en anpassad roll i Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="3705b-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="3705b-104">Ange den ändrade roll definitionen antingen som en JSON-fil eller som en PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="3705b-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="3705b-105">Använd först kommandot Get-AzRoleDefinition för att hämta den anpassade rollen du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="3705b-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="3705b-106">Ändra sedan de egenskaper du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="3705b-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="3705b-107">Spara sedan roll definitionen med det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="3705b-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="3705b-108">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3705b-108">SYNTAX</span></span>

### <span data-ttu-id="3705b-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3705b-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3705b-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3705b-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3705b-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3705b-111">DESCRIPTION</span></span>
<span data-ttu-id="3705b-112">Set-AzRoleDefinition cmdlet uppdaterar en befintlig anpassad roll i Azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="3705b-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="3705b-113">Ange den uppdaterade roll definitionen som indata för kommandot som en JSON-fil eller ett PSRoleDefinition-objekt.</span><span class="sxs-lookup"><span data-stu-id="3705b-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="3705b-114">Roll definitionen för den uppdaterade anpassade rollen måste innehålla ID och alla andra obligatoriska egenskaper för rollen även om de inte har uppdaterats: DisplayName, beskrivning, åtgärder, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="3705b-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="3705b-115">NotActions, DataActions, NotDataActions är valfria.</span><span class="sxs-lookup"><span data-stu-id="3705b-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="3705b-116">Nedan följer ett exempel på en uppdaterad roll definition JSON för Set-AzRoleDefinition {"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "namn": "uppdaterad roll", "Beskrivning": "kan övervaka alla resurser och starta och starta om virtuella datorer", "åtgärder": \[ " */Read", "Microsoft. ClassicCompute/virtualmachines/restart/Action", "Microsoft. ClassicCompute/virtualmachines/start/åtgärd" \] , "NotActions": \[ "* /Write" \] , "DataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/container/BLOB/Read" \] , "NotDataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/container/blobbar/Write" \] , "AssignableScopes": \[ "/Subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX" \] }</span><span class="sxs-lookup"><span data-stu-id="3705b-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="3705b-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3705b-117">EXAMPLES</span></span>

### <span data-ttu-id="3705b-118">Uppdatera med PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="3705b-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="3705b-119">Skapa med en JSON-fil</span><span class="sxs-lookup"><span data-stu-id="3705b-119">Create using JSON file</span></span>
```
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="3705b-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3705b-120">PARAMETERS</span></span>

### <span data-ttu-id="3705b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3705b-121">-DefaultProfile</span></span>
<span data-ttu-id="3705b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3705b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3705b-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="3705b-123">-InputFile</span></span>
<span data-ttu-id="3705b-124">Fil namn som innehåller en enda JSON-serverroll som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="3705b-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="3705b-125">Inkludera bara egenskaperna som ska uppdateras i JSON.</span><span class="sxs-lookup"><span data-stu-id="3705b-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="3705b-126">Egenskapen ID är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="3705b-126">Id property is Required.</span></span>

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

### <span data-ttu-id="3705b-127">-Roll</span><span class="sxs-lookup"><span data-stu-id="3705b-127">-Role</span></span>
<span data-ttu-id="3705b-128">Roll definitions objekt som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="3705b-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="3705b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3705b-129">CommonParameters</span></span>
<span data-ttu-id="3705b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3705b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3705b-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3705b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3705b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3705b-132">INPUTS</span></span>

### <span data-ttu-id="3705b-133">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3705b-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="3705b-134">Parametrar: roll (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3705b-134">Parameters: Role (ByValue)</span></span>

## <span data-ttu-id="3705b-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3705b-135">OUTPUTS</span></span>

### <span data-ttu-id="3705b-136">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3705b-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="3705b-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3705b-137">NOTES</span></span>
<span data-ttu-id="3705b-138">Nyckelord: Azure, AZ, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="3705b-138">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3705b-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3705b-139">RELATED LINKS</span></span>

[<span data-ttu-id="3705b-140">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="3705b-140">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="3705b-141">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3705b-141">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="3705b-142">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3705b-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="3705b-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3705b-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399280"
---
# <span data-ttu-id="00ce9-101">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="00ce9-101">New-AzRoleDefinition</span></span>

## <span data-ttu-id="00ce9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="00ce9-103">Skapar en anpassad roll i Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="00ce9-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="00ce9-104">Ange antingen en definitions fil för JSON-roll eller ett PSRoleDefinition-objekt som indata.</span><span class="sxs-lookup"><span data-stu-id="00ce9-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="00ce9-105">Använd först kommandot Get-AzRoleDefinition för att skapa ett definitions objekt för bas linje.</span><span class="sxs-lookup"><span data-stu-id="00ce9-105">First, use the Get-AzRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="00ce9-106">Ändra sedan dess egenskaper efter behov.</span><span class="sxs-lookup"><span data-stu-id="00ce9-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="00ce9-107">Använd sedan det här kommandot för att skapa en anpassad roll med roll definition.</span><span class="sxs-lookup"><span data-stu-id="00ce9-107">Finally, use this command to create a custom role using role definition.</span></span>

## <span data-ttu-id="00ce9-108">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00ce9-108">SYNTAX</span></span>

### <span data-ttu-id="00ce9-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="00ce9-109">InputFileParameterSet</span></span>
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00ce9-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="00ce9-110">RoleDefinitionParameterSet</span></span>
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00ce9-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00ce9-111">DESCRIPTION</span></span>
<span data-ttu-id="00ce9-112">New-AzRoleDefinition cmdlet skapar en anpassad roll i Azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="00ce9-112">The New-AzRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="00ce9-113">Ange en roll definition som indata för kommandot som en JSON-fil eller ett PSRoleDefinition-objekt.</span><span class="sxs-lookup"><span data-stu-id="00ce9-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="00ce9-114">Definitionen av en indatafil måste innehålla följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="00ce9-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="00ce9-115">DisplayName: namnet på den anpassade rollen</span><span class="sxs-lookup"><span data-stu-id="00ce9-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="00ce9-116">Beskrivning: en kort beskrivning av den roll som sammanfattar den åtkomst som rollen ger.</span><span class="sxs-lookup"><span data-stu-id="00ce9-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="00ce9-117">Åtgärder: den uppsättning operationer som den anpassade rollen ger åtkomst till.</span><span class="sxs-lookup"><span data-stu-id="00ce9-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="00ce9-118">Använd Get-AzProviderOperation för att få den funktion för Azure Resource provider som kan säkras med Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="00ce9-118">Use Get-AzProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="00ce9-119">Här är några giltiga åtgärds strängar:</span><span class="sxs-lookup"><span data-stu-id="00ce9-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="00ce9-120">"\*/Read" beviljar åtkomst till Läs åtgärder för alla Azure Resource providers.</span><span class="sxs-lookup"><span data-stu-id="00ce9-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="00ce9-121">"Microsoft. Network/\*/Read" beviljar åtkomst till Läs åtgärder för alla resurs typer i Microsoft. Network Resource Provider för Azure.</span><span class="sxs-lookup"><span data-stu-id="00ce9-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="00ce9-122">"Microsoft. Compute/virtualMachines/\*" beviljar åtkomst till alla åtgärder för virtuella datorer och dess underordnade resurs typer.</span><span class="sxs-lookup"><span data-stu-id="00ce9-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="00ce9-123">AssignableScopes: uppsättningen med omfattningar (Azure-prenumerationer eller resurs grupper) där den anpassade rollen ska vara tillgänglig för tilldelning.</span><span class="sxs-lookup"><span data-stu-id="00ce9-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="00ce9-124">Med AssignableScopes kan du göra den anpassade rollen tillgänglig för tilldelning i endast de abonnemang eller resurs grupper som behöver den, och inte rörigt användar upplevelsen för resten av abonnemangen eller resurs grupperna.</span><span class="sxs-lookup"><span data-stu-id="00ce9-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="00ce9-125">Här är några giltiga tilldelnings bara scope:</span><span class="sxs-lookup"><span data-stu-id="00ce9-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="00ce9-126">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/Subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": gör rollen tillgänglig för tilldelning i två prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="00ce9-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="00ce9-127">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": gör rollen tillgänglig för tilldelning i ett enda abonnemang.</span><span class="sxs-lookup"><span data-stu-id="00ce9-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="00ce9-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": gör rollen tillgänglig endast för tilldelning i nätverks resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="00ce9-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="00ce9-129">Definitionen av en indatafil kan innehålla följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="00ce9-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="00ce9-130">NotActions: den uppsättning operationer som måste undantas från åtgärderna för att fastställa de effektiva åtgärderna för den anpassade rollen.</span><span class="sxs-lookup"><span data-stu-id="00ce9-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="00ce9-131">Om det finns en specifik åtgärd som du inte vill ge åtkomst till i en anpassad roll är det praktiskt att använda NotActions för att utesluta den, i stället för att ange alla andra åtgärder än den specifika åtgärden i åtgärder.</span><span class="sxs-lookup"><span data-stu-id="00ce9-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="00ce9-132">DataActions: den uppsättning data åtgärder som den anpassade rollen ger åtkomst till.</span><span class="sxs-lookup"><span data-stu-id="00ce9-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="00ce9-133">NotDataActions: den uppsättning operationer som måste undantas från DataActions för att fastställa de effektiva data åtgärderna för den anpassade rollen.</span><span class="sxs-lookup"><span data-stu-id="00ce9-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective data actions for the custom role.</span></span>
<span data-ttu-id="00ce9-134">Om det finns en specifik data åtgärd som du inte vill ge åtkomst till i en anpassad roll är det lämpligt att använda NotDataActions för att utesluta den, i stället för att ange alla andra åtgärder än den specifika åtgärden i åtgärder.</span><span class="sxs-lookup"><span data-stu-id="00ce9-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="00ce9-135">OBS! om en användare har tilldelats en roll som anger en åtgärd i NotActions och även har tilldelats en annan roll som beviljar åtkomst till samma åtgärd – användaren kan utföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="00ce9-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="00ce9-136">NotActions är inte en regel för neka-det är ett bekvämt sätt att skapa en uppsättning tillåtna operationer när specifika operationer måste uteslutas.</span><span class="sxs-lookup"><span data-stu-id="00ce9-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="00ce9-137">Nedan följer ett exempel på en JSON-rolltjänsten som kan tillhandahållas som indata {"namn": "uppdaterad roll", "Beskrivning": "kan övervaka alla resurser och starta och starta om virtuella datorer", "åtgärder": \[ "*/Read", "Microsoft. ClassicCompute/virtualmachines/restart/Action", "Microsoft. ClassicCompute/virtualmachines/start/åtgärd" \] , "NotActions": \[ "*/Write" \] , "DataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/container/BLOB/Read" \] , "NotDataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/container/blobbar/Write" \] , "AssignableScopes": \[ "/Subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX" \] }</span><span class="sxs-lookup"><span data-stu-id="00ce9-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="00ce9-138">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00ce9-138">EXAMPLES</span></span>

### <span data-ttu-id="00ce9-139">Exempel 1: skapa med PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="00ce9-139">Example 1: Create using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### <span data-ttu-id="00ce9-140">Exempel 2: skapa med en JSON-fil</span><span class="sxs-lookup"><span data-stu-id="00ce9-140">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="00ce9-141">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00ce9-141">PARAMETERS</span></span>

### <span data-ttu-id="00ce9-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ce9-142">-DefaultProfile</span></span>
<span data-ttu-id="00ce9-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="00ce9-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00ce9-144">-InputFile</span><span class="sxs-lookup"><span data-stu-id="00ce9-144">-InputFile</span></span>
<span data-ttu-id="00ce9-145">Fil namn som innehåller en enda JSON-serverroll.</span><span class="sxs-lookup"><span data-stu-id="00ce9-145">File name containing a single json role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ce9-146">-Roll</span><span class="sxs-lookup"><span data-stu-id="00ce9-146">-Role</span></span>
<span data-ttu-id="00ce9-147">Roll definitions objekt.</span><span class="sxs-lookup"><span data-stu-id="00ce9-147">Role definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ce9-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ce9-148">CommonParameters</span></span>
<span data-ttu-id="00ce9-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00ce9-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ce9-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00ce9-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ce9-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00ce9-151">INPUTS</span></span>

### <span data-ttu-id="00ce9-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="00ce9-152">None</span></span>

## <span data-ttu-id="00ce9-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00ce9-153">OUTPUTS</span></span>

### <span data-ttu-id="00ce9-154">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="00ce9-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="00ce9-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00ce9-155">NOTES</span></span>
<span data-ttu-id="00ce9-156">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="00ce9-156">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="00ce9-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00ce9-157">RELATED LINKS</span></span>

[<span data-ttu-id="00ce9-158">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="00ce9-158">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="00ce9-159">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="00ce9-159">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="00ce9-160">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="00ce9-160">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

[<span data-ttu-id="00ce9-161">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="00ce9-161">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)


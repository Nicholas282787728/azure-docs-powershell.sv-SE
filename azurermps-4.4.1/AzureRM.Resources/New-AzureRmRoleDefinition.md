---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
ms.openlocfilehash: 23bba16ea6e80d784a9de9bfb10a3a127f53b3f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581316"
---
# <span data-ttu-id="5f526-101">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5f526-101">New-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="5f526-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f526-102">SYNOPSIS</span></span>
<span data-ttu-id="5f526-103">Skapar en anpassad roll i Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="5f526-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="5f526-104">Ange antingen en definitions fil för JSON-roll eller ett PSRoleDefinition-objekt som indata.</span><span class="sxs-lookup"><span data-stu-id="5f526-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="5f526-105">Använd först kommandot Get-AzureRmRoleDefinition för att skapa ett definitions objekt för bas linje.</span><span class="sxs-lookup"><span data-stu-id="5f526-105">First, use the Get-AzureRmRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="5f526-106">Ändra sedan dess egenskaper efter behov.</span><span class="sxs-lookup"><span data-stu-id="5f526-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="5f526-107">Använd sedan det här kommandot för att skapa en anpassad roll med roll definition.</span><span class="sxs-lookup"><span data-stu-id="5f526-107">Finally, use this command to create a custom role using role definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f526-108">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f526-108">SYNTAX</span></span>

### <span data-ttu-id="5f526-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f526-109">InputFileParameterSet</span></span>
```
New-AzureRmRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f526-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f526-110">RoleDefinitionParameterSet</span></span>
```
New-AzureRmRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f526-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f526-111">DESCRIPTION</span></span>
<span data-ttu-id="5f526-112">New-AzureRmRoleDefinition cmdlet skapar en anpassad roll i Azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="5f526-112">The New-AzureRmRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="5f526-113">Ange en roll definition som indata för kommandot som en JSON-fil eller ett PSRoleDefinition-objekt.</span><span class="sxs-lookup"><span data-stu-id="5f526-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>

<span data-ttu-id="5f526-114">Definitionen av en indatafil måste innehålla följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="5f526-114">The input role definition MUST contain the following properties:</span></span>

1) <span data-ttu-id="5f526-115">DisplayName: namnet på den anpassade rollen</span><span class="sxs-lookup"><span data-stu-id="5f526-115">DisplayName: the name of the custom role</span></span>

2) <span data-ttu-id="5f526-116">Beskrivning: en kort beskrivning av den roll som sammanfattar den åtkomst som rollen ger.</span><span class="sxs-lookup"><span data-stu-id="5f526-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>

3) <span data-ttu-id="5f526-117">Åtgärder: den uppsättning operationer som den anpassade rollen ger åtkomst till.</span><span class="sxs-lookup"><span data-stu-id="5f526-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="5f526-118">Använd Get-AzureRmProviderOperations för att få den funktion för Azure Resource provider som kan säkras med Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="5f526-118">Use Get-AzureRmProviderOperations to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="5f526-119">Här är några giltiga åtgärds strängar:</span><span class="sxs-lookup"><span data-stu-id="5f526-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="5f526-120">"\*/Read" beviljar åtkomst till Läs åtgärder för alla Azure Resource providers.</span><span class="sxs-lookup"><span data-stu-id="5f526-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="5f526-121">"Microsoft. Network/\*/Read" beviljar åtkomst till Läs åtgärder för alla resurs typer i Microsoft. Network Resource Provider för Azure.</span><span class="sxs-lookup"><span data-stu-id="5f526-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="5f526-122">"Microsoft. Compute/virtualMachines/\*" beviljar åtkomst till alla åtgärder för virtuella datorer och dess underordnade resurs typer.</span><span class="sxs-lookup"><span data-stu-id="5f526-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>

4) <span data-ttu-id="5f526-123">AssignableScopes: uppsättningen med omfattningar (Azure-prenumerationer eller resurs grupper) där den anpassade rollen ska vara tillgänglig för tilldelning.</span><span class="sxs-lookup"><span data-stu-id="5f526-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="5f526-124">Med AssignableScopes kan du göra den anpassade rollen tillgänglig för tilldelning i endast de abonnemang eller resurs grupper som behöver den, och inte rörigt användar upplevelsen för resten av abonnemangen eller resurs grupperna.</span><span class="sxs-lookup"><span data-stu-id="5f526-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="5f526-125">Här är några giltiga tilldelnings bara scope:</span><span class="sxs-lookup"><span data-stu-id="5f526-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="5f526-126">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/Subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": gör rollen tillgänglig för tilldelning i två prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="5f526-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="5f526-127">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": gör rollen tillgänglig för tilldelning i ett enda abonnemang.</span><span class="sxs-lookup"><span data-stu-id="5f526-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="5f526-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": gör rollen tillgänglig endast för tilldelning i nätverks resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5f526-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>

<span data-ttu-id="5f526-129">Definitionen av en indatafil kan innehålla följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="5f526-129">The input role definition MAY contain the following properties:</span></span>

1) <span data-ttu-id="5f526-130">NotActions: den uppsättning operationer som måste undantas från åtgärderna för att fastställa de effektiva åtgärderna för den anpassade rollen.</span><span class="sxs-lookup"><span data-stu-id="5f526-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="5f526-131">Om det finns en specifik åtgärd som du inte vill ge åtkomst till i en anpassad roll är det praktiskt att använda NotActions för att utesluta den, i stället för att ange alla andra åtgärder än den specifika åtgärden i åtgärder.</span><span class="sxs-lookup"><span data-stu-id="5f526-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>

<span data-ttu-id="5f526-132">OBS! om en användare har tilldelats en roll som anger en åtgärd i NotActions och även har tilldelats en annan roll som beviljar åtkomst till samma åtgärd – användaren kan utföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="5f526-132">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="5f526-133">NotActions är inte en regel för neka-det är ett bekvämt sätt att skapa en uppsättning tillåtna operationer när specifika operationer måste uteslutas.</span><span class="sxs-lookup"><span data-stu-id="5f526-133">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>

<span data-ttu-id="5f526-134">Nedan följer ett exempel på en JSON-rolltjänsten som kan tillhandahållas som indata {"namn": "contoso On-Call", "Beskrivning": "kan övervaka beräkning, nätverk och lagring och starta om virtuella datorer", "åtgärder": \[ "Microsoft. Compute/ */Read", "Microsoft. Compute/virtualMachines/start/Action", "Microsoft. Compute/virtualMachines/restart/Action", "Microsoft. Compute/VirtualMachines/downloadRemoteDesktopConnectionFile/Action", "Microsoft. Network/* /Read", "Microsoft. Storage/ */Read", "Microsoft. Authorization/* /Read", "Microsoft. Resources/prenumerationer/resourceGroups/Read", "Microsoft. Resources/abonnemang/resourceGroups/Resources", "Microsoft. Insights/alertRules" *, "Microsoft. support/* " \] , "AssignableScopes": \[ "/Subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", "/Subscriptions/yyyyyyyy-yyyy-yyyy-yyyy-YYYYYYYYYYYY" \] }</span><span class="sxs-lookup"><span data-stu-id="5f526-134">Following is a sample json role definition that can be provided as input { "Name": "Contoso On-call", "Description": "Can monitor compute, network and storage, and restart virtual machines", "Actions": \[ "Microsoft.Compute/ */read", "Microsoft.Compute/virtualMachines/start/action", "Microsoft.Compute/virtualMachines/restart/action", "Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action", "Microsoft.Network/* /read", "Microsoft.Storage/ */read", "Microsoft.Authorization/* /read", "Microsoft.Resources/subscriptions/resourceGroups/read", "Microsoft.Resources/subscriptions/resourceGroups/resources/read", "Microsoft.Insights/alertRules/ *", "Microsoft.Support/* " \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx","/subscriptions/yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy"\] }</span></span>

## <span data-ttu-id="5f526-135">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f526-135">EXAMPLES</span></span>

### <span data-ttu-id="5f526-136">--------------------------Skapa med PSRoleDefinitionObject--------------------------</span><span class="sxs-lookup"><span data-stu-id="5f526-136">--------------------------  Create using PSRoleDefinitionObject  --------------------------</span></span>
```
PS C:\> $role = Get-AzureRmRoleDefinition -Name "Virtual Machine Contributor"
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
          PS C:\> $role.AssignableScopes.Add("/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e")

          PS C:\> New-AzureRmRoleDefinition -Role $role
```

### <span data-ttu-id="5f526-137">--------------------------Skapa med hjälp av JSON-filen--------------------------</span><span class="sxs-lookup"><span data-stu-id="5f526-137">--------------------------  Create using JSON file  --------------------------</span></span>
```
PS C:\> New-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="5f526-138">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f526-138">PARAMETERS</span></span>

### <span data-ttu-id="5f526-139">-InputFile</span><span class="sxs-lookup"><span data-stu-id="5f526-139">-InputFile</span></span>
<span data-ttu-id="5f526-140">Fil namn som innehåller en enda JSON-serverroll.</span><span class="sxs-lookup"><span data-stu-id="5f526-140">File name containing a single json role definition.</span></span>

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

### <span data-ttu-id="5f526-141">-Roll</span><span class="sxs-lookup"><span data-stu-id="5f526-141">-Role</span></span>
<span data-ttu-id="5f526-142">Roll definitions objekt.</span><span class="sxs-lookup"><span data-stu-id="5f526-142">Role definition object.</span></span>

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

### <span data-ttu-id="5f526-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f526-143">-DefaultProfile</span></span>
<span data-ttu-id="5f526-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f526-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f526-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f526-145">CommonParameters</span></span>
<span data-ttu-id="5f526-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f526-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f526-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f526-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f526-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f526-148">INPUTS</span></span>

## <span data-ttu-id="5f526-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f526-149">OUTPUTS</span></span>

### <span data-ttu-id="5f526-150">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5f526-150">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="5f526-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f526-151">NOTES</span></span>
<span data-ttu-id="5f526-152">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="5f526-152">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5f526-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f526-153">RELATED LINKS</span></span>

[<span data-ttu-id="5f526-154">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="5f526-154">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="5f526-155">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5f526-155">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="5f526-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5f526-156">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

[<span data-ttu-id="5f526-157">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5f526-157">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)


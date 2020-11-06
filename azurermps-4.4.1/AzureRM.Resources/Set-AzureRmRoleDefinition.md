---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 9f5927905e492fd93998e12f97a97a0380755905
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577507"
---
# <span data-ttu-id="7c397-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7c397-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="7c397-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c397-102">SYNOPSIS</span></span>
<span data-ttu-id="7c397-103">Ändrar en anpassad roll i Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="7c397-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="7c397-104">Ange den ändrade roll definitionen antingen som en JSON-fil eller som en PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="7c397-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="7c397-105">Använd först kommandot Get-AzureRmRoleDefinition för att hämta den anpassade rollen du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="7c397-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="7c397-106">Ändra sedan de egenskaper du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="7c397-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="7c397-107">Spara sedan roll definitionen med det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="7c397-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c397-108">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c397-108">SYNTAX</span></span>

### <span data-ttu-id="7c397-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c397-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c397-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c397-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c397-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c397-111">DESCRIPTION</span></span>
<span data-ttu-id="7c397-112">Set-AzureRmRoleDefinition cmdlet uppdaterar en befintlig anpassad roll i Azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="7c397-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="7c397-113">Ange den uppdaterade roll definitionen som indata för kommandot som en JSON-fil eller ett PSRoleDefinition-objekt.</span><span class="sxs-lookup"><span data-stu-id="7c397-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="7c397-114">Roll definitionen för den uppdaterade anpassade rollen måste innehålla ID och alla andra obligatoriska egenskaper för rollen även om de inte har uppdaterats: DisplayName, beskrivning, åtgärder, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="7c397-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="7c397-115">NotActions är valfritt.</span><span class="sxs-lookup"><span data-stu-id="7c397-115">NotActions is optional.</span></span>

<span data-ttu-id="7c397-116">Här följer ett exempel på en uppdaterad roll definition JSON för Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7c397-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition</span></span>

<span data-ttu-id="7c397-117">{"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "namn": "uppdaterad roll", "Beskrivning": "kan övervaka alla resurser och starta och starta om virtuella datorer", "åtgärder": \[ "\*/Read", "Microsoft. ClassicCompute/virtualmachines/restart/Action", "Microsoft. ClassicCompute/virtualmachines/start/åtgärd" \] "AssignableScopes": \[ "/Subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f" \] }</span><span class="sxs-lookup"><span data-stu-id="7c397-117">{ "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "\*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] "AssignableScopes": \["/subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f"\] }</span></span>

## <span data-ttu-id="7c397-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c397-118">EXAMPLES</span></span>

### <span data-ttu-id="7c397-119">--------------------------Uppdatering med PSRoleDefinitionObject--------------------------</span><span class="sxs-lookup"><span data-stu-id="7c397-119">--------------------------  Update using PSRoleDefinitionObject  --------------------------</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/eb910d4f-edbf-429b-94F6-d76bae7ff401", "/subscriptions/a846d197-5eac-45c7-b885-a6227fe6d388")

          PS C:\> New-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="7c397-120">--------------------------Skapa med hjälp av JSON-filen--------------------------</span><span class="sxs-lookup"><span data-stu-id="7c397-120">--------------------------  Create using JSON file  --------------------------</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="7c397-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c397-121">PARAMETERS</span></span>

### <span data-ttu-id="7c397-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7c397-122">-InputFile</span></span>
<span data-ttu-id="7c397-123">Fil namn som innehåller en enda JSON-serverroll som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="7c397-123">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="7c397-124">Inkludera bara egenskaperna som ska uppdateras i JSON.</span><span class="sxs-lookup"><span data-stu-id="7c397-124">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="7c397-125">Egenskapen ID är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="7c397-125">Id property is Required.</span></span>

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

### <span data-ttu-id="7c397-126">-Roll</span><span class="sxs-lookup"><span data-stu-id="7c397-126">-Role</span></span>
<span data-ttu-id="7c397-127">Roll definitions objekt som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="7c397-127">Role definition object to be updated</span></span>

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

### <span data-ttu-id="7c397-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c397-128">-DefaultProfile</span></span>
<span data-ttu-id="7c397-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c397-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c397-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c397-130">CommonParameters</span></span>
<span data-ttu-id="7c397-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c397-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c397-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c397-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c397-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c397-133">INPUTS</span></span>

### <span data-ttu-id="7c397-134">PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7c397-134">PSRoleDefinition</span></span>
<span data-ttu-id="7c397-135">Parametern ' Role ' godkänner värdet av typen ' PSRoleDefinition ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7c397-135">Parameter 'Role' accepts value of type 'PSRoleDefinition' from the pipeline</span></span>

## <span data-ttu-id="7c397-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c397-136">OUTPUTS</span></span>

### <span data-ttu-id="7c397-137">Microsoft. Azure. kommandon. sources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7c397-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="7c397-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c397-138">NOTES</span></span>
<span data-ttu-id="7c397-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="7c397-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="7c397-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c397-140">RELATED LINKS</span></span>

[<span data-ttu-id="7c397-141">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="7c397-141">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="7c397-142">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7c397-142">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="7c397-143">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7c397-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="7c397-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7c397-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)


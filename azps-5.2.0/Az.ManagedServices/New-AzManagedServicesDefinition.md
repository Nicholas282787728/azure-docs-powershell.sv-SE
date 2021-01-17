---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: f8d2eded01e4816b99b71475aca896c697dd5ae0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415475"
---
# <span data-ttu-id="a4b5d-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="a4b5d-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="a4b5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b5d-103">Skapar eller uppdaterar en registrerings definition.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="a4b5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4b5d-104">SYNTAX</span></span>

### <span data-ttu-id="a4b5d-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="a4b5d-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -PrincipalId <String> -RoleDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4b5d-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="a4b5d-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> -PlanName <String> -PlanPublisher <String>
 -PlanProduct <String> -PlanVersion <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4b5d-107">ByAuthorization</span><span class="sxs-lookup"><span data-stu-id="a4b5d-107">ByAuthorization</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4b5d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4b5d-108">DESCRIPTION</span></span>
<span data-ttu-id="a4b5d-109">Skapar eller uppdaterar en registrerings definition.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-109">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="a4b5d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4b5d-110">EXAMPLES</span></span>

### <span data-ttu-id="a4b5d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a4b5d-111">Example 1</span></span>
```
PS C:\> New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b732e39c-c034-44cd-b5a1-094669ccc8c5 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/b732e39c-c034-44cd-b5a1-094669ccc8c5 Succeeded


PS C:\>
```

<span data-ttu-id="a4b5d-112">Skapar en registrerings definition genom roleDefinitionId-och principalId-värden som ges direkt.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-112">Creates a registration definition by roleDefinitionId and principalId values given directly.</span></span>

### <span data-ttu-id="a4b5d-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a4b5d-113">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\>
```

<span data-ttu-id="a4b5d-114">Skapar eller uppdaterar en registrerings definition med auktoriseringsinformation.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-114">Creates or updates a registration definition with authorization details.</span></span>

### <span data-ttu-id="a4b5d-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a4b5d-115">Example 3</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" },
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "9980e02c-c2be-4d73-94e8-173b1dc7cf3c"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7


PS C:\> $definition.Name
55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths -Name 55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7
714160ec-87d5-42bb-8b17-287c0dd7417d 9980e02c-c2be-4d73-94e8-173b1dc7cf3c

PS C:\>
```

<span data-ttu-id="a4b5d-116">Uppdaterar en registrerings definition med auktoriseringsinformation och namnet på registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-116">Updates a registration definition with authorization details and name of the registration definition.</span></span>

## <span data-ttu-id="a4b5d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4b5d-117">PARAMETERS</span></span>

### <span data-ttu-id="a4b5d-118">-Auktorisering</span><span class="sxs-lookup"><span data-stu-id="a4b5d-118">-Authorization</span></span>
<span data-ttu-id="a4b5d-119">Listan för auktorisering med principalId-roleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-119">The authorization mapping list with principalId - roleDefinitionId.</span></span>

```yaml
Type: Microsoft.Azure.Management.ManagedServices.Models.Authorization[]
Parameter Sets: ByPlan, ByAuthorization
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b5d-120">-DefaultProfile</span></span>
<span data-ttu-id="a4b5d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4b5d-122">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a4b5d-122">-Description</span></span>
<span data-ttu-id="a4b5d-123">Beskrivning av registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-123">The description of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5d-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a4b5d-124">-DisplayName</span></span>
<span data-ttu-id="a4b5d-125">Visnings namnet för registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-125">The display name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5d-126">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="a4b5d-126">-ManagedByTenantId</span></span>
<span data-ttu-id="a4b5d-127">ID för ManagedBy-klienten.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-127">The ManagedBy Tenant Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5d-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4b5d-128">-Name</span></span>
<span data-ttu-id="a4b5d-129">Det unika namnet på registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-129">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5d-130">-PlanName</span><span class="sxs-lookup"><span data-stu-id="a4b5d-130">-PlanName</span></span>
<span data-ttu-id="a4b5d-131">Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-131">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5d-132">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="a4b5d-132">-PlanProduct</span></span>
<span data-ttu-id="a4b5d-133">Namnet på produkten.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-133">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5d-134">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="a4b5d-134">-PlanPublisher</span></span>
<span data-ttu-id="a4b5d-135">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-135">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5d-136">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="a4b5d-136">-PlanVersion</span></span>
<span data-ttu-id="a4b5d-137">Planens versions nummer.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-137">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5d-138">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="a4b5d-138">-PrincipalId</span></span>
<span data-ttu-id="a4b5d-139">Huvud-ID för ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-139">The ManagedBy Principal Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5d-140">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a4b5d-140">-RoleDefinitionId</span></span>
<span data-ttu-id="a4b5d-141">Roll Definitions-ID för att tilldela behörigheter till huvud-ID.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-141">The role definition identifier to grant permissions to principal identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5d-142">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4b5d-142">-AsJob</span></span>
<span data-ttu-id="a4b5d-143">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a4b5d-143">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4b5d-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4b5d-144">-Confirm</span></span>
<span data-ttu-id="a4b5d-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4b5d-146">-WhatIf</span></span>
<span data-ttu-id="a4b5d-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4b5d-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b5d-149">CommonParameters</span></span>
<span data-ttu-id="a4b5d-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b5d-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4b5d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b5d-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4b5d-152">INPUTS</span></span>

### <span data-ttu-id="a4b5d-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="a4b5d-153">None</span></span>
## <span data-ttu-id="a4b5d-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4b5d-154">OUTPUTS</span></span>

### <span data-ttu-id="a4b5d-155">Microsoft. Azure. PowerShell. cmdletar. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="a4b5d-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="a4b5d-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4b5d-156">NOTES</span></span>

## <span data-ttu-id="a4b5d-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4b5d-157">RELATED LINKS</span></span>

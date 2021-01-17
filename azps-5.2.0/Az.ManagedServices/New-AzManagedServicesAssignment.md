---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: 8023dde9253ccb4a1f7ff223c4dfdddf773a4728
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415488"
---
# <span data-ttu-id="008d2-101">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="008d2-101">New-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="008d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="008d2-102">SYNOPSIS</span></span>
<span data-ttu-id="008d2-103">Skapar eller uppdaterar en registrering.</span><span class="sxs-lookup"><span data-stu-id="008d2-103">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="008d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="008d2-104">SYNTAX</span></span>

### <span data-ttu-id="008d2-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="008d2-105">Default (Default)</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="008d2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="008d2-106">ByInputObject</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>]
 -RegistrationDefinition <PSRegistrationDefinition> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="008d2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="008d2-107">DESCRIPTION</span></span>
<span data-ttu-id="008d2-108">Skapar eller uppdaterar en registrering.</span><span class="sxs-lookup"><span data-stu-id="008d2-108">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="008d2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="008d2-109">EXAMPLES</span></span>

### <span data-ttu-id="008d2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="008d2-110">Example 1</span></span>
```
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded

PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\>
```

<span data-ttu-id="008d2-111">Skapar en registrerings tilldelning med standard omfånget med hjälp av ID för registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="008d2-111">Creates a registration assignment at the default scope using the registration definition identifier.</span></span>

### <span data-ttu-id="008d2-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="008d2-112">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinition $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b279ec53-b42f-4952-bd62-cd49982e9572 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/b279ec53-b42f-4952-bd62-cd49982e9572 Succeeded


PS C:\>
```

<span data-ttu-id="008d2-113">Skapar en registrerings tilldelning med ett registrerings definitions objekt som indata.</span><span class="sxs-lookup"><span data-stu-id="008d2-113">Creates a registration assignment with a registration definition object as input.</span></span>

### <span data-ttu-id="008d2-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="008d2-114">Example 3</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded

PS C:\>
```

<span data-ttu-id="008d2-115">Uppdaterar en registrerings tilldelning med ID och namn för registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="008d2-115">Updates a registration assignment with a registration definition identifier and name.</span></span>


## <span data-ttu-id="008d2-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="008d2-116">PARAMETERS</span></span>

### <span data-ttu-id="008d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="008d2-117">-DefaultProfile</span></span>
<span data-ttu-id="008d2-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="008d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="008d2-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="008d2-119">-Name</span></span>
<span data-ttu-id="008d2-120">Det unika namnet på registrerings uppgiften.</span><span class="sxs-lookup"><span data-stu-id="008d2-120">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="008d2-121">-RegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="008d2-121">-RegistrationDefinition</span></span>
<span data-ttu-id="008d2-122">Indatafilen för registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="008d2-122">The registration definition input object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="008d2-123">-RegistrationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="008d2-123">-RegistrationDefinitionId</span></span>
<span data-ttu-id="008d2-124">Fullständigt resurs-ID för registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="008d2-124">The fully qualified resource id of the registration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="008d2-125">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="008d2-125">-Scope</span></span>
<span data-ttu-id="008d2-126">Omfattningen där registrerings uppgiften ska skapas.</span><span class="sxs-lookup"><span data-stu-id="008d2-126">The scope where the registration assignment should be created.</span></span>

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

### <span data-ttu-id="008d2-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="008d2-127">-AsJob</span></span>
<span data-ttu-id="008d2-128">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="008d2-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="008d2-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="008d2-129">-Confirm</span></span>
<span data-ttu-id="008d2-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="008d2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="008d2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="008d2-131">-WhatIf</span></span>
<span data-ttu-id="008d2-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="008d2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="008d2-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="008d2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="008d2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008d2-134">CommonParameters</span></span>
<span data-ttu-id="008d2-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="008d2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008d2-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="008d2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008d2-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="008d2-137">INPUTS</span></span>

### <span data-ttu-id="008d2-138">Microsoft. Azure. PowerShell. cmdletar. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="008d2-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
### <span data-ttu-id="008d2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="008d2-139">System.String</span></span>
## <span data-ttu-id="008d2-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="008d2-140">OUTPUTS</span></span>

### <span data-ttu-id="008d2-141">Microsoft. Azure. PowerShell. cmdletar. ManagedServices. Models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="008d2-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="008d2-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="008d2-142">NOTES</span></span>

## <span data-ttu-id="008d2-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="008d2-143">RELATED LINKS</span></span>

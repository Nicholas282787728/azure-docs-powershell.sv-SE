---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: a3a39db5f110f247ab58f2b4c6afcdb4536f4f50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270563"
---
# <span data-ttu-id="d0c46-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d0c46-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="d0c46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0c46-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c46-103">Tar bort en registrering.</span><span class="sxs-lookup"><span data-stu-id="d0c46-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="d0c46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0c46-104">SYNTAX</span></span>

### <span data-ttu-id="d0c46-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="d0c46-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [-Scope <String>] -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0c46-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d0c46-106">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0c46-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0c46-107">DESCRIPTION</span></span>
<span data-ttu-id="d0c46-108">Tar bort en registrering.</span><span class="sxs-lookup"><span data-stu-id="d0c46-108">Deletes a registration assignment.</span></span>

## <span data-ttu-id="d0c46-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0c46-109">EXAMPLES</span></span>

### <span data-ttu-id="d0c46-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d0c46-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80
PS C:\>
```

<span data-ttu-id="d0c46-111">Tar bort registrerings tilldelningen med namn i standard omfattningen.</span><span class="sxs-lookup"><span data-stu-id="d0c46-111">Deletes the registration assignment by name at the default scope.</span></span>

### <span data-ttu-id="d0c46-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d0c46-112">Example 2</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 12b05f0f-3426-48da-9e67-738e1dbf775f
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
PS C:\>
```

<span data-ttu-id="d0c46-113">Tar bort registrerings tilldelningen med hjälp av angivet objekt.</span><span class="sxs-lookup"><span data-stu-id="d0c46-113">Deletes the registration assignment using the input object provided.</span></span>

### <span data-ttu-id="d0c46-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="d0c46-114">Example 3</span></span>
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


PS C:\> Remove-AzManagedServicesAssignment -Name b279ec53-b42f-4952-bd62-cd49982e9572 -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8
PS C:\>
```

<span data-ttu-id="d0c46-115">Tar bort registrerings tilldelningen med namn enligt det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="d0c46-115">Deletes the registration assignment by name at the given scope.</span></span>

## <span data-ttu-id="d0c46-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0c46-116">PARAMETERS</span></span>

### <span data-ttu-id="d0c46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0c46-117">-DefaultProfile</span></span>
<span data-ttu-id="d0c46-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0c46-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0c46-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0c46-119">-InputObject</span></span>
<span data-ttu-id="d0c46-120">Objektet för registrerings tilldelning.</span><span class="sxs-lookup"><span data-stu-id="d0c46-120">The registration assignment object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0c46-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0c46-121">-Name</span></span>
<span data-ttu-id="d0c46-122">Det unika namnet på registrerings uppgiften.</span><span class="sxs-lookup"><span data-stu-id="d0c46-122">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="d0c46-123">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="d0c46-123">-Scope</span></span>
<span data-ttu-id="d0c46-124">Omfattningen av registrerings uppgiften.</span><span class="sxs-lookup"><span data-stu-id="d0c46-124">The scope of the registration assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0c46-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0c46-125">-AsJob</span></span>
<span data-ttu-id="d0c46-126">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d0c46-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0c46-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0c46-127">-Confirm</span></span>
<span data-ttu-id="d0c46-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0c46-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0c46-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0c46-129">-WhatIf</span></span>
<span data-ttu-id="d0c46-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0c46-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0c46-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0c46-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0c46-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c46-132">CommonParameters</span></span>
<span data-ttu-id="d0c46-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0c46-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c46-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0c46-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c46-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0c46-135">INPUTS</span></span>

### <span data-ttu-id="d0c46-136">Microsoft. Azure. PowerShell. cmdletar. ManagedServices. Models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="d0c46-136">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="d0c46-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0c46-137">OUTPUTS</span></span>

### <span data-ttu-id="d0c46-138">System. Void</span><span class="sxs-lookup"><span data-stu-id="d0c46-138">System.Void</span></span>
## <span data-ttu-id="d0c46-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0c46-139">NOTES</span></span>

## <span data-ttu-id="d0c46-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0c46-140">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: 6c9c4b562acbf80dba9b1b414345d5eb8e3ecc60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261256"
---
# <span data-ttu-id="9903f-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="9903f-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="9903f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9903f-102">SYNOPSIS</span></span>
<span data-ttu-id="9903f-103">Skapar eller uppdaterar en registrerings definition.</span><span class="sxs-lookup"><span data-stu-id="9903f-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="9903f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9903f-104">SYNTAX</span></span>

### <span data-ttu-id="9903f-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="9903f-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9903f-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="9903f-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] -PlanName <String>
 -PlanPublisher <String> -PlanProduct <String> -PlanVersion <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9903f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9903f-107">DESCRIPTION</span></span>
<span data-ttu-id="9903f-108">Skapar eller uppdaterar en registrerings definition.</span><span class="sxs-lookup"><span data-stu-id="9903f-108">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="9903f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9903f-109">EXAMPLES</span></span>

### <span data-ttu-id="9903f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9903f-110">Example 1</span></span>
```powershell
PS C:\> PS C:\> New-AzManagedServicesDefinition -Name name -ManagedByTenantId bab3375b-6197-4a15-a44b-16c41faa91d7 -PrincipalId d6f6c88a-5b7a-455e-ba40-ce146d4d3671 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -Description mydef

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fdad02a1-a715-4352-844f-2923233590da bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="9903f-111">Skapar eller uppdaterar en registrerings definition baserat på nödvändiga parametrar.</span><span class="sxs-lookup"><span data-stu-id="9903f-111">Creates or updates a registration definition given the required parameters.</span></span>

### <span data-ttu-id="9903f-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9903f-112">Example 2</span></span>
```powershell
PS C> New-AzManagedServicesDefinition -Name asd -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7" -PlanName plan -PlanPublisher publisher -PlanProduct product -PlanVersion 0.1

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
8cde7c19-1750-468e-973e-b711549edc35 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="9903f-113">Skapar eller uppdaterar en registrerings definition med abonnemangs informationen.</span><span class="sxs-lookup"><span data-stu-id="9903f-113">Creates or updates a registration definition with the plan details.</span></span>

## <span data-ttu-id="9903f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9903f-114">PARAMETERS</span></span>

### <span data-ttu-id="9903f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9903f-115">-AsJob</span></span>
<span data-ttu-id="9903f-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9903f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9903f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9903f-117">-DefaultProfile</span></span>
<span data-ttu-id="9903f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9903f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9903f-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="9903f-119">-Description</span></span>
<span data-ttu-id="9903f-120">Beskrivning av registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="9903f-120">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="9903f-121">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="9903f-121">-ManagedByTenantId</span></span>
<span data-ttu-id="9903f-122">ID för ManagedBy-klienten.</span><span class="sxs-lookup"><span data-stu-id="9903f-122">The ManagedBy Tenant Identifier.</span></span>

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

### <span data-ttu-id="9903f-123">-PlanName</span><span class="sxs-lookup"><span data-stu-id="9903f-123">-PlanName</span></span>
<span data-ttu-id="9903f-124">Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9903f-124">The name of the plan.</span></span>

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

### <span data-ttu-id="9903f-125">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="9903f-125">-PlanProduct</span></span>
<span data-ttu-id="9903f-126">Namnet på produkten.</span><span class="sxs-lookup"><span data-stu-id="9903f-126">The name of the Product.</span></span>

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

### <span data-ttu-id="9903f-127">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="9903f-127">-PlanPublisher</span></span>
<span data-ttu-id="9903f-128">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="9903f-128">The name of the Publisher.</span></span>

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

### <span data-ttu-id="9903f-129">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="9903f-129">-PlanVersion</span></span>
<span data-ttu-id="9903f-130">Planens versions nummer.</span><span class="sxs-lookup"><span data-stu-id="9903f-130">The version number of the plan.</span></span>

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

### <span data-ttu-id="9903f-131">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="9903f-131">-PrincipalId</span></span>
<span data-ttu-id="9903f-132">Huvud-ID för ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="9903f-132">The ManagedBy Principal Identifier.</span></span>

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

### <span data-ttu-id="9903f-133">-RegistrationDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9903f-133">-RegistrationDefinitionName</span></span>
<span data-ttu-id="9903f-134">Namnet på registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="9903f-134">The name of the Registration Definition.</span></span>

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

### <span data-ttu-id="9903f-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="9903f-135">-RoleDefinitionId</span></span>
<span data-ttu-id="9903f-136">Den hanterade tjänst leverantörens roll identifierare.</span><span class="sxs-lookup"><span data-stu-id="9903f-136">The Managed Service Provider's Role Identifier.</span></span>

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

### <span data-ttu-id="9903f-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9903f-137">-Confirm</span></span>
<span data-ttu-id="9903f-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9903f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9903f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9903f-139">-WhatIf</span></span>
<span data-ttu-id="9903f-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9903f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9903f-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9903f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9903f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9903f-142">CommonParameters</span></span>
<span data-ttu-id="9903f-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9903f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9903f-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9903f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9903f-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9903f-145">INPUTS</span></span>

### <span data-ttu-id="9903f-146">Ingen</span><span class="sxs-lookup"><span data-stu-id="9903f-146">None</span></span>

## <span data-ttu-id="9903f-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9903f-147">OUTPUTS</span></span>

### <span data-ttu-id="9903f-148">Microsoft. Azure. PowerShell. cmdletar. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="9903f-148">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="9903f-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9903f-149">NOTES</span></span>

## <span data-ttu-id="9903f-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9903f-150">RELATED LINKS</span></span>

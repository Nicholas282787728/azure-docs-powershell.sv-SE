---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: 6c9c4b562acbf80dba9b1b414345d5eb8e3ecc60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091923"
---
# <span data-ttu-id="3f4d6-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="3f4d6-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="3f4d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4d6-103">Skapar eller uppdaterar en registrerings definition.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="3f4d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f4d6-104">SYNTAX</span></span>

### <span data-ttu-id="3f4d6-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="3f4d6-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4d6-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="3f4d6-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] -PlanName <String>
 -PlanPublisher <String> -PlanProduct <String> -PlanVersion <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f4d6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f4d6-107">DESCRIPTION</span></span>
<span data-ttu-id="3f4d6-108">Skapar eller uppdaterar en registrerings definition.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-108">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="3f4d6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f4d6-109">EXAMPLES</span></span>

### <span data-ttu-id="3f4d6-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3f4d6-110">Example 1</span></span>
```powershell
PS C:\> PS C:\> New-AzManagedServicesDefinition -Name name -ManagedByTenantId bab3375b-6197-4a15-a44b-16c41faa91d7 -PrincipalId d6f6c88a-5b7a-455e-ba40-ce146d4d3671 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -Description mydef

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fdad02a1-a715-4352-844f-2923233590da bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="3f4d6-111">Skapar eller uppdaterar en registrerings definition baserat på nödvändiga parametrar.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-111">Creates or updates a registration definition given the required parameters.</span></span>

### <span data-ttu-id="3f4d6-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3f4d6-112">Example 2</span></span>
```powershell
PS C> New-AzManagedServicesDefinition -Name asd -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7" -PlanName plan -PlanPublisher publisher -PlanProduct product -PlanVersion 0.1

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
8cde7c19-1750-468e-973e-b711549edc35 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="3f4d6-113">Skapar eller uppdaterar en registrerings definition med abonnemangs informationen.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-113">Creates or updates a registration definition with the plan details.</span></span>

## <span data-ttu-id="3f4d6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f4d6-114">PARAMETERS</span></span>

### <span data-ttu-id="3f4d6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f4d6-115">-AsJob</span></span>
<span data-ttu-id="3f4d6-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3f4d6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f4d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4d6-117">-DefaultProfile</span></span>
<span data-ttu-id="3f4d6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f4d6-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3f4d6-119">-Description</span></span>
<span data-ttu-id="3f4d6-120">Beskrivning av registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-120">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="3f4d6-121">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="3f4d6-121">-ManagedByTenantId</span></span>
<span data-ttu-id="3f4d6-122">ID för ManagedBy-klienten.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-122">The ManagedBy Tenant Identifier.</span></span>

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

### <span data-ttu-id="3f4d6-123">-PlanName</span><span class="sxs-lookup"><span data-stu-id="3f4d6-123">-PlanName</span></span>
<span data-ttu-id="3f4d6-124">Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-124">The name of the plan.</span></span>

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

### <span data-ttu-id="3f4d6-125">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="3f4d6-125">-PlanProduct</span></span>
<span data-ttu-id="3f4d6-126">Namnet på produkten.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-126">The name of the Product.</span></span>

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

### <span data-ttu-id="3f4d6-127">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="3f4d6-127">-PlanPublisher</span></span>
<span data-ttu-id="3f4d6-128">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-128">The name of the Publisher.</span></span>

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

### <span data-ttu-id="3f4d6-129">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="3f4d6-129">-PlanVersion</span></span>
<span data-ttu-id="3f4d6-130">Planens versions nummer.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-130">The version number of the plan.</span></span>

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

### <span data-ttu-id="3f4d6-131">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="3f4d6-131">-PrincipalId</span></span>
<span data-ttu-id="3f4d6-132">Huvud-ID för ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-132">The ManagedBy Principal Identifier.</span></span>

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

### <span data-ttu-id="3f4d6-133">-RegistrationDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3f4d6-133">-RegistrationDefinitionName</span></span>
<span data-ttu-id="3f4d6-134">Namnet på registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-134">The name of the Registration Definition.</span></span>

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

### <span data-ttu-id="3f4d6-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3f4d6-135">-RoleDefinitionId</span></span>
<span data-ttu-id="3f4d6-136">Den hanterade tjänst leverantörens roll identifierare.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-136">The Managed Service Provider's Role Identifier.</span></span>

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

### <span data-ttu-id="3f4d6-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f4d6-137">-Confirm</span></span>
<span data-ttu-id="3f4d6-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f4d6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f4d6-139">-WhatIf</span></span>
<span data-ttu-id="3f4d6-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f4d6-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f4d6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4d6-142">CommonParameters</span></span>
<span data-ttu-id="3f4d6-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f4d6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4d6-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f4d6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4d6-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f4d6-145">INPUTS</span></span>

### <span data-ttu-id="3f4d6-146">Ingen</span><span class="sxs-lookup"><span data-stu-id="3f4d6-146">None</span></span>

## <span data-ttu-id="3f4d6-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f4d6-147">OUTPUTS</span></span>

### <span data-ttu-id="3f4d6-148">Microsoft. Azure. PowerShell. cmdletar. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="3f4d6-148">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="3f4d6-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f4d6-149">NOTES</span></span>

## <span data-ttu-id="3f4d6-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f4d6-150">RELATED LINKS</span></span>

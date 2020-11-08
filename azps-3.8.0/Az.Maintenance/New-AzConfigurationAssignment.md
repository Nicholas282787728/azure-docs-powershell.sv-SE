---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: f0c5c52773d5750b86ce82d696e9130df76f4700
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091948"
---
# <span data-ttu-id="717b0-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="717b0-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="717b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="717b0-102">SYNOPSIS</span></span>
<span data-ttu-id="717b0-103">Registrera konfiguration för resursen.</span><span class="sxs-lookup"><span data-stu-id="717b0-103">Register configuration for resource.</span></span>

## <span data-ttu-id="717b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="717b0-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="717b0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="717b0-105">DESCRIPTION</span></span>
<span data-ttu-id="717b0-106">Registrera underhålls konfiguration för resursen.</span><span class="sxs-lookup"><span data-stu-id="717b0-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="717b0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="717b0-107">EXAMPLES</span></span>

### <span data-ttu-id="717b0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="717b0-108">Example 1</span></span>
```powershell
PS C:\> New-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName -MaintenanceConfigurationId $maintenanceConfigurationCreated.Id -Location $location


Location                   : westus2
MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
ResourceId                 : 7b32ed22-dc7b-4a17-9c42-36c024f4c9f9
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="717b0-109">Registrera underhålls konfiguration för didicated värden.</span><span class="sxs-lookup"><span data-stu-id="717b0-109">Register maintenance configuration for didicated host.</span></span>

## <span data-ttu-id="717b0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="717b0-110">PARAMETERS</span></span>

### <span data-ttu-id="717b0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="717b0-111">-AsJob</span></span>
<span data-ttu-id="717b0-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="717b0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="717b0-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="717b0-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="717b0-114">Konfigurations tilldelningens namn ska matcha MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="717b0-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="717b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="717b0-115">-DefaultProfile</span></span>
<span data-ttu-id="717b0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="717b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="717b0-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="717b0-117">-Location</span></span>
<span data-ttu-id="717b0-118">Platsen utan utrymmen för resursen.</span><span class="sxs-lookup"><span data-stu-id="717b0-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="717b0-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="717b0-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="717b0-120">Den fullständigt kvalificerade MaintenanceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="717b0-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="717b0-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="717b0-121">-ProviderName</span></span>
<span data-ttu-id="717b0-122">Namnet på resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="717b0-122">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="717b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="717b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="717b0-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="717b0-124">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="717b0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="717b0-125">-ResourceId</span></span>
<span data-ttu-id="717b0-126">Konfigurations tilldelningens namn ska matcha MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="717b0-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="717b0-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="717b0-127">-ResourceName</span></span>
<span data-ttu-id="717b0-128">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="717b0-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="717b0-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="717b0-129">-ResourceParentName</span></span>
<span data-ttu-id="717b0-130">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="717b0-130">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="717b0-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="717b0-131">-ResourceParentType</span></span>
<span data-ttu-id="717b0-132">Den överordnade resurs typen.</span><span class="sxs-lookup"><span data-stu-id="717b0-132">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="717b0-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="717b0-133">-ResourceType</span></span>
<span data-ttu-id="717b0-134">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="717b0-134">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="717b0-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="717b0-135">-Confirm</span></span>
<span data-ttu-id="717b0-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="717b0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="717b0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="717b0-137">-WhatIf</span></span>
<span data-ttu-id="717b0-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="717b0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="717b0-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="717b0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="717b0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="717b0-140">CommonParameters</span></span>
<span data-ttu-id="717b0-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="717b0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="717b0-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="717b0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="717b0-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="717b0-143">INPUTS</span></span>

### <span data-ttu-id="717b0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="717b0-144">System.String</span></span>

## <span data-ttu-id="717b0-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="717b0-145">OUTPUTS</span></span>

### <span data-ttu-id="717b0-146">Microsoft. Azure. commands. Maintenance. Models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="717b0-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="717b0-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="717b0-147">NOTES</span></span>

## <span data-ttu-id="717b0-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="717b0-148">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398339"
---
# <span data-ttu-id="c117b-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="c117b-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="c117b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c117b-102">SYNOPSIS</span></span>
<span data-ttu-id="c117b-103">Registrera konfiguration för resursen.</span><span class="sxs-lookup"><span data-stu-id="c117b-103">Register configuration for resource.</span></span>

## <span data-ttu-id="c117b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c117b-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c117b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c117b-105">DESCRIPTION</span></span>
<span data-ttu-id="c117b-106">Registrera underhålls konfiguration för resursen.</span><span class="sxs-lookup"><span data-stu-id="c117b-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="c117b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c117b-107">EXAMPLES</span></span>

### <span data-ttu-id="c117b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c117b-108">Example 1</span></span>
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

<span data-ttu-id="c117b-109">Registrera underhålls konfiguration för dedikerad värd.</span><span class="sxs-lookup"><span data-stu-id="c117b-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="c117b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c117b-110">PARAMETERS</span></span>

### <span data-ttu-id="c117b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c117b-111">-AsJob</span></span>
<span data-ttu-id="c117b-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c117b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c117b-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="c117b-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="c117b-114">Konfigurations tilldelningens namn ska matcha MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="c117b-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="c117b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c117b-115">-DefaultProfile</span></span>
<span data-ttu-id="c117b-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c117b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c117b-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="c117b-117">-Location</span></span>
<span data-ttu-id="c117b-118">Platsen utan utrymmen för resursen.</span><span class="sxs-lookup"><span data-stu-id="c117b-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="c117b-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c117b-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="c117b-120">Den fullständigt kvalificerade MaintenanceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c117b-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="c117b-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="c117b-121">-ProviderName</span></span>
<span data-ttu-id="c117b-122">Namnet på resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="c117b-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="c117b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c117b-123">-ResourceGroupName</span></span>
<span data-ttu-id="c117b-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c117b-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="c117b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c117b-125">-ResourceId</span></span>
<span data-ttu-id="c117b-126">Konfigurations tilldelningens namn ska matcha MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="c117b-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="c117b-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c117b-127">-ResourceName</span></span>
<span data-ttu-id="c117b-128">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="c117b-128">The resource name.</span></span>

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

### <span data-ttu-id="c117b-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="c117b-129">-ResourceParentName</span></span>
<span data-ttu-id="c117b-130">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="c117b-130">The parent resource name.</span></span>

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

### <span data-ttu-id="c117b-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="c117b-131">-ResourceParentType</span></span>
<span data-ttu-id="c117b-132">Den överordnade resurs typen.</span><span class="sxs-lookup"><span data-stu-id="c117b-132">The parent resource type.</span></span>

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

### <span data-ttu-id="c117b-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c117b-133">-ResourceType</span></span>
<span data-ttu-id="c117b-134">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="c117b-134">The resource type.</span></span>

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

### <span data-ttu-id="c117b-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c117b-135">-Confirm</span></span>
<span data-ttu-id="c117b-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c117b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c117b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c117b-137">-WhatIf</span></span>
<span data-ttu-id="c117b-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c117b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c117b-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c117b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c117b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c117b-140">CommonParameters</span></span>
<span data-ttu-id="c117b-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c117b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c117b-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c117b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c117b-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c117b-143">INPUTS</span></span>

### <span data-ttu-id="c117b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c117b-144">System.String</span></span>

## <span data-ttu-id="c117b-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c117b-145">OUTPUTS</span></span>

### <span data-ttu-id="c117b-146">Microsoft. Azure. commands. Maintenance. Models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="c117b-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="c117b-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c117b-147">NOTES</span></span>

## <span data-ttu-id="c117b-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c117b-148">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: 137540ae71e097e98d390e2ab2efb2f6643928e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091940"
---
# <span data-ttu-id="de412-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="de412-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="de412-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de412-102">SYNOPSIS</span></span>
<span data-ttu-id="de412-103">Avregistrera konfiguration för resursen.</span><span class="sxs-lookup"><span data-stu-id="de412-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="de412-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de412-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de412-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de412-105">DESCRIPTION</span></span>
<span data-ttu-id="de412-106">Avregistrera konfiguration för resursen.</span><span class="sxs-lookup"><span data-stu-id="de412-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="de412-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de412-107">EXAMPLES</span></span>

### <span data-ttu-id="de412-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="de412-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="de412-109">Avregistrera konfiguration för resursen.</span><span class="sxs-lookup"><span data-stu-id="de412-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="de412-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de412-110">PARAMETERS</span></span>

### <span data-ttu-id="de412-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de412-111">-AsJob</span></span>
<span data-ttu-id="de412-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="de412-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de412-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="de412-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="de412-114">Konfigurations tilldelningens namn.</span><span class="sxs-lookup"><span data-stu-id="de412-114">The configuration assignment name.</span></span>

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

### <span data-ttu-id="de412-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de412-115">-DefaultProfile</span></span>
<span data-ttu-id="de412-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de412-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de412-117">-Force</span><span class="sxs-lookup"><span data-stu-id="de412-117">-Force</span></span>
<span data-ttu-id="de412-118">Tvinga bort utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="de412-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="de412-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de412-119">-PassThru</span></span>
<span data-ttu-id="de412-120">Returnerar statusen för Remove-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="de412-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="de412-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="de412-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="de412-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="de412-122">-ProviderName</span></span>
<span data-ttu-id="de412-123">Namnet på resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="de412-123">The resource provider Name.</span></span>

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

### <span data-ttu-id="de412-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de412-124">-ResourceGroupName</span></span>
<span data-ttu-id="de412-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="de412-125">The resource Group Name.</span></span>

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

### <span data-ttu-id="de412-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="de412-126">-ResourceName</span></span>
<span data-ttu-id="de412-127">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="de412-127">The resource name.</span></span>

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

### <span data-ttu-id="de412-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="de412-128">-ResourceParentName</span></span>
<span data-ttu-id="de412-129">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="de412-129">The parent resource name.</span></span>

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

### <span data-ttu-id="de412-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="de412-130">-ResourceParentType</span></span>
<span data-ttu-id="de412-131">Den överordnade resurs typen.</span><span class="sxs-lookup"><span data-stu-id="de412-131">The parent resource type.</span></span>

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

### <span data-ttu-id="de412-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="de412-132">-ResourceType</span></span>
<span data-ttu-id="de412-133">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="de412-133">The resource type.</span></span>

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

### <span data-ttu-id="de412-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de412-134">-Confirm</span></span>
<span data-ttu-id="de412-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de412-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de412-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de412-136">-WhatIf</span></span>
<span data-ttu-id="de412-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de412-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de412-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de412-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de412-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de412-139">CommonParameters</span></span>
<span data-ttu-id="de412-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de412-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de412-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de412-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de412-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de412-142">INPUTS</span></span>

### <span data-ttu-id="de412-143">System. String</span><span class="sxs-lookup"><span data-stu-id="de412-143">System.String</span></span>

## <span data-ttu-id="de412-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de412-144">OUTPUTS</span></span>

### <span data-ttu-id="de412-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de412-145">System.Boolean</span></span>

## <span data-ttu-id="de412-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de412-146">NOTES</span></span>

## <span data-ttu-id="de412-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de412-147">RELATED LINKS</span></span>
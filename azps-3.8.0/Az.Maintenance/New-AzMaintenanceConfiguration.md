---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: eb51fe99a1dbfdd5838fcd4fd5de93a5d7fb36e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091946"
---
# <span data-ttu-id="53616-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="53616-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="53616-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53616-102">SYNOPSIS</span></span>
<span data-ttu-id="53616-103">Skapa eller uppdatera konfigurations post</span><span class="sxs-lookup"><span data-stu-id="53616-103">Create or Update configuration record</span></span>

## <span data-ttu-id="53616-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53616-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53616-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53616-105">DESCRIPTION</span></span>
<span data-ttu-id="53616-106">Skapa eller uppdatera konfigurations post</span><span class="sxs-lookup"><span data-stu-id="53616-106">Create or Update configuration record</span></span>

## <span data-ttu-id="53616-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53616-107">EXAMPLES</span></span>

### <span data-ttu-id="53616-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="53616-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="53616-109">Skapa en underhålls konfiguration med scope-värden</span><span class="sxs-lookup"><span data-stu-id="53616-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="53616-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53616-110">PARAMETERS</span></span>

### <span data-ttu-id="53616-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53616-111">-AsJob</span></span>
<span data-ttu-id="53616-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="53616-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53616-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53616-113">-DefaultProfile</span></span>
<span data-ttu-id="53616-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53616-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53616-115">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="53616-115">-ExtensionProperty</span></span>
<span data-ttu-id="53616-116">Anknytnings egenskaper per resurs.</span><span class="sxs-lookup"><span data-stu-id="53616-116">The Extension properties per resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53616-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="53616-117">-Location</span></span>
<span data-ttu-id="53616-118">Platsen för underhålls konfiguration.</span><span class="sxs-lookup"><span data-stu-id="53616-118">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="53616-119">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="53616-119">-MaintenanceScope</span></span>
<span data-ttu-id="53616-120">Underhålls omfattning.</span><span class="sxs-lookup"><span data-stu-id="53616-120">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="53616-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="53616-121">-Name</span></span>
<span data-ttu-id="53616-122">Konfigurations namn för underhåll.</span><span class="sxs-lookup"><span data-stu-id="53616-122">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="53616-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53616-123">-ResourceGroupName</span></span>
<span data-ttu-id="53616-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="53616-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="53616-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="53616-125">-Tag</span></span>
<span data-ttu-id="53616-126">ARM-taggarna.</span><span class="sxs-lookup"><span data-stu-id="53616-126">The ARM Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53616-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53616-127">-Confirm</span></span>
<span data-ttu-id="53616-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53616-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53616-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53616-129">-WhatIf</span></span>
<span data-ttu-id="53616-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="53616-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53616-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="53616-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53616-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53616-132">CommonParameters</span></span>
<span data-ttu-id="53616-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53616-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53616-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53616-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53616-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53616-135">INPUTS</span></span>

### <span data-ttu-id="53616-136">System. String</span><span class="sxs-lookup"><span data-stu-id="53616-136">System.String</span></span>

## <span data-ttu-id="53616-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53616-137">OUTPUTS</span></span>

### <span data-ttu-id="53616-138">Microsoft. Azure. commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="53616-138">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="53616-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53616-139">NOTES</span></span>

## <span data-ttu-id="53616-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53616-140">RELATED LINKS</span></span>

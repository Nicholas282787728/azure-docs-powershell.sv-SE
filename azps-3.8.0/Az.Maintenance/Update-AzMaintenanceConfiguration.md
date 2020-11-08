---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: ed6f94944f00cd138d3140c2bd69029a98ea9f15
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091941"
---
# <span data-ttu-id="f84ec-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f84ec-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="f84ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f84ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f84ec-103">Konfigurations post för korrigering</span><span class="sxs-lookup"><span data-stu-id="f84ec-103">Patch configuration record</span></span>

## <span data-ttu-id="f84ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f84ec-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f84ec-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f84ec-105">DESCRIPTION</span></span>
<span data-ttu-id="f84ec-106">Konfigurations post för patch-underhåll</span><span class="sxs-lookup"><span data-stu-id="f84ec-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="f84ec-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f84ec-107">EXAMPLES</span></span>

### <span data-ttu-id="f84ec-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f84ec-108">Example 1</span></span>
```powershell
PS C:\> Update-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -Configuration $configuration


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="f84ec-109">Konfigurations post för patch-underhåll</span><span class="sxs-lookup"><span data-stu-id="f84ec-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="f84ec-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f84ec-110">PARAMETERS</span></span>

### <span data-ttu-id="f84ec-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f84ec-111">-AsJob</span></span>
<span data-ttu-id="f84ec-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f84ec-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f84ec-113">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f84ec-113">-Configuration</span></span>
<span data-ttu-id="f84ec-114">Underhålls konfigurationen uppdateras.</span><span class="sxs-lookup"><span data-stu-id="f84ec-114">The maintenance configuration to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f84ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84ec-115">-DefaultProfile</span></span>
<span data-ttu-id="f84ec-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f84ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f84ec-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f84ec-117">-Name</span></span>
<span data-ttu-id="f84ec-118">Konfigurations namn för underhåll.</span><span class="sxs-lookup"><span data-stu-id="f84ec-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="f84ec-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f84ec-119">-ResourceGroupName</span></span>
<span data-ttu-id="f84ec-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="f84ec-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="f84ec-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f84ec-121">-Confirm</span></span>
<span data-ttu-id="f84ec-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f84ec-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f84ec-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f84ec-123">-WhatIf</span></span>
<span data-ttu-id="f84ec-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f84ec-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f84ec-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f84ec-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f84ec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84ec-126">CommonParameters</span></span>
<span data-ttu-id="f84ec-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f84ec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84ec-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f84ec-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84ec-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f84ec-129">INPUTS</span></span>

### <span data-ttu-id="f84ec-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f84ec-130">System.String</span></span>

### <span data-ttu-id="f84ec-131">Microsoft. Azure. commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f84ec-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="f84ec-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f84ec-132">OUTPUTS</span></span>

### <span data-ttu-id="f84ec-133">Microsoft. Azure. commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f84ec-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="f84ec-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f84ec-134">NOTES</span></span>

## <span data-ttu-id="f84ec-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f84ec-135">RELATED LINKS</span></span>

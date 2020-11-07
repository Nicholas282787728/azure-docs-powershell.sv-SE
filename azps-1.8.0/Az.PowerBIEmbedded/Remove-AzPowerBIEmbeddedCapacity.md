---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fff76d83c3cb80c620414d07808e473ac3892e99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747531"
---
# <span data-ttu-id="36445-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="36445-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="36445-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36445-102">SYNOPSIS</span></span>
<span data-ttu-id="36445-103">Tar bort en instans av PowerBI inbäddade kapacitet.</span><span class="sxs-lookup"><span data-stu-id="36445-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="36445-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36445-104">SYNTAX</span></span>

### <span data-ttu-id="36445-105">ByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="36445-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36445-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="36445-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36445-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="36445-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36445-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36445-108">DESCRIPTION</span></span>
<span data-ttu-id="36445-109">Remove-AzPowerBIEmbeddedCapacity-cmdleten tar bort en instans av PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="36445-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="36445-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36445-110">EXAMPLES</span></span>

### <span data-ttu-id="36445-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="36445-111">Example 1</span></span>
```
PS C:\> Remove-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="36445-112">Det här kommandot tar bort kapaciteten som heter testcapacity i resourcegroup testRG</span><span class="sxs-lookup"><span data-stu-id="36445-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="36445-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36445-113">PARAMETERS</span></span>

### <span data-ttu-id="36445-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36445-114">-DefaultProfile</span></span>
<span data-ttu-id="36445-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36445-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36445-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36445-116">-InputObject</span></span>
<span data-ttu-id="36445-117">Indatavärdet för överföring</span><span class="sxs-lookup"><span data-stu-id="36445-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36445-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="36445-118">-Name</span></span>
<span data-ttu-id="36445-119">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="36445-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36445-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36445-120">-PassThru</span></span>
<span data-ttu-id="36445-121">Returnerar den borttagna kapacitets informationen om åtgärden har slutförts</span><span class="sxs-lookup"><span data-stu-id="36445-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="36445-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36445-122">-ResourceGroupName</span></span>
<span data-ttu-id="36445-123">Namn på den Azure-adressresurs som kapaciteten tillhör</span><span class="sxs-lookup"><span data-stu-id="36445-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36445-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36445-124">-ResourceId</span></span>
<span data-ttu-id="36445-125">Azure Resource-ID</span><span class="sxs-lookup"><span data-stu-id="36445-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36445-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="36445-126">-Confirm</span></span>
<span data-ttu-id="36445-127">Ber användaren bekräfta om åtgärden ska utföras</span><span class="sxs-lookup"><span data-stu-id="36445-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="36445-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36445-128">-WhatIf</span></span>
<span data-ttu-id="36445-129">Beskriver åtgärderna som den aktuella åtgärden utför utan att utföra dem</span><span class="sxs-lookup"><span data-stu-id="36445-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="36445-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36445-130">CommonParameters</span></span>
<span data-ttu-id="36445-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36445-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36445-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36445-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36445-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36445-133">INPUTS</span></span>

### <span data-ttu-id="36445-134">System. String</span><span class="sxs-lookup"><span data-stu-id="36445-134">System.String</span></span>

### <span data-ttu-id="36445-135">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="36445-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="36445-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36445-136">OUTPUTS</span></span>

### <span data-ttu-id="36445-137">Microsoft. Azure. commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="36445-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="36445-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36445-138">NOTES</span></span>

## <span data-ttu-id="36445-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36445-139">RELATED LINKS</span></span>

[<span data-ttu-id="36445-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="36445-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="36445-141">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="36445-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)
